# git_commands

## Ignoring Files and/or Directories
- git .ignore -> creates a list of files and/or directories to be ignored by git
  - git.ignore.
- git log --oneline --decorate --graph
- git log -p \<path> -> shows the commit history of the file at path
- git log --follow -p -- \<path-to-file-name> -> shows the commit history of the file at `path-to-file-name` beyond name changes
- git stash -> place changes to tracked files in stash buffer
- git stash -p -> cycle through changed files and select changes to be stashed
  - ? -> help
  - / -> search for  a hung by regex
  - n -> don't stash the hunk
  - q -> quit - Any hunks that have been selected will be stashed
  - s -> split this hunk into smaller hunks
  - y -> select this hunk to be stashed

# Bibliography & Resources
1. https://git-scm.com/book/it/v2/Git-Tools-Stashing-and-Cleaning

## Table of Contents
- [[git]]
- [[git_commands]]
- [[git_tags]]
- [[git_workflow]]
- [[index]]
