1. pwd
Command
pwd
Full Form
Print Working Directory
Purpose

Shows your current location in the file system.

Example
pwd

Output:

/home/ubuntu
Real Life

Like asking:

"Which room am I currently standing in?"

2. ls
Command
ls
Purpose

Lists files and folders in the current directory.

Example
ls

Output:

notes.txt
linux
project
3. ls -l
Command
ls -l
Purpose

Shows detailed information.

Displays
Permissions
Owner
Size
Date
File Name
Example
-rw-r--r-- 1 user user 120 notes.txt
4. ls -a
Command
ls -a
Purpose

Shows hidden files.

Example
.
..
.git
.vscode
Important

Git repositories contain:

.git

which is hidden.

5. ls -la
Command
ls -la
Purpose

Shows:

Hidden files
Detailed information

Most commonly used version.

6. cd
Command
cd foldername
Full Form
Change Directory
Purpose

Move into another folder.

Example
cd linux
7. cd ..
Command
cd ..
Purpose

Move one level up.

Example

Current:

/home/ubuntu/linux

After:

cd ..

Result:

/home/ubuntu
8. cd ~
Command
cd ~
Purpose

Move to home directory.

Example
/home/ubuntu
9. cd /
Command
cd /
Purpose

Move to root directory.

Example
/

Top-most location in Linux.

10. tree
Command
tree
Purpose

Shows folder structure visually.

Example
project
├── linux
├── git
└── networking
Note

May require installation.

11. find
Command
find . -name "*.txt"
Purpose

Search files and folders.

Example
find . -name "*.md"

Output:

Linux_Notes.md
Git_Notes.md
12. locate
Command
locate notes.txt
Purpose

Quickly find files.

Note

May not be installed everywhere.