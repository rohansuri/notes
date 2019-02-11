List of scenario based git commands that are of day to day help.

* Adding more changes to a previous commit  
  Altering changes done in a commit  
  TODO

* Quick view of commit history  
  `git log --oneline`

* Remove a file mistakenly added to the latest commit  
 (a git add folder might add executables/binaries)

```bash
  # HEAD^ means reset to a commit just before HEAD
  git reset --soft HEAD^
  git reset HEAD /path/to/unwanted/file
  
  # -c means reuse a commit object and take it's author info, timestamp, commit message
  # ORIG_HEAD is a reference to the old head. It is set by any dangerous commands (reset here for example)
  # reflogs are a better alternative as they are always set. reflog takes the form HEAD@{1}
  git commit -c ORIG_HEAD

  # One could also do a git reset --mixed HEAD^ and re-add the only files that are required.
```

## Questions

* What are the different modes of reset?

* Difference between index file and working tree?
