Git Configuration 
-----------------

config - command used to configure git and view configurations

	Example:

	git config --global user.name "Sam"
		Configures the user name as "Sam" in ~/.gitconfig
		
	git config --global user.email "samwaterston@gmail.com"
		Configures the user's email as "Sam" in ~/.gitconfig
		
	git config user.name "Tony"
		Configures the user name as "Tony" in .git/config for that directory
		
	git config --list
		List all the currently configured values.

Basic repo handling
-------------------

init - To initialise a git repository in an existing folder

	Example:
	
	git init
		Create .git directory (contains all repository information) in the current directory


add - To start tracking a file and/or to stage a file
	
	Examples:

	git add myfile
		Start tracking "myfile" (if not tracked) and stage "myfile"
	git add .
		Track/Stage all the untracked/unstaged files in the current directory

commit - To commit the changes made in the repository's directory

	Example:

	git commit -m "sample_commit"
		Commit the changes made in the staged file(s) with the message "sample_commit"
		
	git commit -a -m "sample commit"
		Commit changes made in all the files currently being tracked

status - To print details regarding the changes made in the repository's directory

	Example:
	
	git status 
		Show the status of files in the current directory i.e. Untracked/Unmodified/Modified/Staged


diff - To print details regarding files which have been modified after the last succesful commit 

	Examples:
	
	git diff
		Show the changes made in the tracked (but unstaged) files after the last successful commit
		
	git diff --cached
		Show the changes made in the staged files that will be recorded in the next commit
		
	git diff --staged
		(Same as the above, can be used in git version 1.6.1 or higher)

rm - To remove a tracked file
	
	Examples:
	
	git rm myfile
		Stop tracking "myfile", remove it from the repository's directory and stage "myfile" removal
		
	git rm --cached myfile
		Stop tracking "myfile" and stage "myfile" removal from the repository
	
mv - Rename a file

	Example:
	
	git mv myfile1 myfile2
		Stage the renaming of myfile1 to myfile2

log - To print commit history in reverse chronological order

	Examples:

	git log
		List the commits made in the repository
	git log p -3
		List the previous 3 commits made in the repository
		
reset - To unstage a staged file

	Example:
	
	git reset HEAD myfile
		Unstage the staged "myfile" file
	
checkout - To unmodify a modified file

	Example:
	
	git checkout -- myfile
		To revert the changes made and restore "myfile" to the last successful commit

Remote Handling
---------------

remote add - To add a remote

	Example:

	git remote add origin https://github.com/fosscell/gitworkshop.git
		Add a remote server under the name "origin" with url "https://github.com/fosscell/gitworkshop.git"

pull - To fetch the changes from the remote and merge with the local repository

	Example:
	
	git pull origin master
		Fetch and merge the changes on the branch "master" on the remote "origin" 
		
push - To push the commits to a remote server

	Example:

	git push origin master
		Update the changes made in the local branch "master" (the default branch) on the remote "origin"

remote show - To print the details of a specific remote

	Example:

	git remote show origin
		Show all the details of the remote "origin"

remote rename - To rename a remote

	Example:
	
	git remote rename origin mynewremote
		Rename the remote "origin" to "mynewremote"

remote rm - To remove a remote

	Example:
	
	git remote rm mynewremote
		Remove the remote "mynewremote"

remote set-url - To change the url of a remote

	Example:

	git remote set-url origin https://github.com/fosscell/bashworkshop.git
		To change the current url of the remote "origin" to the new url "https://github.com/fosscell/bashworkshop.git"
	
Branching
---------

branch - To create/delete a new branch

	Example:
	
	git branch mybranch
		Create a new branch called "mybranch"
		
	git branch -d mybranch
		Delete the branch "mybranch" 
		
checkout - Switch to a different branch

	Example:
	
	git checkout mybranch
		Switch to the branch "mybranch"
		
	git checkout -b newbranch
		Create a branch called newbranch and switch to it
		
fetch - To fetch the changes from a remote repository

	git fetch origin
		Fetch the changes from the remote "origin"
		
merge - Merge two branches

	git merge mybranch
		Merge the changes from mybranch with the currently checked out branch

push - push the changes in your local repo to a remote repo

	git push origin
		Push the changes in all local branches to the remote "origin"
		
	git push origin master
		Push only the changes in the master branch to the remote "origin"
		
pull - fetch the changes from a remote repository and merge it with the local branches

	git pull origin mybranch
		Merge into the current branch the remote branch "mybranch"
		
	git pull origin
		Merge the currently checked out local branch with the branch pointed to be HEAD in the remote repository
