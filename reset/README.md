## `--soft`
```bash
git reset --soft <commit>
```
As far as I understand, Git's soft reset is somewhat like `git checkout <commit>`, except that with `git checkout` all of your tracked files need to be unmodified (unless you `git checkout -f` by force).
`git reset --soft <commit>` points `HEAD` to the indicated commit while still maintaining the content of your modified files, waiting for a new commit.

One usage of this soft reset is to squash several commits into one single commit.
```bash
git reset --soft HEAD~3
git commit
```
Cf. [stackoverflow](https://stackoverflow.com/questions/5189560/squash-my-last-x-commits-together-using-git?page=1&tab=votes#tab-top)

Another use case is as follows
> 1. You add some works and you commit the changes
> 2. Then you want to push that new commit to your remote repo, but then you
>    realize that the remote repo contains some changes that you forgot to pull back
>    first
> 3. So now you cannot push and your local is one commit divergent from your remote

In this case, you can
1. Create a backup branch for safety at the newest commit: `$ git branch safety`
1. Point `HEAD` one commit backwards: `$ git reset --soft HEAD~1`
1. Pull the latest changes from remote: `$ git pull`
1. Merge the safety branch's changes to master `$ git merge safety`
