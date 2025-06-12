## `fetch`
1. Can we `fetch` btw different directories in one's own machine?
    - Yes. E.g.
      ```bash
      $ cd ~/git-repos/gitlab/phunc20/B
      $ git fetch ~/git-repos/gitlab/phunc20/A
      $ git merge FETCH_HEAD
      ```
      See more at `fetch/README.md` from this repo.
