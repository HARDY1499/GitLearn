Git Learning

Create by Linus Torvalds (the Genius that created Linux Kernel xD)

Git is a distributed version control system used to - 
* easily recover files
* see who introduced a bug and when
* roll back to a previously working state

Types of VCS (Version Control System) - 
1. Local VCS - when the versions of a repository are stored locally on a storage device to provide backup and help rollback.
2. Centralised VCS - when the versions of a repo are stored on a central server where everyone can pull and push onto the server.
3. Distributed VCS (like Git) - when the versions of a repo are stored on a server, but the backups are also available when needed on the machines of everyone who is working on it (hence the distributed keyword).

Git Features - 
1. Captures snapshots of project and not the new differences.
2. Almost every operation is local
3. Git has integrity. It uses checksums(checksum is a string that accompanies a file and this cs is used to verify whether or not the file has been tampered with) to verify file integrity.

There are 3 areas in a git project directory:
1. working directory (local)
2. staging area (ready to be committed to the repo)
3. git directory (repo)

￼

Git Commands :

* git status : to check status of a git folder
* git init : initialise a folder as a git repository
* git add . (OR git add --a):  to add all the files to the staging area (previously untracked files are now being tracked for any modifications)
* git commit -m “message” :  commits the files in the staging area and adds a description message with it
* git log : log of all the commits up until now.
* rm -rf .git : deletes the .git folder, deleting the whole repo. The files still remain there but the past commits are no longer accessible
* git clone : this command is used to clone a repo using the repo url 
* touch .gitignore : touch is a linux command which can be used to create a new file “.gitignore” which is used to make a list of files that git will ignore. Adding the names of the files that you want git to ignore to the “.gitignore” file will work. You can use “*.filetype” to ignore all the files of the same type in the given dir. To ignore a folder use “Foldername/“ format and any folder of the same name and its contents will be ignored.
* git diff : this command is used to compare the contents of working directory and staging area. It helps point out the differences in a file version that is in the staging area and the same file with a different version in the working area
* git diff --staged : compares the current staging area to the last commit you performed.
* git commit -a -m “message” : Any files that were previously staged but have been modified and the new version has not been staged will be directly committed. This is used to bypass the staging area and directly commit. However, untracked file will not be committed.
* git rm filename.doc : used to delete a file from a working directory and this change will directly be visible in the staging area
* git mv filename.txt filename_renamed.txt : this is the move command which is used to move one file to another or in this case , we have used the move command to rename the file by moving it. This renamed file will also be staged.
* git rm --cached filename.txt : this will untrack the file explicitly if it was already being tracked
* git log -p : to see the log of commits as well as the changes made in those commits
* git log --stat : to see the log of commits as well as a shorter summary of changes made in those commits
* git log --pretty=oneline : to see the log of commits as well as the messages in one commit per line (generally used for printing a log)
* git log --pretty=short/full
* git log --since=2.days : will show you the log for commits since last 2 days
* git commit --amend : to amend or modify the last commit and also amend the commit message
* git restore --staged filename.txt : is generally used to unstage a previously staged file
* git checkout -- filename.txt : will restore the modified file to its version from the last commit
* git checkout -f : will restore all the modified files to their versions from the previous commit. Basically all files will revert to previous commit.
* git remote add <remotename> <link_to_repository_on_github> : this command is used to add a repository on GitHub as a remote on to your git working directory on you local pc. Generally the remotename is set to “origin”.
* git remote -v : used to view the available repositories you can pull from or push to

Before getting to the next point, an SSH key needs to be added to your GitHub account for granting your computer access to the remote repository. For this you need to Google : “ssh keys GitHub” and the first link will guide you through the procedure you need to follow to generate and add ssh keys to your GitHub account.

* git push -u origin master : this command is used to push your working directory into the remote repository that in this case is name “origin” into the master branch.
* git config --global alias.st status : this command is the alias command which can be used to change the alias of a command like status into st so that when you use the command “git st “ it runs the status command. This can be done for any other git command like push, commit, log etc.
* git checkout master : is used to return back to the master branch in the git repo
* git branch : to see all the current branches of this repo

It is highly recommended to first ensure that your working tree is clean before you switch branches in git. Ensure you commit the staged files and that the tree is clean when status is checked

* git merge branchname : this command will merge the current branch with the given “branchname”. This can lead to conflicts based on changes you made in this other branch. Depending on which changes you want to keep, you then have to add the new modified files to staging area and then commit them. 
* git branch --merged : shows already merged branches
* git branch --no-merged : shows not merged branches
* git branch -d branchname : to delete a branch. if the branch is not merged this will give you an error
* git checkout -b branchname : this command is used to make a new branch
* git push -d origin branchname : this command is used to delete a branch from your remote repo

The branching workflow has 2 parts : Long Running Branches and Topic Branches. As the name suggest the long running branches are the main branches that last as long as the project is still under progress and Topic Branches are the branches which are topical and will be terminated once that topic comes to a conclusion.





