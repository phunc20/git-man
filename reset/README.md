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


