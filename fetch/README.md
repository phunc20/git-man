`fetch` means you're fetching, i.e. obtaining, works from a remote repo.
Note that `fetch` can be regarded a better practice than `pull` in that

- It only downloads and saves the work from a remote repo without merging into your local branches.
- This way can avoid conflicts.

Note that one can also `fetch` any Git directories from a local folder to another local
folder. A possible scenario be like

> You want a backup of your `~/.gnupg/` directory in a hard drive.
> Overwriting by either `rsync` or `cp` does not give you peace of mind,
> making you worry whether all files being correctly backed up.

In this case, you may, e.g.

```bash
$ mkdir /tmp/red
$ sudo mount /dev/sdb1 /tmp/red
```

and then use `git log` to check the different commits in both `/tmp/red/.gnupg/`
and `~/.gnupg/` before `fetch`ing.

```bash
$ cd /tmp/red/.gnupg
$ git fetch ~/.gnupg
remote: Enumerating objects: 31, done.
remote: Counting objects: 100% (31/31), done.
remote: Compressing objects: 100% (21/21), done.
remote: Total 28 (delta 9), reused 0 (delta 0), pack-reused 0 (from 0)
Unpacking objects: 100% (28/28), 2.81 KiB | 2.00 KiB/s, done.
From /home/phunc20/.gnupg
 * branch            HEAD       -> FETCH_HEAD
$ git merge FETCH_HEAD
Updating e441a3e..fb6f2c4
Fast-forward
 create mode 100644 tofu.db
```
