1. whoami
Command
whoami
Purpose

Shows the currently logged-in user.

Example

Output:

ubuntu

or

sanjhi
Interview Question

How do you check which user you're currently using?

Answer:

whoami
2. id
Command
id
Purpose

Shows detailed user information.

Example

Output:

uid=1000(ubuntu)
gid=1000(ubuntu)
groups=1000(ubuntu)
Explanation
uid = User ID

gid = Group ID

groups = Groups user belongs to
3. groups
Command
groups
Purpose

Shows all groups of the current user.

Example

Output:

ubuntu sudo docker
Why Important?

Many permissions are controlled through groups.

Example:

docker group

lets you run Docker without sudo.

4. ls -l
Command
ls -l
Purpose

Shows file permissions.

Example
-rwxr-xr-x 1 user user 100 file.txt
Breakdown
-rwxr-xr-x

means:

Owner   Group   Others

rwx     r-x     r-x
Permission Meaning
r = Read

w = Write

x = Execute
5. chmod
Command
chmod permissions file
Purpose

Changes permissions.

Example 1

Make executable:

chmod +x script.sh

Before:

-rw-r--r--

After:

-rwxr-xr-x
Example 2
chmod 755 script.sh
Meaning
Owner  = 7 = rwx

Group  = 5 = r-x

Others = 5 = r-x
Example 3
chmod 644 notes.txt
Meaning
Owner  = rw-

Group  = r--

Others = r--

Very common for files.

Understanding Numbers
Read
r = 4
Write
w = 2
Execute
x = 1
Examples
7
4 + 2 + 1

rwx
6
4 + 2

rw-
5
4 + 1

r-x
4
4

r--
Interview Question

What does:

chmod 755 script.sh

mean?

Answer:

Owner  : rwx

Group  : r-x

Others : r-x
6. chown
Command
sudo chown user file.txt
Purpose

Changes owner of a file.

Example
sudo chown ubuntu notes.txt

Now:

ubuntu

owns the file.

Difference
chmod
Changes permissions
chown
Changes ownership

Interview favorite.

7. chgrp
Command
sudo chgrp developers file.txt
Purpose

Changes group ownership.

Example
sudo chgrp docker script.sh
8. sudo
Command
sudo command
Full Form
Super User Do
Purpose

Run command as administrator.

Example
sudo apt update
Why Important?

Normal users cannot perform system-level tasks.

9. passwd
Command
passwd
Purpose

Change current user's password.

Example
passwd

Prompts:

Current Password

New Password

Confirm Password
10. su
Command
su username
Full Form
Switch User
Purpose

Switch to another account.

Example
su root

Switches to root user.

11. umask
Command
umask
Purpose

Shows default permissions for newly created files.

Example

Output:

0022