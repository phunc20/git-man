## `--shortstat`
This option allows us to see how many lines have been modified.
```bash
$ git diff --shortstat attributes.json
1 file changed, 1375 insertions(+), 1375 deletions(+)
```


## `--staged`
After you `git add` your files, when you `git diff`, you won't be able to see the difference any more;
the `--staged` option comes to rescue:
```bash
git diff --staged [filename]
```


## `--name-only`
Sometimes what we want to know is which files are different between two commits. In this case,
we can use commands similar to the following:
```bash
git diff --name-only SHA1 SHA2
git diff --name-only HEAD~10 HEAD~5
```


