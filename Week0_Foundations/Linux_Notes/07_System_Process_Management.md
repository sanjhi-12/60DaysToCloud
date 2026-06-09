# System Information & Process Management Commands

This section covers Linux commands used to monitor processes, analyze system performance, troubleshoot servers, and manage resources. These commands are heavily used by Cloud Engineers, DevOps Engineers, SREs, and System Administrators.

---

## 1. `ps`

### Full Form

Process Status

### Purpose

Shows processes running in the current terminal session.

### Command

```bash
ps
```

### Example Output

```text
PID TTY          TIME CMD
1234 pts/0   00:00:00 bash
5678 pts/0   00:00:00 ps
```

### Used When

* Checking active processes
* Debugging terminal sessions

---

## 2. `ps aux`

### Purpose

Displays all running processes on the system.

### Command

```bash
ps aux
```

### Example Output

```text
USER    PID %CPU %MEM COMMAND
root    123 0.0  1.2 nginx
ubuntu  456 0.5  2.0 python
```

### Interview Question

**How do you view all running processes?**

Answer:

```bash
ps aux
```

---

## 3. `top`

### Purpose

Provides real-time system monitoring.

### Displays

* CPU Usage
* Memory Usage
* Running Processes
* System Load

### Command

```bash
top
```

### Exit

Press:

```text
q
```

### Interview Favorite

**Question:**

```text
CPU usage is 100%. What command will you use first?
```

**Answer:**

```bash
top
```

---

## 4. `htop`

### Purpose

Modern version of `top`.

### Benefits

* Better user interface
* Easier navigation
* Color-coded resource usage

### Command

```bash
htop
```

### Installation

```bash
sudo apt install htop
```

### Used When

* Monitoring servers
* Identifying resource-heavy processes

---

## 5. `jobs`

### Purpose

Shows background jobs running in the current shell.

### Command

```bash
jobs
```

### Example

Start a background process:

```bash
sleep 100 &
```

Check jobs:

```bash
jobs
```

### Output

```text
[1]+ Running sleep 100 &
```

---

## 6. `kill`

### Purpose

Stops a process gracefully.

### Command

```bash
kill PID
```

### Example

```bash
kill 1234
```

Where:

```text
1234 = Process ID (PID)
```

### Used When

* Stopping applications
* Ending stuck processes

---

## 7. `kill -9`

### Purpose

Forcefully terminates a process.

### Command

```bash
kill -9 PID
```

### Example

```bash
kill -9 1234
```

### Interview Question

**Difference between `kill` and `kill -9`?**

Answer:

```text
kill     → Graceful termination

kill -9  → Force termination
```

---

## 8. `free -m`

### Purpose

Displays memory usage in megabytes (MB).

### Command

```bash
free -m
```

### Example Output

```text
total used free
7980  2500 5480
```

### Interview Question

**How do you check memory usage?**

Answer:

```bash
free -m
```

---

## 9. `df -h`

### Full Form

Disk Free

### Purpose

Shows disk space usage.

### Command

```bash
df -h
```

### Example Output

```text
Filesystem Size Used Avail
/dev/sda1 100G 45G 55G
```

### Interview Question

**Disk is full. What command should you run first?**

Answer:

```bash
df -h
```

---

## 10. `du -sh`

### Full Form

Disk Usage

### Purpose

Displays the size of a directory.

### Command

```bash
du -sh .
```

### Example Output

```text
120M .
```

---

### Check Sizes of All Folders

```bash
du -sh *
```

Very useful for locating large folders.

---

## 11. `uptime`

### Purpose

Shows:

* System uptime
* Number of logged-in users
* Load averages

### Command

```bash
uptime
```

### Example Output

```text
up 10 days
```

### Used When

* Monitoring server health
* Checking system stability

---

## 12. `uname -a`

### Purpose

Displays detailed operating system information.

### Command

```bash
uname -a
```

### Shows

* Linux Kernel Version
* OS Information
* Architecture

### Example Output

```text
Linux ubuntu 5.15 ...
```

---

## 13. `lscpu`

### Purpose

Displays CPU information.

### Command

```bash
lscpu
```

### Shows

```text
CPU(s)
Architecture
Model Name
CPU MHz
Threads
Cores
```

### Used When

* Checking server specifications
* Capacity planning

---

## 14. `vmstat`

### Purpose

Displays system performance statistics.

### Command

```bash
vmstat
```

### Shows

* CPU Usage
* Memory Usage
* Running Processes
* Disk Activity

### Used When

* Performance analysis
* Troubleshooting slow servers

---

## 15. `watch`

### Purpose

Runs a command repeatedly at fixed intervals.

### Command

```bash
watch df -h
```

### Example

```bash
watch free -m
```

### Why Useful?

Instead of manually rerunning commands, Linux refreshes the output automatically.

---

# Troubleshooting Scenarios

## Server Running Slowly

```bash
top
```

---

## High Memory Usage

```bash
free -m
```

---

## Disk Full

```bash
df -h
```

Then:

```bash
du -sh *
```

---

## Application Hung

Find Process:

```bash
ps aux
```

Stop Process:

```bash
kill PID
```

Force Stop:

```bash
kill -9 PID
```

---

# Quick Revision Table

| Command  | Purpose                        |
| -------- | ------------------------------ |
| ps       | View current session processes |
| ps aux   | View all processes             |
| top      | Real-time monitoring           |
| htop     | Advanced monitoring            |
| jobs     | View background jobs           |
| kill     | Gracefully stop process        |
| kill -9  | Force stop process             |
| free -m  | Check memory usage             |
| df -h    | Check disk usage               |
| du -sh   | Check folder size              |
| uptime   | View system uptime             |
| uname -a | View OS information            |
| lscpu    | View CPU details               |
| vmstat   | Performance statistics         |
| watch    | Repeat command automatically   |

---

# Most Frequently Used Commands

```bash
ps aux
top
kill
kill -9
free -m
df -h
du -sh
uptime
uname -a
lscpu
```

These commands are among the most frequently used in Cloud Engineering, DevOps, SRE, and Linux administration.

---

# Interview Questions

### Q1. Difference between `ps` and `top`?

**Answer**

```text
ps → Snapshot of processes

top → Real-time process monitoring
```

---

### Q2. How do you check memory usage?

**Answer**

```bash
free -m
```

---

### Q3. How do you check disk usage?

**Answer**

```bash
df -h
```

---

### Q4. Difference between `kill` and `kill -9`?

**Answer**

```text
kill     → Graceful termination

kill -9  → Force termination
```

---

### Q5. Which command shows CPU information?

**Answer**

```bash
lscpu
```
