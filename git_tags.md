# git_tags

git_tag - A name that points to a commit
- Marks a particular point in hx
- Use for releases

## Lightweight vs Heavyweight tags
- Heavyweight Tags have a message associated with them
- Creating Tags  
  ```
  ## Lightweight Tag
  $ git tag [target]
  ```
  ```
  ## Heavyweight
  $ git tag target [-m "Message making heavyweight"]
  ``` 
- Showing Tags
  ```
  $ git show tag_name
  ```

## Tag Convention
- Tags are similar to branches except they are not supposed to change over time. (Ie it points to a particular revision and never changes over time.)




- [[git]]
- [[git_commands]]
- [[git_tags]]
- [[git_workflow]]
- [[index]]