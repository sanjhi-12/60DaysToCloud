1. cat
Command
cat file.txt
Full Form
Concatenate
Purpose

Displays the entire content of a file.

Example

Create file:

echo "Linux Learning" > notes.txt

View:

cat notes.txt

Output:

Linux Learning
Multiple Files
cat file1.txt file2.txt

Displays both files together.

2. more
Command
more file.txt
Purpose

Views large files page by page.

Example
more notes.txt
Controls
Space → Next page

Enter → Next line

q → Quit
3. less
Command
less file.txt
Purpose

Advanced file viewer.

More powerful than more.

Example
less notes.txt
Controls
Arrow Keys → Navigate

/Page Down → Forward

Page Up → Backward

q → Quit
Interview Note

For large logs:

less app.log

is preferred.

4. head
Command
head file.txt
Purpose

Shows first 10 lines.

Example

Create:

echo "Line1" > data.txt
echo "Line2" >> data.txt
echo "Line3" >> data.txt

Run:

head data.txt

Output:

Line1
Line2
Line3
First 5 Lines
head -5 data.txt
5. tail
Command
tail file.txt
Purpose

Shows last 10 lines.

Example
tail data.txt

Output:

Line1
Line2
Line3
Last 5 Lines
tail -5 data.txt
6. tail -f
Command
tail -f app.log
Purpose

Live log monitoring.

Why Important?

When applications generate logs continuously:

User Login
Database Connected
Request Received

you can watch them in real time.

DevOps/SRE Use
tail -f nginx.log

One of the most commonly used troubleshooting commands.

7. wc
Command
wc file.txt
Full Form
Word Count
Purpose

Counts:

Lines
Words
Characters
Example
wc data.txt

Output:

3 3 18 data.txt

Meaning:

Lines Words Characters
Count Lines Only
wc -l data.txt
Count Words Only
wc -w data.txt
Count Characters Only
wc -c data.txt
8. nl
Command
nl file.txt
Purpose

Shows line numbers.

Example
nl notes.txt

Output:

1 Linux Learning
2 Cloud Engineering
9. tac
Command
tac file.txt
Purpose

Displays file content in reverse order.

Example

File:

Line1
Line2
Line3

Output:

Line3
Line2
Line1
10. strings
Command
strings file
Purpose

Extracts readable text from binary files.

Used occasionally for debugging.