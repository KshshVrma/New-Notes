is used for repository management where you can remotely append/edit the content.

we initialilze the repo with 

git init

we add the files to be tracked with 
git add

we commit the repository with 

git commit

we push the commit to the remote repository with 

git push

to update the commit history:
git cherry-pick -m 1 abc
git cherry-pci abc
git rebase -i HEAD~4

|   |   |   |
|---|---|---|
|`git init`|Initializes a Git repository|Creates `.git/` directory|

|   |   |   |
|---|---|---|
|`git add <file>`|Adds files to staging|Moves files to **staging area**|

|   |   |   |
|---|---|---|
|`git commit -m "message"`|Saves changes permanently|Creates a new **commit**|

|   |   |   |
|---|---|---|
|`git push origin main`|Uploads commits to remote|Updates the **remote repository**|


another good option is git cherry pick : this option allows to pick specific coommits of a differrent branch to be applied to the curretn branch meaning that wihtout copying the previous commits and merging the branches, we can pick up the code from the other branches.