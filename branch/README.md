There is in addition to the command `git branch`, the option `-a`
```bash
git branch -a
```
which list more branches _that might be hidden from your view_.
- These branches might have a more proper name, like remote branches that are not default.

```bash
~/git-repos/phunc20 ❯❯❯ git clone https://github.com/phunc20/18S191.git
Cloning into '18S191'...
remote: Enumerating objects: 18, done.
remote: Counting objects: 100% (18/18), done.
remote: Compressing objects: 100% (13/13), done.
remote: Total 7022 (delta 10), reused 13 (delta 5), pack-reused 7004
Receiving objects: 100% (7022/7022), 4.47 MiB | 2.33 MiB/s, done.
Resolving deltas: 100% (3458/3458), done.
~/git-repos/phunc20 ❯❯❯ cd 18S191/
~/git-repos/phunc20/18S191 ❯❯❯ ls
homework  lecture_notebooks  README.md  website  website-docs.md
~/git-repos/phunc20/18S191 ❯❯❯ git br
* fall20
~/git-repos/phunc20/18S191 ❯❯❯ git co phunc20
Branch 'phunc20' set up to track remote branch 'phunc20' from 'origin'.
Switched to a new branch 'phunc20'
~/git-repos/phunc20/18S191 ❯❯❯ git st
On branch phunc20
Your branch is up to date with 'origin/phunc20'.

nothing to commit, working tree clean
~/git-repos/phunc20/18S191 ❯❯❯ git br
  fall20
* phunc20

~/git-repos/phunc20/18S191 ❯❯❯ git log
commit ec8a245e32e9f9dc709fdac2f2906c1d4789795e
Author: phunc20 <wucf20@gmail.com>
Date:   Mon Jan 25 12:34:28 2021 +0700

    seems to work; need some cleaning of the code later

commit ca26f80c18984da987ea03d013c6d6bf6a5f7aeb
Author: phunc20 <wucf20.@gmail.com>
Date:   Sun Jan 24 16:51:17 2021 +0700

    afternoon 1st half on 04-gpu.jl

commit a232d1a3d9018592429182224f97299abf1d4c85
Author: phunc20 <wucf20.@gmail.com>
Date:   Thu Jan 21 13:31:17 2021 +0700

    morning reading gpu by Edelman

commit f1215dd62f310151beed4cd4655157071b7fd0bc
Author: Logan Kilpatrick <23kilpatrick23@gmail.com>
Date:   Tue Jan 19 12:47:15 2021 -0800

    Update DeployPage.yml
    
    Switch to main

commit 14ca6fa5178f5c0025c5e845c7c40b7ea219d0dd
Author: Alan Edelman <mit.edelman@gmail.com>
Date:   Tue Jan 12 13:58:26 2021 -0500

    Update README.md

commit 579d832cc06329fcad98ab31a65f220506f78faf
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
