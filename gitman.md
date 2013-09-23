Basic Repo handling commands
----------------------------

init - To initialise a git repository in an existing folder

	Examples:
	
	cd myfolder
		go into the directory 
	git init
		create .git directory which contains all repository information


add - To start tracking a file and/or to stage a file
	
	Examples:

	git add file1
		Start tracking file1 if not tracked, if already tracked then stage it
	git add .
		Track/Stage all the files in the folder

commit - To commit the changes made in the repository's directory

	Examples:

	git commit -m "sample_commit"
		Commit the changes made in the file(s) with message "sample_commit"

status - To print details regarding the changes made in the repository's directory

	Examples:
	
	git status 
		Show the status of files i.e. Untracked/Unmodified/Modified/Staged


diff - To print details regarding files which have been modified after the last succesful commit 

	Examples:
	
	git diff
		Show the changes made in the tracked (but unstaged staged) files after the last succeful commit
	git diff --cached
		Show the changes made in the staged files that will go into the nest commit 
	git diff --staged
		(Same as the above, can be used in git 1.6.1 or higher)

rm - To remove a tracked file
	
	Examples:
	
	git rm file1
		Stop tracking the file,remove it from the repository's directory and stage the file's removal
	git rm --cached file1
		Stop tracking the file and stage the file's removal
	
mv - To move a file

	Examples:
	
	git mv file1 file2
		Move file1 to file2, remove file1 from repository's directory and start tracking file2

log - To print commit history in reverse chronological order

	Examples:

	git log
		List the commits made in the repository
	git log p 3
		List the previous 3 commits made in the repository
		
