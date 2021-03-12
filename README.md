# useful-git-commands
git commands
--------------

	Initial Setup and config
	-------------------------
	git config --global user.email youremailhere
	git config --global user.name yournamehere

		Now to check if they are correctly set up
		git config --global user.email
		git config --global user.name

	git init
	Initialized empty git repository in C:/Users/nns/Desktop/.git

		To see this hidden .git folder
		ls -lart

git status
	To check current status. 
	For example if any file is untracked by git currently
	If any file is untracked , it will be shown
	Now if you want to track that file with git , you can use git add
		gid add file1.html
		//So now this file is in the staging area
		//Quick fact: Areas in git ---> Untracked , Staged , Unmodified , Modified
		//Now check git status
			It says: Changes to be commited.		(i.e the file is now in the staging area. you can commit now)

git status -s
	gives short summarised status


To commit changes
	git commit
		OR
	git commit -m "some commit message"

Pro tip: Keep checking git status

Suppose a file in staging area were modified and you wanted to roll back changes to previous commit state
	git checkout file1.html

Suppose all files in staging area were modified and you wanted to roll back changes to previous commit state
	git checkout -f

To check what all has been commited
	git log

To see only previous 5 commits
	git log -p -5



git diff command
-----------------
compares working tree with staging area

How to compare staging area with last commit
	git diff --staged

Deleting files
---------------
	git rm file1.html
	Deletes file from working directory and staging area

	What if I only want to remove file from staging area?
		git rm --cached file1.html

To check which branch are you on
	git branch
To change branch
	git checkout sample	//this will change your branch to branch 'sample'

Merging two branches in git
---------------------------
Say you are in branch 'good' and you want to merge branch 'boy' with it
	git merge boy



