1. What if I mistakenly commit on `develop` branch while what I wanted to do was
   to create a new branch and commit on that branch?
   - Multiple solutions are possible, it seems
     1. Remove local `develop` branch and then re-track `origin/develop` again.
        ```bash
        git br -D develop
        git co --track origin/develop
        ```
     1. Use `reset`. Cf. <https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git?page=1&tab=scoredesc#tab-top>
