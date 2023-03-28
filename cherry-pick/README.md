One use case of the `cherry-pick` command is as follows.
1. Imagine that we are on branch Y whereas we thought that we were on branch X
2. We made new changes destined for branch X on branch Y
3. We `git commit`

How do we **carry the changes introduced in the last commit on branch Y to branch X**?

Denoting the commit hash of the newly introduced modification by `<commit_hash>`, we
could use the following code to carry the latest change to branch X.
```bash
$ git co X
$ git cherry-pick --no-commit <commit_hash>
```







