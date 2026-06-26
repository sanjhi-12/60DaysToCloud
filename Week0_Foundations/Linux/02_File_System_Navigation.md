# File System Navigation Commands

This section covers the Linux commands used to navigate through directories and explore the file system.

---

## 1. `pwd`

### Full Form

Print Working Directory

### Purpose

Shows your current location in the file system.

### Command

```bash
pwd
```

### Example Output

```text
/home/ubuntu
```

### Real-Life Analogy

Like asking:

> "Which room am I currently standing in?"

---

## 2. `ls`

### Purpose

Lists files and folders in the current directory.

### Command

```bash
ls
```

### Example Output

```text
notes.txt
linux
project
```

### Used When

* Viewing files in a folder
* Checking directory contents

---

## 3. `ls -l`

### Purpose

Displays detailed information about files and folders.

### Command

```bash
ls -l
```

### Displays

* Permissions
* Owner
* Size
* Date Modified
* File Name

### Example Output

```text
-rw-r--r-- 1 user user 120 notes.txt
```

---

## 4. `ls -a`

### Purpose

Shows hidden files and directories.

### Command

```bash
ls -a
```

### Example Output

```text
.
..
.git
.vscode
```

### Important Note

Git repositories contain a hidden folder:

```text
.git
```

This folder stores all Git history and configuration.

---

## 5. `ls -la`

### Purpose

Shows:

* Hidden files
* Detailed file information

### Command

```bash
ls -la
```

### Why Use It?

This is one of the most commonly used Linux commands because it combines:

```text
ls -a + ls -l
```

---

## 6. `cd`

### Full Form

Change Directory

### Purpose

Moves into another directory.

### Command

```bash
cd foldername
```

### Example

```bash
cd linux
```

---

## 7. `cd ..`

### Purpose

Moves one directory level up.

### Command

```bash
cd ..
```

### Example

Current Location:

```text
/home/ubuntu/linux
```

Run:

```bash
cd ..
```

Result:

```text
/home/ubuntu
```

---

## 8. `cd ~`

### Purpose

Moves directly to the home directory.

### Command

```bash
cd ~
```

### Example Output

```text
/home/ubuntu
```

### Why Important?

Useful when you're deep inside multiple directories and want to quickly return home.

---

## 9. `cd /`

### Purpose

Moves to the root directory.

### Command

```bash
cd /
```

### Example Output

```text
/
```

### Important Note

The root directory is the top-most directory in Linux.

All other folders exist under it.

---

## 10. `tree`

### Purpose

Displays the folder structure visually.

### Command

```bash
tree
```

### Example Output

```text
project
├── linux
├── git
└── networking
```

### Used When

* Understanding project structure
* Visualizing directories

### Note

May need installation:

```bash
sudo apt install tree
```

---

## 11. `find`

### Purpose

Searches for files and folders.

### Command

```bash
find . -name "*.txt"
```

### Example

```bash
find . -name "*.md"
```

### Example Output

```text
Linux_Notes.md
Git_Notes.md
```

### Why Important?

One of the most powerful Linux commands for locating files.

---

## 12. `locate`

### Purpose

Quickly searches for files using a database index.

### Command

```bash
locate notes.txt
```

### Example Output

```text
/home/ubuntu/notes.txt
```

### Advantage

Much faster than `find`.

### Note

May not be installed on all systems.

Install:

```bash
sudo apt install mlocate
```

Update database:

```bash
sudo updatedb
```

---

# Quick Revision Table

| Command | Purpose                   |
| ------- | ------------------------- |
| pwd     | Show current directory    |
| ls      | List files and folders    |
| ls -l   | Detailed file information |
| ls -a   | Show hidden files         |
| ls -la  | Detailed + hidden files   |
| cd      | Change directory          |
| cd ..   | Move one level up         |
| cd ~    | Go to home directory      |
| cd /    | Go to root directory      |
| tree    | Show folder structure     |
| find    | Search files and folders  |
| locate  | Fast file search          |

---

# Most Frequently Used Commands

```bash
pwd
ls
ls -la
cd
cd ..
cd ~
find
tree
```

These commands form the foundation of Linux navigation and are used daily by Cloud Engineers, DevOps Engineers, and SREs.
