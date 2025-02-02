The command `git ls-files` can list (recursively)
all Git tracked files under the current directory,
pretty much like the Linux command `ls`.

| Git | Linux |
| --- | ----- |
| `git ls-files` | `ls` |
| `git ls-files .` | `ls .` |
| `git ls-files src/` | `ls src/` |


# Different Usecases
- To grep keywords in tracked files only, e.g. finding all Python scripts
  containing usage of f-strings
  ```bash
  # Initial guess
  $ grep -n "f\"" $(git ls-files)
  # Better yet
  $ grep -n "[^a-Z0-9]f\"" $(git ls-files **/*.py)
  ```
- Find git-tracked files with particular extensions, e.g.
  finding images of some Hugo website
  ```bash
  $ git lf content/*.jpg
  ```
  Regex are supported, e.g. finding JPEG w/o `logo` in the file name
  ```bash
  $ git lf *[^logo].jpg
  ```

