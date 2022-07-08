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
E.g.
```
$ git diff --name-only 7c9f41e91e718790e0096144d7e0f66fefe5b370
blame/README.md
branch/README.md
checkout/README.md
config/README.md
diff/README.md
key/README.md
reset/README.md
stash/README.md
```


## `--compact-summary`
This option is somewhat like `--name-only`: It shows the number of edited lines in addition
```bash
$ git diff --compact-summary 7c9f41e91e718790e0096144d7e0f66fefe5b370
 blame/README.md (new)    | 26 ++++++++++++++++++++++++++
 branch/README.md         |  4 ++++
 checkout/README.md (new) | 76 ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
 config/README.md (new)   | 25 +++++++++++++++++++++++++
 diff/README.md           | 14 ++++++++------
 key/README.md (new)      |  1 +
 reset/README.md (new)    | 15 +++++++++++++++
 stash/README.md (new)    |  8 ++++++++
 8 files changed, 163 insertions(+), 6 deletions(-)
```
