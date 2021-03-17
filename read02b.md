#Read: 02b - Revisions and the Cloud (Summary)

(1) VERSION CONTROL.

Version Control(VCS): is a system that allows change, track modifications, and manage the project.
1. A Local VCS: contains one database on your hard disk.
2. Centralized Version Control(CVCS): Centralized server help to share files with individuals, like team members.
"If a CVCS goes down, collaborators cannot work with each other "
3. Distributed Version Control(DVCS): " Allows clients to create mirrored repositories, 
so the data backups can be easily be placed on the server to replace any lost information." which help you to prevent CVCS faliure.
___________
Git is DVCS that creates a snapshot of the file and stores a reference to it. 
it relies on local operations, so you can continue to work even without internet connection.
___________
(2) History of Git

"Git traces its roots to the open source software project Linux kernel."
"Linus Torvalds, the chief architect of the Linux kernel, began creating Git, With the intention of creating a DVCS."
____________
(3) GETTING STARTED

After installing;
-Git includes inherent Graphical User Interface (GUI) tools, you can access it using this link -> https://git-scm.com/downloads/guis
- git config -> command that modify a configuration text file, like setting your username and email address.
 git config --list  (for check setting)
 git help command (to access manual)
____________
(4) SETTING UP A GIT REPOSITORY
Importing:
To import an existing project or directory into Git ->
cd 'file or directory'
git init (to Initialize Git repository)
git add *.c (add all files with .c)
git add LICENSE
git commit -m “MSG”

Cloning: create a copy of an existing Git repository
the command is -> git clone
____________
(5) WorkFlow

The local Git repository has three components:
Working Directory (The actual files reside here)  Add->  Index(The area used for staging) Commit -> Head(Points to the most recent commit).

Saved File can be *Tracked(can be modified, unmodified, or staged -part of the most recent file snapshot-) or *Untracked(not in the last snapshot).
"*After cloning a repository, files have tracked status and are unmodified because they have been checked out but not edited."

The Life Cycle of File Status:
"After you edit a file, Git flags it as modified because of changes made after the previous commit. -> You stage the modified file ->
you commit staged changes."
Command To Check File Status ->  git status 
_
Track one file -> git add filename
Track all files -> git add *
"After using these commands, files are tracked and staged for committing."

commit the changes -> git commit -m “made change x,y,z” // for all git commit -a

push changes to a remote repository ->  git push origin master // local is “master”, the remote repository is “origin”.

temporarily removes changes and hides them -> git stash
use this command again to retrieve the hidden changes.

Noor Hajbi, 16/03/2021.