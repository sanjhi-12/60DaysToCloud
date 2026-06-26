# File Management Commands

This section covers the Linux commands used to create, copy, move, rename, and delete files and directories.

---

## 1. `mkdir`

### Full Form

Make Directory

### Purpose

Creates a new directory (folder).

### Command

```bash
mkdir foldername
```

### Example

```bash
mkdir linux
```

Check:

```bash
ls
```

Output:

```text
linux
```

---

### Create Multiple Folders

```bash
mkdir linux git networking
```

---

### Create Nested Folders

```bash
mkdir -p project/docs/images
```

Creates:

```text
project
└── docs
    └── images
```

---

## 2. `touch`

### Purpose

Creates an empty file.

### Command

```bash
touch file.txt
```

### Example

```bash
touch notes.txt
```

Check:

```bash
ls
```

Output:

```text
notes.txt
```

---

### Create Multiple Files

```bash
touch file1.txt file2.txt file3.txt
```

---

## 3. `echo`

### Purpose

Displays text and writes data into files.

### Command

```bash
echo "Hello Linux"
```

### Example

```bash
echo "Learning Linux"
```

Output:

```text
Learning Linux
```

---

### Write Text to a File

```bash
echo "Linux Day 1" > notes.txt
```

View content:

```bash
cat notes.txt
```

Output:

```text
Linux Day 1
```

---

### Append Text to a File

```bash
echo "Linux is powerful" >> notes.txt
```

View content:

```bash
cat notes.txt
```

Output:

```text
Linux Day 1
Linux is powerful
```

---

### Difference Between `>` and `>>`

| Symbol | Purpose                          |
| ------ | -------------------------------- |
| `>`    | Overwrites existing content      |
| `>>`   | Appends content to existing file |

### Interview Question

**What is the difference between `>` and `>>`?**

Answer:

```text
>  → Overwrite file

>> → Append to file
```

---

## 4. `cp`

### Full Form

Copy

### Purpose

Copies files and directories.

### Command

```bash
cp source.txt destination.txt
```

### Example

```bash
cp notes.txt backup.txt
```

Result:

```text
notes.txt
backup.txt
```

---

### Copy Entire Directory

```bash
cp -r folder1 folder2
```

### Example

```bash
cp -r linux linux_backup
```

### Note

```text
-r = Recursive
```

Required when copying directories.

---

## 5. `mv`

### Full Form

Move

### Purpose

Moves or renames files and directories.

### Command

```bash
mv old.txt new.txt
```

---

### Rename File

```bash
mv notes.txt linux_notes.txt
```

Before:

```text
notes.txt
```

After:

```text
linux_notes.txt
```

---

### Move File

```bash
mv linux_notes.txt backups/
```

---

### Move Directory

```bash
mv project archive/
```

---

## 6. `rm`

### Full Form

Remove

### Purpose

Deletes files.

### Command

```bash
rm file.txt
```

### Example

```bash
rm notes.txt
```

### Warning

```text
Deleted = Deleted
```

Linux does not move files to a recycle bin by default.

---

## 7. `rmdir`

### Purpose

Deletes empty directories.

### Command

```bash
rmdir folder
```

### Example

```bash
mkdir temp

rmdir temp
```

### Important

```text
rmdir only works on empty directories.
```

---

## 8. `rm -r`

### Purpose

Deletes directories and all contents inside them.

### Command

```bash
rm -r folder
```

### Example

```bash
rm -r project
```

---

### Dangerous Version

```bash
rm -rf folder
```

Meaning:

```text
-r = Recursive

-f = Force
```

### Interview Note

`rm -rf` is one of the most powerful and dangerous Linux commands because it deletes files and folders without confirmation.

---

## 9. `file`

### Purpose

Identifies the type of a file.

### Command

```bash
file notes.txt
```

### Example Output

```text
notes.txt: ASCII text
```

### Used When

* Identifying unknown files
* Troubleshooting file formats

---

## 10. `stat`

### Purpose

Displays detailed information about a file.

### Command

```bash
stat notes.txt
```

### Shows

* File Size
* Permissions
* Owner
* Group
* Creation Time
* Modification Time
* Access Time

### Example Output

```text
File: notes.txt
Size: 120
Access: rw-r--r--
Owner: ubuntu
Modified: 2026-06-08
```

---

# Quick Revision Table

| Command  | Purpose                      |
| -------- | ---------------------------- |
| mkdir    | Create directory             |
| mkdir -p | Create nested directories    |
| touch    | Create file                  |
| echo     | Display/write text           |
| cp       | Copy file                    |
| cp -r    | Copy directory               |
| mv       | Move or rename               |
| rm       | Delete file                  |
| rmdir    | Delete empty directory       |
| rm -r    | Delete directory recursively |
| file     | Show file type               |
| stat     | Show file details            |

---

# Most Frequently Used Commands

```bash
mkdir
touch
echo
cp
cp -r
mv
rm
rm -r
file
stat
```

These commands form the foundation of file management in Linux and are used daily by Cloud Engineers, DevOps Engineers, and System Administrators.
