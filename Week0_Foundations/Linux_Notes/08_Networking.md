1. ping
Command
ping google.com
Purpose

Checks connectivity between your machine and another system.

Example Output
Reply from 142.250.x.x
What It Tests
Network Reachability
Interview Question

How do you check if a server is reachable?

Answer:

ping server-ip
2. curl
Command
curl google.com
Purpose

Fetches content from a website/API.

Example
curl https://api.github.com

Output:

{
 "current_user_url": ...
}
Why Important?

Cloud Engineers use APIs constantly.

Check Website Headers
curl -I google.com

Output:

HTTP/1.1 200 OK
3. wget
Command
wget https://example.com/file.zip
Purpose

Downloads files.

Example
wget https://example.com/index.html
Difference
curl → View data

wget → Download data
4. ip a
Command
ip a
Purpose

Shows IP addresses.

Example Output
192.168.1.10
Why Important?

Used constantly on Linux servers.

5. ip route
Command
ip route
Purpose

Shows routing table.

Example Output
default via 192.168.1.1
6. hostname -I
Command
hostname -I
Purpose

Shows system IP address only.

Example
192.168.1.10
7. ifconfig
Command
ifconfig
Purpose

Shows network interface information.

Note

Older command.

Modern Linux prefers:

ip a
8. nslookup
Command
nslookup google.com
Purpose

Checks DNS resolution.

Example Output
google.com
142.250.x.x
Interview Question

How do you verify DNS is working?

Answer:

nslookup google.com
9. dig
Command
dig google.com
Full Form
Domain Information Groper
Purpose

Advanced DNS lookup.

Example
dig openai.com

Displays:

A Record
MX Record
TTL
DNS Server
10. netstat
Command
netstat
Purpose

Shows network connections.

Show Listening Ports
netstat -tuln
Output
80
443
22
Important Ports
22   SSH

80   HTTP

443  HTTPS
11. ss
Command
ss -tuln
Purpose

Modern replacement for netstat.

Interview Question

Which command shows open ports?

Answer:

ss -tuln

or

netstat -tuln
12. traceroute
Command
traceroute google.com
Purpose

Shows path packets take.

Example
Laptop
↓
Router
↓
ISP
↓
Google
13. ssh
Command
ssh user@server-ip
Full Form
Secure Shell
Purpose

Connect to remote servers.

Example
ssh ubuntu@34.100.x.x
Week 2 Command

You'll use this every day when working with VMs.

14. ssh-keygen
Command
ssh-keygen
Purpose

Creates SSH key pair.

Generates
Private Key
Public Key

Used for secure authentication.

15. scp
Command
scp file.txt user@server:/home/ubuntu
Full Form
Secure Copy
Purpose

Transfer files between systems.

Example
scp app.py ubuntu@34.x.x.x:/home/ubuntu
16. telnet
Command
telnet google.com 80
Purpose

Check if a port is reachable.

17. nmap
Command
nmap localhost
Purpose

Port scanning.

Example Output
22/tcp open ssh
80/tcp open http