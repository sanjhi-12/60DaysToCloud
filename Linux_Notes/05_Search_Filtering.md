1. find
Command
find . -name "*.txt"
Purpose

Find files and folders.

Example

Create:

touch notes.txt
touch data.txt
touch app.log

Run:

find . -name "*.txt"

Output:

./notes.txt
./data.txt
Find Log Files
find . -name "*.log"
Find Directory
find . -type d
Find File
find . -type f
2. grep
Command
grep "error" app.log
Purpose

Search text inside files.

Example

Create:

echo "server started" > app.log
echo "database connected" >> app.log
echo "error connecting db" >> app.log

Run:

grep "error" app.log

Output:

error connecting db
3. grep -i
Command
grep -i "error" app.log
Purpose

Case-insensitive search.

Example

Add:

echo "ERROR: Login Failed" >> app.log

Run:

grep -i "error" app.log

Output:

error connecting db
ERROR: Login Failed
4. grep -n
Command
grep -n "error" app.log
Purpose

Shows line numbers.

Output
3:error connecting db
5. grep -r
Command
grep -r "error" .
Purpose

Search recursively through folders.

Example

Search all files:

grep -r "database" .
6. sort
Command
sort names.txt
Purpose

Sorts data alphabetically.

Example

Create:

echo "Charlie" > names.txt
echo "Alice" >> names.txt
echo "Bob" >> names.txt

Run:

sort names.txt

Output:

Alice
Bob
Charlie
7. uniq
Command
uniq names.txt
Purpose

Removes duplicate lines.

Example
echo "Alice" > data.txt
echo "Alice" >> data.txt
echo "Bob" >> data.txt

Run:

uniq data.txt

Output:

Alice
Bob
8. sort + uniq

Very common combination.

sort data.txt | uniq
Purpose

Sort first, then remove duplicates.

9. cut
Command
cut -d "," -f1 users.csv
Purpose

Extract specific columns.

Example

Create:

echo "Rahul,22,Mumbai" > users.csv
echo "Priya,21,Pune" >> users.csv

Run:

cut -d "," -f1 users.csv

Output:

Rahul
Priya
10. tr
Command
tr a-z A-Z
Purpose

Transform characters.

Example
echo "linux" | tr a-z A-Z

Output:

LINUX
11. xargs
Command
find . -name "*.txt" | xargs ls
Purpose

Passes output of one command as input to another.

12. pipe ( | )
Command
cat app.log | grep error
Purpose

Send output of one command to another.

Example
cat names.txt | sort
13. tee
Command
echo "Hello" | tee output.txt
Purpose

Displays output and saves it to a file.