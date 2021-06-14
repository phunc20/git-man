



## <s>Remove Mistakenly Commited files in Previous Commits</s> Not Working!
<s>The following command needs to be run from the toplevel of the working tree. Otherwise, the command will
simply be ignore, i.e. having no effect, and a warning will be printed at terminal:</s>
```
You need to run this command from the toplevel of the working tree.
```

```bash
git filter-branch --index-filter 'git rm --cached --ignore-unmatch path/to/mistake_file' --tag-name-filter cat -- --all
```



