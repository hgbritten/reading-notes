# Revisions and the Cloud

## The History of Version Control
  - Local VCS (orignally designed so programmers could work on a project with many states, but only on one hard disk)
  - Centralized VCS (SOMEONES HARD DISK BROKE AND WE LOST EVERYTHING!! Designed so that many programmers could work on the same project with that project being stored on a single server)
  - Distributed VCS (THE SERVER HARD DISK BROKE AND WE LOST EVERYTHING!!! Designed so that if a CVS goes down not all hope is lost. The DVC invention of the DVC has undoubtedly saved countless hours of work and streamlined working together as a team to finish projects)
  
### What is Git?
  - A DVCS that tracks all changes made and prevents the loss of data
  - Created my the great Linus Torvalds after a dispute over another popular DVCS BinKeeper
  - Git has many customizable features and is obviously easy for anyone interested in coding to start using considering we are using it on our first day of 102
  
#### How does it work?
  - Once Git is installed on your computer and set up with your name and email it is time to ***clone*** your work! EXAMPLE: git clone https://github.com/test
  - The _working directory_ has all the files for the repository that you cloned
  - The _index_ is the area used for staging
  - The _head_ is the most recent changes that have been made

#### Saving? Tracked vs. Untracked
  - **Tracked** changes were made and were part of the most recent snapshot. If you run a get status command and the message says something like nothing to commit all your files are tracked
  - **Untracked** were not in the last snapshot and are not ready to be committed, these can be seen with git status command

#### Tracking and staging new files
  - To track a *single* file use the command git add filename
  - To track *all* files use the command git add . or *

#### When committing a file always use the git commit -m command and leave yourself a message ALWAYS or you might get lost forever to the timeless void

#### When everything you need to commit is ready and committed use the git push origin main command the master command is now outdated

#### Stashing - great to use when you are not ready to commit the changes you have made. Use git stash to stash them and git stash apply to see them again

##### To see your remotes by running the git remote command 

[<== Back](README.md)
