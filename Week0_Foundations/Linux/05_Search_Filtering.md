# Search & Filtering Commands

This section covers Linux commands used to search files, filter data, process text, and analyze logs. These commands are heavily used in Cloud Engineering, DevOps, SRE, and System Administration.

---

## 1. `find`

### Purpose

Searches for files and directories.

### Command

```bash
find . -name "*.txt"
```

### Example

Create files:

```bash
touch notes.txt
touch data.txt
touch app.log
```

Run:

```bash
find . -name "*.txt"
```

### Example Output

```text
./notes.txt
./data.txt
```

---

### Find Log Files

```bash
find . -name "*.log"
```

---

### Find Directories

```bash
find . -type d
```

---

### Find Files

```bash
find . -type f
```

---

## 2. `grep`

### Purpose

Searches for text inside files.

### Command

```bash
grep "error" app.log
```

### Example

Create log file:

```bash
echo "server started" > app.log
echo "database connected" >> app.log
echo "error connecting db" >> app.log
```

Run:

```bash
grep "error" app.log
```

### Output

```text
error connecting db
```

### Used When

* Searching logs
* Finding errors
* Troubleshooting applications

---

## 3. `grep -i`

### Purpose

Performs case-insensitive searches.

### Command

```bash
grep -i "error" app.log
```

### Example

Add:

```bash
echo "ERROR: Login Failed" >> app.log
```

Run:

```bash
grep -i "error" app.log
```

### Output

```text
error connecting db
ERROR: Login Failed
```

---

## 4. `grep -n`

### Purpose

Displays matching lines with line numbers.

### Command

```bash
grep -n "error" app.log
```

### Output

```text
3:error connecting db
```

### Used When

* Debugging scripts
* Finding exact line locations

---

## 5. `grep -r`

### Purpose

Searches recursively through folders and subfolders.

### Command

```bash
grep -r "error" .
```

### Example

```bash
grep -r "database" .
```

Searches every file inside the current directory tree.

---

## 6. `sort`

### Purpose

Sorts text alphabetically or numerically.

### Command

```bash
sort names.txt
```

### Example

Create:

```bash
echo "Charlie" > names.txt
echo "Alice" >> names.txt
echo "Bob" >> names.txt
```

Run:

```bash
sort names.txt
```

### Output

```text
Alice
Bob
Charlie
```

---

## 7. `uniq`

### Purpose

Removes duplicate lines.

### Command

```bash
uniq names.txt
```

### Example

```bash
echo "Alice" > data.txt
echo "Alice" >> data.txt
echo "Bob" >> data.txt
```

Run:

```bash
uniq data.txt
```

### Output

```text
Alice
Bob
```

### Note

`uniq` works best on sorted data.

---

## 8. `sort | uniq`

### Purpose

Sorts data and removes duplicates.

### Command

```bash
sort data.txt | uniq
```

### Why Important?

A common Linux pattern for cleaning data.

### Example

```text
Alice
Alice
Bob
Charlie
Charlie
```

Output:

```text
Alice
Bob
Charlie
```

---

## 9. `cut`

### Purpose

Extracts specific columns from structured data.

### Command

```bash
cut -d "," -f1 users.csv
```

### Example

Create:

```bash
echo "Rahul,22,Mumbai" > users.csv
echo "Priya,21,Pune" >> users.csv
```

Run:

```bash
cut -d "," -f1 users.csv
```

### Output

```text
Rahul
Priya
```

### Explanation

```text
-d = delimiter
-f = field
```

---

## 10. `tr`

### Purpose

Transforms characters.

### Command

```bash
tr a-z A-Z
```

### Example

```bash
echo "linux" | tr a-z A-Z
```

### Output

```text
LINUX
```

### Used When

* Converting case
* Text processing

---

## 11. `xargs`

### Purpose

Passes output from one command as input to another command.

### Command

```bash
find . -name "*.txt" | xargs ls
```

### Example

Find all text files and list them.

### Why Important?

Useful when combining commands in automation scripts.

---

## 12. Pipe (`|`)

### Purpose

Sends output from one command directly into another command.

### Example

```bash
cat app.log | grep error
```

### Another Example

```bash
cat names.txt | sort
```

### Explanation

```text
Command 1 Output
          ↓
      Pipe (|)
          ↓
Command 2 Input
```

### One of the most important Linux concepts.

---

## 13. `tee`

### Purpose

Displays output on the screen and saves it to a file.

### Command

```bash
echo "Hello" | tee output.txt
```

### Example Output

```text
Hello
```

Also creates:

```text
output.txt
```

containing:

```text
Hello
```

### Used When

* Logging command output
* Saving results while viewing them

---

# Quick Revision Table

| Command | Purpose                      |
| ------- | ---------------------------- |
| find    | Search files and folders     |
| grep    | Search text                  |
| grep -i | Case-insensitive search      |
| grep -n | Show line numbers            |
| grep -r | Recursive search             |
| sort    | Sort data                    |
| uniq    | Remove duplicates            |
| cut     | Extract columns              |
| tr      | Transform text               |
| xargs   | Pass output as arguments     |
| |       | Pipe output between commands |
| tee     | Display and save output      |

---

# Most Frequently Used Commands

```bash
find
grep
grep -i
grep -n
grep -r
sort
cut
tr
tee
```

These commands form the foundation of Linux troubleshooting, log analysis, automation, and DevOps workflows.

---

# Interview Questions

### Q1. Difference between `find` and `grep`?

**Answer**

```text
find → Searches files and directories

grep → Searches text inside files
```

---

### Q2. What does `grep -i` do?

**Answer**

```text
Performs a case-insensitive search.
```

---

### Q3. What does the pipe (`|`) operator do?

**Answer**

```text
Passes output of one command as input to another command.
```

---

### Q4. Why use `tee`?

**Answer**

```text
Displays output and saves it to a file at the same time.
```
