# Linux Basics Commands

This section covers the fundamental Linux commands every Cloud Engineer, DevOps Engineer, and SRE should know.

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
sanjhi
```

### Used When

* Checking which account you're using
* Working on servers

---

## 2. `hostname`

### Purpose

Shows the machine/server name.

### Command

```bash
hostname
```

### Example Output

```text
ubuntu-server
```

### Used When

* Identifying servers
* SSH troubleshooting

---

## 3. `date`

### Purpose

Displays the current date and time.

### Command

```bash
date
```

### Example Output

```text
Mon Jun 8 10:30:15 IST 2026
```

### Used When

* Checking server time
* Log analysis

---

## 4. `cal`

### Purpose

Displays a calendar.

### Command

```bash
cal
```

### Example Output

```text
June 2026
```

### Used When

* Quickly viewing dates
* Basic Linux practice

---

## 5. `history`

### Purpose

Shows previously executed commands.

### Command

```bash
history
```

### Example Output

```text
1 pwd
2 ls
3 mkdir linux
```

### Used When

* Reviewing previous commands
* Recovering forgotten commands

---

## 6. `clear`

### Purpose

Clears the terminal screen.

### Command

```bash
clear
```

### Used When

* Keeping the terminal clean and readable

---

## 7. `uname`

### Purpose

Shows the operating system name.

### Command

```bash
uname
```

### Example Output

```text
Linux
```

---

## 8. `uname -a`

### Purpose

Displays detailed operating system information.

### Command

```bash
uname -a
```

### Example Output

```text
Linux ubuntu 5.15 ...
```

### Used When

* Checking Linux version
* Troubleshooting servers

---

## 9. `uptime`

### Purpose

Shows how long the system has been running.

### Command

```bash
uptime
```

### Example Output

```text
up 5 days
```

### Used When

* Monitoring server uptime

---

## 10. `id`

### Purpose

Displays user ID and group information.

### Command

```bash
id
```

### Example Output

```text
uid=1000 gid=1000 groups=1000
```

---

## 11. `groups`

### Purpose

Shows all groups the current user belongs to.

### Command

```bash
groups
```

### Example Output

```text
sudo docker users
```

---

## 12. `man`

### Purpose

Displays the manual page for a command.

### Command

```bash
man ls
```

### Examples

```bash
man pwd
man mkdir
```

### Used When

* Learning new commands
* Understanding command options

---

## 13. `echo`

### Purpose

Prints text to the terminal.

### Command

```bash
echo "Hello Linux"
```

### Example Output

```text
Hello Linux
```

---

## 14. `exit`

### Purpose

Closes the current terminal or SSH session.

### Command

```bash
exit
```

### Used When

* Disconnecting from SSH
* Leaving the terminal

---

# Quick Revision Table

| Command  | Purpose                    |
| -------- | -------------------------- |
| whoami   | Show current user          |
| hostname | Show machine name          |
| date     | Show current date and time |
| cal      | Display calendar           |
| history  | Show command history       |
| clear    | Clear terminal             |
| uname    | Show OS name               |
| uname -a | Show detailed OS info      |
| uptime   | Show system uptime         |
| id       | Show user information      |
| groups   | Show user groups           |
| man      | Open command manual        |
| echo     | Print text                 |
| exit     | Close terminal session     |
