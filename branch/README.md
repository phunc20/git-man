There is in, addition to the `git branch` command, the option `-a`
```bash
git branch -a
```
which list more branches _that might be hidden from your view_.
- These branches might have a more proper name, like remote branches that are not default.
  ```bash
  ~/git-repos/phunc20/18S191 ❯❯❯ git br
  * fall20
  ~/git-repos/phunc20/18S191 ❯❯❯ git co phunc20
  Branch 'phunc20' set up to track remote branch 'phunc20' from 'origin'.
  Switched to a new branch 'phunc20'
  ~/git-repos/phunc20/18S191 ❯❯❯ git br
    fall20
  * phunc20
  
  ~/git-repos/phunc20/18S191 ❯❯❯ git br -a
    fall20
  * phunc20
    remotes/origin/HEAD -> origin/fall20
    remotes/origin/SIR_notebook
    remotes/origin/Spring21
    remotes/origin/Spring21-franklin-output
    remotes/origin/dps/hw1
    remotes/origin/fall20
    remotes/origin/gh-pages
    remotes/origin/hw8
    remotes/origin/phunc20
    remotes/origin/s/hw2
    remotes/origin/s/lecture3
    remotes/origin/seam_carving_example
    remotes/origin/tlienart-deploy
  ~/git-repos/phunc20/18S191 ❯❯❯
  ```
- **`git branch -r`** or `git branch --remote` can be used to view remote branches exclusively.
  ```bash
  ~/git-repos/phunc20/pytorch-Deep-Learning ❯❯❯ git br
  * master
  ~/git-repos/phunc20/pytorch-Deep-Learning ❯❯❯ git br --help
  'br' is aliased to 'branch'
  ~/git-repos/phunc20/pytorch-Deep-Learning ❯❯❯ git br -r
    origin/AIMS-FL18
    origin/AIMS-resolve
    origin/AIMS_readme
    origin/CoDaS-HEP_2018
    origin/HEAD -> origin/master
    origin/ebetica-patch-1
    origin/ebetica-patch-2
    origin/full-master
    origin/master
    origin/phunc20
    origin/revert-44-fix-scrollbar
  ~/git-repos/phunc20/pytorch-Deep-Learning ❯❯❯ git br --remote
    origin/AIMS-FL18
    origin/AIMS-resolve
    origin/AIMS_readme
    origin/CoDaS-HEP_2018
    origin/HEAD -> origin/master
    origin/ebetica-patch-1
    origin/ebetica-patch-2
    origin/full-master
    origin/master
    origin/phunc20
    origin/revert-44-fix-scrollbar
  ```


## Delete A Remote Branch
```bash
git push -d <remote_name> <branch_name>
```
