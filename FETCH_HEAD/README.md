Sometimes when you `git fetch` from a directory in your local machine,
a subsequent `git log` won't show the fetched commits.
In this case, you can

- `git log FETCH_HEAD` to see all the logs until the `FETCH_HEAD`
- `git log HEAD..FETCH_HEAD` to see all the logs from `HEAD` to `FETCH_HEAD`
