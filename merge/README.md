## W/o Inheriting The Commits: `--squash`
The verb **"squash"**'s mental model is the action of
forcibly flattening, say, a can.

`--squash` in `git merge` means squashing a whole bunch
of commits into one single, new, commit.

Say, you're on branch `A` and you want to merge files
on branch `B`, discarding the extra commits on `B`, you can
```sh
git merge --squash B
```

