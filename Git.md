# Version Control 
is a system that allows you to revisit various versions of a file or set of files by recording changes. **Through version control**, one can revert a file or project to a previous version, track modifications and modifying individuals, and compare changes. By utilizing a Version Control System (VCS), mistakes with files can easily be rectified.

**Git is a DVCS** (Distributed Version Control systems)
If a CVS goes down, collaborators **cannot** work with each other on a file or save changes and new versions
## git beifitis:
- Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server
- very single change applied to any file or directory is tracked by Git.
-  Git makes it extremely difficult for a snapshot of your file that is committed to be lost.
- Files in Git can reside in three main states: committed, modified and staged.

1- Committed Data is securely stored in a local database

2- Modified File has been changed but not committed to the database

3- Staged Flagged a file’s changed version to be committed in the next snapshot.
 
There are three ways to get more information on a particular command, by accessing the manual:

1- git help command

`git command --help`

`man git-command`

to import an existing project or directory into Git

`$ cd test (cd = change directory)`

Use the git init command
`$ git init` 

To start tracking these repository files, perform an initial commit by typing the following:

`$ git add *.c`

`$ git add LICENSE`

`$ git commit -m “any message here” `


## cloaning
You can also create a copy of an existing Git repository from a particular server by using the clone command with a repository’s URL:

`$ git clone https://github.com/test`


 ## The Life Cycle of File Status
1-After you edit a file, Git flags it as modified because of changes made after the previous commit.

2-You stage the modified file.

3-Then, you commit staged changes.


Committing a File
`$ git commit -m “made change x,y,z”`


Committing All Changes
$ git commit -a




