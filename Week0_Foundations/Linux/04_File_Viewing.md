# File Viewing Commands

This section covers Linux commands used to view, inspect, and monitor file contents. These commands are especially important for reading logs, troubleshooting applications, and analyzing system files.

---

## 1. `cat`

### Full Form

Concatenate

### Purpose

Displays the entire content of a file.

### Command

```bash
cat file.txt
```

### Example

Create a file:

```bash
echo "Linux Learning" > notes.txt
```

View file content:

```bash
cat notes.txt
```

### Example Output

```text
Linux Learning
```

---

### View Multiple Files

```bash
cat file1.txt file2.txt
```

Displays the contents of both files together.

---

## 2. `more`

### Purpose

Views large files page by page.

### Command

```bash
more file.txt
```

### Example

```bash
more notes.txt
```

### Controls

| Key   | Action    |
| ----- | --------- |
| Space | Next page |
| Enter | Next line |
| q     | Quit      |

### Used When

Viewing large files without opening an editor.

---

## 3. `less`

### Purpose

Advanced file viewer.

More powerful than `more` because it allows forward and backward navigation.

### Command

```bash
less file.txt
```

### Example

```bash
less notes.txt
```

### Controls

| Key       | Action        |
| --------- | ------------- |
| ↑ / ↓     | Navigate      |
| Page Down | Move forward  |
| Page Up   | Move backward |
| q         | Quit          |

### Interview Note

For large log files:

```bash
less app.log
```

is generally preferred over `cat`.

---

## 4. `head`

### Purpose

Displays the first 10 lines of a file.

### Command

```bash
head file.txt
```

### Example

Create a file:

```bash
echo "Line1" > data.txt
echo "Line2" >> data.txt
echo "Line3" >> data.txt
```

Run:

```bash
head data.txt
```

### Example Output

```text
Line1
Line2
Line3
```

---

### Show First 5 Lines

```bash
head -5 data.txt
```

---

### Used When

* Checking file headers
* Reading the beginning of log files

---

## 5. `tail`

### Purpose

Displays the last 10 lines of a file.

### Command

```bash
tail file.txt
```

### Example

```bash
tail data.txt
```

### Example Output

```text
Line1
Line2
Line3
```

---

### Show Last 5 Lines

```bash
tail -5 data.txt
```

### Used When

* Reading recent log entries
* Viewing the latest activity in a file

---

## 6. `tail -f`

### Purpose

Monitors file updates in real time.

### Command

```bash
tail -f app.log
```

### Why Important?

When applications continuously write logs:

```text
User Login
Database Connected
Request Received
```

new entries appear immediately in the terminal.

---

### DevOps / SRE Usage

```bash
tail -f nginx.log
```

One of the most commonly used troubleshooting commands.

### Used When

* Monitoring application logs
* Debugging servers
* Tracking live activity

---

## 7. `wc`

### Full Form

Word Count

### Purpose

Counts lines, words, and characters in a file.

### Command

```bash
wc file.txt
```

### Example

```bash
wc data.txt
```

### Example Output

```text
3 3 18 data.txt
```

Meaning:

```text
Lines Words Characters
```

---

### Count Lines Only

```bash
wc -l data.txt
```

---

### Count Words Only

```bash
wc -w data.txt
```

---

### Count Characters Only

```bash
wc -c data.txt
```

---

## 8. `nl`

### Purpose

Displays file contents with line numbers.

### Command

```bash
nl file.txt
```

### Example

```bash
nl notes.txt
```

### Example Output

```text
1 Linux Learning
2 Cloud Engineering
```

### Used When

* Reviewing scripts
* Referring to specific line numbers

---

## 9. `tac`

### Purpose

Displays file content in reverse order.

### Command

```bash
tac file.txt
```

### Example

File Content:

```text
Line1
Line2
Line3
```

Run:

```bash
tac file.txt
```

### Output

```text
Line3
Line2
Line1
```

---

## 10. `strings`

### Purpose

Extracts readable text from binary files.

### Command

```bash
strings file
```

### Example

```bash
strings binaryfile
```

### Used When

* Debugging applications
* Investigating binary files
* Finding readable information inside executables

---

# Quick Revision Table

| Command | Purpose                                 |
| ------- | --------------------------------------- |
| cat     | Display file content                    |
| more    | View file page by page                  |
| less    | Advanced file viewer                    |
| head    | Show first lines                        |
| tail    | Show last lines                         |
| tail -f | Live log monitoring                     |
| wc      | Count lines, words, characters          |
| nl      | Show line numbers                       |
| tac     | Reverse file content                    |
| strings | Extract readable text from binary files |

---

# Most Frequently Used Commands

```bash
cat
less
head
tail
tail -f
wc
```

These commands are heavily used in Cloud Engineering, DevOps, SRE, and System Administration for reading logs, troubleshooting applications, and monitoring systems.
