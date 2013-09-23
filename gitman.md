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

status - To print details regarding the changes made in the repository's directory

	Example:
	
	git status 
		Show the status of files in the current directory i.e. Untracked/Unmodified/Modified/Staged


diff - To print details regarding files which have been modified after the last succesful commit 

	Examples:
	
	git diff
		Show the changes made in the tracked (but unstaged) files after the last succeful commit
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
	
mv - To move a file

	Example:
	
	git mv myfile1 myfile2
		Move "myfile1" to "myfile2", remove "myfile1" from repository's directory and start tracking "myfile2"

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
		To revert the changes made and restore "myfile" to the last succesful commit

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

