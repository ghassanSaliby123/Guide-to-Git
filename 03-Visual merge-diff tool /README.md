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

-------------------------
### Brnaching and merging
- Get the branches `git branch`
- Get the local and the remote branches `git branch -a`
- Create a new branch `git branch <branch_name>`
- Switch to another branch 'git checkout <the_other_branch_name>'
- Change the name of the branch `git branch -m <current_name> <new_name>`. The -m stands for move.
- Delete a branch `git branch -d <branch_name>`. The -d for delete , should not be on the branch while we delete it
- Show the difference between 2 branches `git diff <branch1> <branch2>`. We can also use the difftool
### Merge 2 branches
Merge will default do a fast forward merge which literally move your main branch's tip forward to the end of your feature branch. This keeps all commits created in your feature branch sequential while integrating it neatly back into your main branch. <br>
If we make a change on a branch then switch to main branch and do another changes before doing the merge. The merge here will be called an automatic merge.
Sometimes it leads to conflicts when we change the same file on different branches. Here we can use the mergetool to resolve the conflict. 
`git merge <the_source_branch>` <br>
<b>Note: </b>.orig file is the original copy of the file saved by git 

