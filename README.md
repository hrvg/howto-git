# Summary

This repository is a small contribution to github, mainly used as an example workflow for myself but shared as a quick cheat sheet of the main commands.

See also the following useful resources:

- https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners
- https://www.slideshare.net/HubSpot/git-101-git-and-github-for-beginners
- https://guides.github.com/activities/hello-world/
- https://sangsoonam.github.io/2017/02/01/create-pull-request-hub.html

# Cheat sheet

## Initializing git
- git config user.name 'username'
- git config user.email 'username@mail.com'
- git config --global credential.helper "cache --timeout=3600"
- git config --global core.editor 'nano'

## Creating a local repository
- mkdir dummy-project : make directory
- cd dummy-project : change to directory
- git init : create local repository (or repo)
- touch code.txt
- git status : self-explanatory
- git add : adding files to the staging environment (i.e. files to be commited)
- git add code.txt
- git status : self-explanatory
- git commit -m 'Explanatory comment' : commit changes with 'Explanatory comment' to local repo

## Remote repo and sync with local repository
- create a repo on github.com
- git remote add origin https://github.com/username/reponame.git : adding 
- git push -u origin master : pushing master to remote repo i.e. sync-ing changes

## Creating a branch
- git checkout -b 'branch-name' : create a new branch (e.g. to left the main project untouched)
- git checkout branch-name : switch to branch, e.g. git checkout master switch you back to master
- git branch : list branches
- git push origin branch-name ## Pushing branch

## Modifying branch
- git status : verifying in which branch you are working
- gedit code.txt ## Add some random text here
- git status : checking that code.txt has been modified
- git add code.txt : adding code.txt to staging environment
- git status : checking that it has been added 
- git push origin branch-name : pushhing change to the remote repo
- git branch -d branche-name : deleting branch from the local repo
- git push origin --delete branch-name : deleting branch from the remote repo

## Adding a pull request (PR)	
- https://github.com/username/gitname/pulls
- click on 'New pull request', add some text to explain the changes you have made to the code
- you can review changes, add comments, etc
- if everything is okay, 'Merge pull request' will add changes to the main branch
- you can then delete the branch
- git branch -d branch-name : delete the local branch

## Updating local repo
- git checkout master : get into master
- git status : check
- git pull origin master : pulling change from remote repo to local repo

## Workflow
- branch from master or from current branch
- perform changes
- add changes to staging environment
- commit changes
- push changes to remote repo
- pull request
- merge pull request or discuss about changes
- delete branches if needed both locally and remotely
- git fetch -p : prune the local repo to remove ref that are not in the remote repo
