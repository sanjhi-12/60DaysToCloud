1. ps
Command
ps
Full Form
Process Status
Purpose

Shows processes running in the current terminal session.

Example
ps

Output:

PID TTY TIME CMD
1234 pts/0 00:00:00 bash
5678 pts/0 00:00:00 ps
2. ps aux
Command
ps aux
Purpose

Shows ALL running processes.

Example
ps aux

Output:

USER PID %CPU %MEM COMMAND
root 123 0.0 1.2 nginx
ubuntu 456 0.5 2.0 python
Interview Question

How do you view all running processes?

Answer:

ps aux
3. top
Command
top
Purpose

Real-time system monitoring.

Shows:

CPU usage
Memory usage
Running processes
Example
top
Exit

Press:

q
Interview Favorite

Question:

CPU is 100%. What command will you use first?

Answer:

top
4. htop
Command
htop
Purpose

Modern version of top.

Better UI.

Colorful interface.

Note

May require installation:

sudo apt install htop
5. jobs
Command
jobs
Purpose

Shows background jobs.

Example

Start process:

sleep 100 &

Check:

jobs

Output:

[1]+ Running sleep 100 &
6. kill
Command
kill PID
Purpose

Stops a process gracefully.

Example
kill 1234

Where:

1234 = PID
7. kill -9
Command
kill -9 PID
Purpose

Forcefully stops a process.

Example
kill -9 1234
Interview Question

Difference?

kill     = graceful termination

kill -9  = force termination
8. free -m
Command
free -m
Purpose

Shows memory usage in MB.

Example

Output:

total used free
7980 2500 5480
Interview Question

How do you check memory usage?

Answer:

free -m
9. df -h
Command
df -h
Full Form
Disk Free
Purpose

Shows disk usage.

Example

Output:

Filesystem Size Used Avail
/dev/sda1 100G 45G 55G
Interview Question

Disk is full. First command?

Answer:

df -h
10. du -sh
Command
du -sh .
Full Form
Disk Usage
Purpose

Shows size of current folder.

Example
du -sh .

Output:

120M .
Check Folder Sizes
du -sh *

Very useful.

11. uptime
Command
uptime
Purpose

Shows:

How long system has been running
Load averages
Example
uptime

Output:

up 10 days
12. uname -a
Command
uname -a
Purpose

Shows:

Linux kernel
OS details
Architecture
Example
uname -a

Output:

Linux ubuntu 5.15 ...
13. lscpu
Command
lscpu
Purpose

Shows CPU information.

Example

Displays:

CPU(s)
Architecture
Model Name
14. vmstat
Command
vmstat
Purpose

Shows:

Memory
CPU
Processes

Useful for performance analysis.

15. watch
Command
watch df -h
Purpose

Runs a command repeatedly.

Example
watch free -m