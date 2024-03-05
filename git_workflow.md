# Git_workflow

Setting up multiple branches to facilitate passing the application from step to step until it reaches production.

## Branches

- production - real data, real users, real important
  - only tagged 
  - hotfixes - fix bugs in production
- staging (blue/green) - duplicate of production environment which is the final set of checks before going into production
- main (dev) - The branch that hold code under Development
  - feature - branches checked out for the development of specific functionalities
  - these branches will be merged back into main before going into staging and then production
- demo - Demo branch mimics production 
  - code should be pushed to demo as part of the production step
  - has a demo-db that can safely be changed to do sales and/or training
  
## Commits
- Associate the commit with an issue ticket
- Name commits as type/description/[person]
  - type [bug_fix | feature | ux_update ] for example
  - description - Tells what is being changed
  - person is optional in case the PR is being worked on by a team


- [[git]]
- [[git_commands]]
- [[git_tags]]
- [[git_workflow]]
- [[index]]