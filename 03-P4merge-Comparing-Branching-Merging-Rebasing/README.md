## This section covers the following:
- p4merge tool
- Comparing
- Branching and merging
- Rebasing

--------------------
### Install and configure p4merge tool
After configuring the p4merge tool (as explaineed in the pdf) we can use `git difftool` instead if `git diff`
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
### Branching and merging
- Get the branches `git branch`
- Get the local and the remote branches `git branch -a`
- Create a new branch `git branch <branch_name>`
- Switch to another branch 'git checkout <the_other_branch_name>'
- Change the name of the branch `git branch -m <current_name> <new_name>`. The -m stands for move.
- Delete a branch `git branch -d <branch_name>`. The -d for delete , should not be on the branch while we delete it
- Show the difference between 2 branches `git diff <branch1> <branch2>`. We can also use the difftool
![01 Branch-2 kopiera](https://user-images.githubusercontent.com/93892538/182479420-1badf6b5-2333-4240-8f0d-36d32966fcee.png)
### Merge 2 branches
Merge will default do a fast forward merge which literally move your main branch's tip forward to the end of your feature branch. This keeps all commits created in your feature branch sequential while integrating it neatly back into your main branch. <br>
If we make a change on a branch then switch to main branch and do another changes before doing the merge. The merge here will be called an automatic merge.
Sometimes it leads to conflicts when we change the same file on different branches. Here we can use the mergetool to resolve the conflict. 
`git merge <the_source_branch>` <br> 
<b>Note: </b>.orig file is the original copy of the file saved by git.
![02 Branch-1 kopiera](https://user-images.githubusercontent.com/93892538/182480334-aa615668-594c-4115-beeb-f15fbfcb23e2.png)

---------------------------
### Rebasing
For example, we do some changings on branch A and another changes on branch B, when we want to merge B to A, it simply write all the commits from B as one commit to A. With rebasing git rewrites all the commits from B to A. <br>
`git rebase <target_branch>`<br>
Rebasing the remote branch with the local branch through pull `git pull --rebase origin main`. Better to update the references between the local repositpry and the remote one through `git fetch origin main` command first 
 ![1_K4anH9QzRcPqLCv-7HyiCQ](https://user-images.githubusercontent.com/93892538/182480421-b501a4e5-8634-41e7-8e84-f91b79544b2d.png)

---------------------------
### Rebasing VS Merging
![hkftpmgzz7ixtqaxldsw](https://user-images.githubusercontent.com/93892538/182480628-f3f75784-e6e8-4d03-8651-1a518d62fea2.jpeg)
