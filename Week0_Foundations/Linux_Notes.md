# Linux Commands Learned - Day 1

## Navigation Commands

### pwd

Print Working Directory.
Shows current location in the file system.

### ls

Lists files and directories.

### ls -l

Shows detailed information:

* Permissions
* Owner
* Size
* Date

### cd

Changes directory.

### cd ..

Moves one level up.

## File & Directory Commands

### mkdir

Creates directories.

### touch

Creates empty files.

### cp

Copies files.

### mv

Moves or renames files.

### rm

Deletes files.

### rmdir

Deletes empty directories.

## File Content Commands

### cat

Displays file content.

### echo

Prints text or writes text into files.

### more

Displays file content page by page.

## Utility Commands

### history

Shows previously executed commands.

### clear

Clears terminal screen.

### tree

Displays folder structure in tree format.

### whoami

Displays current user.

### hostname

Displays machine name.

### date

Displays current date and time.

### ping

Checks network connectivity.

# Additional Linux Commands Learned

## rm

Deletes a file.

Example:

rm test.txt

Use carefully because deleted files are not moved to a recycle bin.

---

## rmdir

Deletes an empty directory.

Example:

rmdir temp

Only works if the directory is empty.

---

## head

Displays the first 10 lines of a file.

Example:

head notes.txt

Useful for checking the beginning of large files.

---

## tail

Displays the last 10 lines of a file.

Example:

tail notes.txt

Useful for checking recent entries in logs.

---

## tail -f

Displays live updates to a file.

Example:

tail -f app.log

Commonly used by DevOps and SRE engineers for monitoring logs.

---

## wc

Word Count command.

Example:

wc notes.txt

Displays:

* Number of lines
* Number of words
* Number of characters

---

## find

Searches for files and directories.

Examples:

find . -name "*.txt"

find . -name "*.log"

Useful for locating files on a system.

---

## grep

Searches for text inside files.

Example:

grep "error" app.log

Useful for finding errors, warnings, and specific information in logs.

---

## grep -i

Case-insensitive search.

Example:

grep -i "error" app.log

Matches:
error
ERROR
Error

---

## grep -n

Displays matching lines along with line numbers.

Example:

grep -n "database" app.log

---

# Linux Permissions

Linux permissions determine who can access files and directories.

Permission Types:

r = Read
w = Write
x = Execute

Example:

-rwxr-xr-x

Breakdown:

Owner  = rwx
Group  = r-x
Others = r-x

---

## chmod

Changes file permissions.

Make file executable:

chmod +x script.sh

Set permissions numerically:

chmod 755 script.sh

Meaning:

7 = rwx
5 = r-x
5 = r-x

---

## chmod 644

Common permission setting for files.

chmod 644 file.txt

Meaning:

Owner  = rw-
Group  = r--
Others = r--

---

## chown

Changes ownership of files and directories.

Example:

sudo chown user file.txt

Difference:

chmod = changes permissions

chown = changes owner
