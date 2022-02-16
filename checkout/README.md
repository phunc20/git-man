## Go Back from `git reset --soft`
Say, you went to some earlier commit by `git reset --soft 79fa5bf`, and
you want to go back to the latest commit.

`git log --all` could help you locate yourself, but

> you should `git co main` instead of `git co <latest_commit_id>`

```bash
~/git-repos/phunc20/git-man$ git log --all --oneline --graph
* 73dea82 (origin/main, origin/HEAD, main) squash several commits into one using
| * bbf6f31 (test_rebase) rebase note taking
|/
* 69e259a diff --name-only
* 181196a how to delete a remote branch
* 7c9f41e rm and rm --cached: take note
* 5ce7da4 about git diff
* 65eb849 ignore recursively files with a certain pattern
* 9aeb58f take note how to delete remote branch
* acbfb33 usage of ~/.ssh/config file to specify ssh key
* 7c2eda1 remove committed file in old commits: Failed
* 79fa5bf (HEAD) git grep
* 20f0ae1 1st ever commit of this repo; git br
* 0960e9b Initial commit
~/git-repos/phunc20/git-man$ git co 73dea82
Previous HEAD position was 79fa5bf git grep
HEAD is now at 73dea82 squash several commits into one using
~/git-repos/phunc20/git-man$ git st
HEAD detached at 73dea82
nothing to commit, working tree clean
~/git-repos/phunc20/git-man$ git log --all --oneline --graph
* 73dea82 (HEAD, origin/main, origin/HEAD, main) squash several commits into one using
| * bbf6f31 (test_rebase) rebase note taking
|/
* 69e259a diff --name-only
* 181196a how to delete a remote branch
* 7c9f41e rm and rm --cached: take note
* 5ce7da4 about git diff
* 65eb849 ignore recursively files with a certain pattern
* 9aeb58f take note how to delete remote branch
* acbfb33 usage of ~/.ssh/config file to specify ssh key
* 7c2eda1 remove committed file in old commits: Failed
* 79fa5bf git grep
* 20f0ae1 1st ever commit of this repo; git br
* 0960e9b Initial commit
~/git-repos/phunc20/git-man$ git br
* (HEAD detached at 73dea82)
  main
  test_rebase
~/git-repos/phunc20/git-man$ git co main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
~/git-repos/phunc20/git-man$ git st
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
~/git-repos/phunc20/git-man$ git log --all --oneline --graph
* 73dea82 (HEAD -> main, origin/main, origin/HEAD) squash several commits into one using
| * bbf6f31 (test_rebase) rebase note taking
|/
* 69e259a diff --name-only
* 181196a how to delete a remote branch
* 7c9f41e rm and rm --cached: take note
* 5ce7da4 about git diff
* 65eb849 ignore recursively files with a certain pattern
* 9aeb58f take note how to delete remote branch
* acbfb33 usage of ~/.ssh/config file to specify ssh key
* 7c2eda1 remove committed file in old commits: Failed
* 79fa5bf git grep
* 20f0ae1 1st ever commit of this repo; git br
* 0960e9b Initial commit
~/git-repos/phunc20/git-man$ git br
* main
  test_rebase
```
