Project commands explanation:
Note : Some commands might be missing as this file has been written three days after the project has been completed. 

1. Set Up the Repository:
	a. Create a new Git repository in a dedicated directory for the project:
		git init task-manager
		cd task-manager


b. Create a text file named (tasks.txt) to serve as your simple task database.
		Created a file using VS

2. Add Initial Tasks:
a. Add some initial tasks to tasks.txt , such as:

b. Stage and commit these changes:
		git add . 
		git commit -m "Intial Commit"  

3. Create Branches and Work on Features:
a. Create and move to a new branch called (feature/add-tasks) to add new tasks:
		git checkout -b feature/add-tasks

Project details

b. Add more tasks to tasks.txt and commit them:
		git add . 
		git commit -m "2nd Commit"  

c. Create and move to another branch called (feature/remove-tasks) to remove
some tasks:
		git checkout -b feature/remove-tasks


d. Remove a task from tasks.txt and commit the change:

		git add . 
		git commit -m "First Commit in Remove-tasks"  

4. Merge Branches and Handle Conflicts:
a. Switch to the (master) branch and try to merge (feature/add-tasks) and
(feature/remove-task) one by one, expecting a conflict:
b. If a conflict occurs, resolve it by editing (tasks.txt), keeping the desired changes,
then stage and commit the resolution:
		
		git checkout master
		Merge branch 'feature/remove-tasks'
		nano feature/add-tasks.txt
		git add . 
		git commit -m "Merge branch 'feature/remove-tasks'"  


5. Use Git Rebase:
a. Create and move to a new branch (feature/update-tasks) to update some tasks:
		
		git checkout -b feature/update-tasks
		
		
b. Make changes to (tasks.txt) and commit them:
		
		echo "- Review Git merge and rebase" >> tasks.txt
		git add . 
		git commit m "1st Commit in update" 

c. Use rebase to integrate changes from (feature/update-tasks) into the (master)
		
		git checkout master
		git rebase feature/update-tasks 

7. Reverting to Previous Commits:
a. Make an incorrect change to tasks.txt:
		
		# Add incorrect task
		git add . 
		git commit m "Add incorrect task" 

b. Use git revert to undo the commit:
		
		git revert 0dbe4a418c9ca179b1d0b4ff8c6ba7dabc851f39 
		git add . 
		git commit  

Working with Remote Repository:
a. Create a remote repository on GitHub.
		
		# Created using GitHub web 

b. Link and push the local repository to the remote repository:
		
		git status 
		git add . 
		git commit 
		git remote set-url origin https://github.com/Gearvian/task-manger.git 
		git push -u origin master
