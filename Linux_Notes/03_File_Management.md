1. mkdir
Command
mkdir foldername
Full Form
Make Directory
Purpose

Creates a new folder.

Example
mkdir linux

Check:

ls

Output:

linux
Create Multiple Folders
mkdir linux git networking
Create Nested Folders
mkdir -p project/docs/images

Creates:

project
└── docs
    └── images
2. touch
Command
touch file.txt
Purpose

Creates an empty file.

Example
touch notes.txt

Check:

ls

Output:

notes.txt
Create Multiple Files
touch file1.txt file2.txt file3.txt
3. echo
Command
echo "Hello Linux"
Purpose

Displays text.

Example
echo "Learning Linux"

Output:

Learning Linux
Write Text To File
echo "Linux Day 1" > notes.txt

View:

cat notes.txt

Output:

Linux Day 1
Append Text
echo "Linux is powerful" >> notes.txt

View:

cat notes.txt

Output:

Linux Day 1
Linux is powerful
Difference
>    Overwrites file

>>   Appends to file

Interview favorite.

4. cp
Command
cp source.txt destination.txt
Full Form
Copy
Purpose

Copies files.

Example
cp notes.txt backup.txt

Result:

notes.txt
backup.txt
Copy Folder
cp -r folder1 folder2
Purpose

Copies entire folder.

Example:

cp -r linux linux_backup
5. mv
Command
mv old.txt new.txt
Full Form
Move
Purpose

Moves or renames files.

Rename File
mv notes.txt linux_notes.txt

Before:

notes.txt

After:

linux_notes.txt
Move File
mv linux_notes.txt backups/
Move Folder
mv project archive/
6. rm
Command
rm file.txt
Full Form
Remove
Purpose

Deletes files.

Example
rm notes.txt
Warning
Deleted = Deleted

No recycle bin.

7. rmdir
Command
rmdir folder
Purpose

Deletes empty folders.

Example
mkdir temp

rmdir temp
Important

Works only if folder is empty.

8. rm -r
Command
rm -r folder
Purpose

Deletes folder and all contents.

Example
rm -r project
Interview Note
rm -rf folder

means:

-r = recursive

-f = force

Very powerful command.

9. file
Command
file notes.txt
Purpose

Shows file type.

Example

Output:

notes.txt: ASCII text
10. stat
Command
stat notes.txt
Purpose

Shows detailed file information.

Displays
Size
Permissions
Owner
Creation time
Modification time