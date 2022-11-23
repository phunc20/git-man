git config lfs.https://gitlab.com/phunc20/nlp_learning.git/info/lfs.locksverify true



## Troubleshoot
- If you only set up LFS at some computer and that you have multiple machines
  already developping the same project before introducing LFS, then, on your
  other machine, simply `git pull` wouldn't give you those big files in LFS;
  instead, it seems that you need to **`git lfs pull`**


