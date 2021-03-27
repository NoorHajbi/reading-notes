#Read: 01 - The Coder's Computer (Summary)
(1)
Within a terminal there is (a shell) This is a part of OS that defines how the terminal will behave and looks after executing commands.
"the most common one is bash."
 (echo) command can be used, to know which shell is used.
________
(2)
Basic Commands:
pwd ( Print Working Directory).
ls [options] [location] -> (list) It listed the contents of the current directory.
ls -l -> (long listing).
ls -l /etc -> list that directories contents (not current directory).
.......
"File system under Linux is a hierarchical structure:  
The root directory, denoted by a single slash (/). It has subdirectories, they have subdirectories and so on."
path types:
1- Absolute ->begins with a forward slash (/).

2- Relative -> "They will not begin with a slash."
.......
More Paths:
~  -> "A shortcut for your home directory." (/home/ryan/Documents or ~/Documents)

. - "This is a reference to your current directory, As  ./Documents."

.. - "This is a reference to the parent directory. " ../

......
 cd (change directory) ->
ways to use it: (cd Documents) or (cd /) or (cd ~/Documents) or (cd ../../) or (cd)
____________
(3)

"everything is a file in Linux even text file."
.......
-"Linux is an Extensionless System"
Unlike Windows, Linux ignores the extension(.exe/.png/.txt ,etc) and looks inside the file to determine what type of file it is.

.......
Unlike windows: Linux is Case Sensitive.
......
Spaces is ok but not in all cases
for the filename that has over one section you can use ' ' or /, Like: cd 'Holiday Photos' or cd Holiday\ Photos.
......

ls -a -> "List the contents of a directory, including hidden files."