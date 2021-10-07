## Basics
- `git rm <file>` will remove that file from Git's index as well as from the filesystem. The latter means that, when you `ls <file>` after `git rm`ing it, you will not see the file any more.
- To remove the file from Git's index and keep the file on the filesystem, one can use `git rm --cached <file>`.
  In other words,
  ```bash
  git rm <file>
  # is equiv. to
  git rm --cached <file>; rm <file>
  ```


## <s>Remove Mistakenly Commited files in Previous Commits</s> Not Working!
<s>The following command needs to be run from the toplevel of the working tree. Otherwise, the command will
simply be ignore, i.e. having no effect, and a warning will be printed at terminal:</s>
```
You need to run this command from the toplevel of the working tree.
```

```bash
git filter-branch --index-filter 'git rm --cached --ignore-unmatch path/to/mistake_file' --tag-name-filter cat -- --all
```



