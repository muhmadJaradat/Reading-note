# **Vision control System**
VCS allows you to make different versions of your code every time you make a change which will make tracking modifications and comparing changes more easier.
## **Local Version Control**
The local version control make these versions only on your computer where no one else can see it remotely.
## **Centralized Version Control**
CVC saves versions for several developers in a server where all these developers who have access to the server see these versions of others to share their knowledge between them.
## **Distributed Version Control**
Distributed Version Control systems (DVCS) solves the major concerns in the CVCS like if the server goes down,collaborators cannot work with each other on a file or save changes and new versions.Also, in the event of corruption of a central database’s hard disk — with the absence of backups — all work will be lost, except for any portions on local machines.
DVCS solves this by making mirrored respositories. These data backups can be easily be placed on the server to replace any lost information.
## **Git**
Git is basically a DVCS that store data everytime you make a commit it create a snapshot of the your file and stores a reference to it, so like this you will have new version every time you make change in your file. However, these versions stored only locally on your hard disk.
## ***states***
Git files could be found in three states:

*1.Committed:*

Data is securely stored in a local database.

*2.Modified:*

File has been changed but not committed to the database.

*3.Stages:*

 Flagged a file’s changed version to be committed in the next snapshot.
 ![](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png).
 ## **Local Repository Structure**
 The local Git repository has three components:

1. Working Directory: The actual files reside here.
2. Index: The area used for staging
3. Head: Points to the most recent commit
![](https://blog.udemy.com/wp-content/uploads/2015/08/image036.png)
## **Saving changes**
All in the project are either in a tracked or untracked state.
#### **Tracked**
Tracked files can be modified, unmodified, or staged; they were part of the most recent file snapshot.

####  **Untracked**
Untracked files were not in the last snapshot and do not currently reside in the staging area.

## **The Life Cycle of File Status**
1- Editing a file in Git flages it as a modified file.

2- After that you stage the modified.

3- Then, if you want to save these changes commit these staged changes.

![](https://blog.udemy.com/wp-content/uploads/2015/08/image006.png)
## **Check File Status**
To figure out your file status, use git status command
## **Tracking and Staging a New File**
Use the command git add filename to track a single file. And for tracking all files in a repository by using the following command:
git add *
## **Committing a File**
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

$ git commit -m “made change x,y,z”
For committing all changes use the following command:
$ git commit -a
## **Pushing Changes**
For exporting and pushing the changes to a remote repository, so others can see it, use the following command: 
$ git push origin master
## **Stashing Changes** 
Use: Git Stash to temporarily removes changes and hides them, giving you a clean working directory. and When you are ready to continue working on the changes, simply use the git stash apply command to retrieve the hidden changes.

