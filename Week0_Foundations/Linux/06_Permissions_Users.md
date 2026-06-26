# Permissions & Users Commands

This section covers Linux user management, groups, file permissions, ownership, and privilege escalation. These concepts are critical for Cloud Engineers, DevOps Engineers, SREs, and System Administrators.

---

## 1. `whoami`

### Purpose

Shows the currently logged-in user.

### Command

```bash
whoami
```

### Example Output

```text
ubuntu
```

or

```text
sanjhi
```

### Interview Question

**How do you check which user you're currently using?**

Answer:

```bash
whoami
```

---

## 2. `id`

### Purpose

Displays detailed user information.

### Command

```bash
id
```

### Example Output

```text
uid=1000(ubuntu)
gid=1000(ubuntu)
groups=1000(ubuntu)
```

### Explanation

| Term   | Meaning                    |
| ------ | -------------------------- |
| uid    | User ID                    |
| gid    | Group ID                   |
| groups | Groups the user belongs to |

### Used When

* Checking user permissions
* Troubleshooting access issues

---

## 3. `groups`

### Purpose

Shows all groups the current user belongs to.

### Command

```bash
groups
```

### Example Output

```text
ubuntu sudo docker
```

### Why Important?

Many Linux permissions are controlled through groups.

Example:

```text
docker
```

Users in the Docker group can run Docker commands without using `sudo`.

---

## 4. `ls -l`

### Purpose

Displays file permissions.

### Command

```bash
ls -l
```

### Example Output

```text
-rwxr-xr-x 1 user user 100 file.txt
```

---

### Permission Breakdown

```text
-rwxr-xr-x
```

Meaning:

```text
Owner   Group   Others

rwx     r-x     r-x
```

---

### Permission Meanings

| Symbol | Meaning |
| ------ | ------- |
| r      | Read    |
| w      | Write   |
| x      | Execute |

---

## 5. `chmod`

### Purpose

Changes file permissions.

### Command

```bash
chmod permissions file
```

---

### Example 1: Make File Executable

```bash
chmod +x script.sh
```

Before:

```text
-rw-r--r--
```

After:

```text
-rwxr-xr-x
```

---

### Example 2

```bash
chmod 755 script.sh
```

Meaning:

```text
Owner  = 7 = rwx

Group  = 5 = r-x

Others = 5 = r-x
```

---

### Example 3

```bash
chmod 644 notes.txt
```

Meaning:

```text
Owner  = rw-

Group  = r--

Others = r--
```

Very common permission setting for files.

---

## Understanding Permission Numbers

### Read

```text
r = 4
```

### Write

```text
w = 2
```

### Execute

```text
x = 1
```

---

### Common Values

| Number | Permission |
| ------ | ---------- |
| 7      | rwx        |
| 6      | rw-        |
| 5      | r-x        |
| 4      | r--        |

---

### Interview Question

**What does `chmod 755 script.sh` mean?**

Answer:

```text
Owner  : rwx

Group  : r-x

Others : r-x
```

---

## 6. `chown`

### Purpose

Changes ownership of a file or directory.

### Command

```bash
sudo chown user file.txt
```

### Example

```bash
sudo chown ubuntu notes.txt
```

Now:

```text
ubuntu
```

owns the file.

---

### Difference Between `chmod` and `chown`

| Command | Purpose             |
| ------- | ------------------- |
| chmod   | Changes permissions |
| chown   | Changes ownership   |

### Interview Favorite

Many interviewers ask this distinction.

---

## 7. `chgrp`

### Purpose

Changes group ownership.

### Command

```bash
sudo chgrp developers file.txt
```

### Example

```bash
sudo chgrp docker script.sh
```

---

## 8. `sudo`

### Full Form

```text
Super User Do
```

### Purpose

Runs commands with administrator privileges.

### Command

```bash
sudo command
```

### Example

```bash
sudo apt update
```

### Why Important?

Normal users cannot perform system-level operations.

---

## 9. `passwd`

### Purpose

Changes the current user's password.

### Command

```bash
passwd
```

### Example

```bash
passwd
```

Prompts:

```text
Current Password

New Password

Confirm Password
```

---

## 10. `su`

### Full Form

```text
Switch User
```

### Purpose

Switches to another user account.

### Command

```bash
su username
```

### Example

```bash
su root
```

Switches to the root account.

---

## 11. `umask`

### Purpose

Shows the default permissions assigned to newly created files and directories.

### Command

```bash
umask
```

### Example Output

```text
0022
```

### Why Important?

Determines default permission settings for new files.

---

# Quick Revision Table

| Command | Purpose                  |
| ------- | ------------------------ |
| whoami  | Show current user        |
| id      | Show user details        |
| groups  | Show user groups         |
| ls -l   | View permissions         |
| chmod   | Change permissions       |
| chown   | Change ownership         |
| chgrp   | Change group ownership   |
| sudo    | Run as administrator     |
| passwd  | Change password          |
| su      | Switch user              |
| umask   | View default permissions |

---

# Most Frequently Used Commands

```bash
whoami
id
groups
ls -l
chmod
chmod 755
chmod 644
chmod +x
chown
sudo
passwd
su
```

These commands form the foundation of Linux security, access control, and user management.

---

# Interview Questions

### Q1. Difference between `chmod` and `chown`?

**Answer**

```text
chmod → Changes permissions

chown → Changes ownership
```

---

### Q2. What does `chmod 755` mean?

**Answer**

```text
Owner  : rwx

Group  : r-x

Others : r-x
```

---

### Q3. What does `sudo` do?

**Answer**

```text
Runs commands with administrator privileges.
```

---

### Q4. What do `r`, `w`, and `x` mean?

**Answer**

```text
r = Read

w = Write

x = Execute
```
