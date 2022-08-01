### Install and configure p4merge tool
After configuring the p4merge tool we can use `git difftool` instead if `git diff`
### Comparing the working directory with the staginng area
`git diff`
### Comparing the working directory with the latest commit
`git diff HEAD` HEAD is a reference to the latest commit on the current branch 
- we can cheack what HEAD refers to through `cat .hit/HEAD`
### Comparing the staging area with last commit
`git diff --staged HEAD`
### Comparing several commits
Get the commit ID through `git log` then `git diff <ID1> <ID2>` 
- We can compare the last 2 commits `git diff HEAD HEAD^` since HEAD^ refers to last commit -1 
### Compare the local master branch with the remote repository
`git diff main origin/main` since main is the local branch and origin/main is remote_repository_name/remote_branch_name
-------------
=============================-----------------
