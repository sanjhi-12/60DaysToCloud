# Networking Commands

This section covers Linux networking commands used for connectivity testing, DNS troubleshooting, remote access, file transfers, and network diagnostics. These commands are essential for Cloud Engineers, DevOps Engineers, SREs, and System Administrators.

---

## 1. `ping`

### Purpose

Checks connectivity between your machine and another system.

### Command

```bash
ping google.com
```

### Example Output

```text
Reply from 142.250.x.x
```

### What It Tests

```text
Network Reachability
```

### Interview Question

**How do you check if a server is reachable?**

Answer:

```bash
ping server-ip
```

---

## 2. `curl`

### Purpose

Fetches content from websites and APIs.

### Command

```bash
curl google.com
```

### Example

```bash
curl https://api.github.com
```

### Example Output

```json
{
  "current_user_url": "..."
}
```

### Why Important?

Cloud Engineers work with APIs constantly.

---

### Check Website Headers

```bash
curl -I google.com
```

### Example Output

```text
HTTP/1.1 200 OK
```

---

## 3. `wget`

### Purpose

Downloads files from the internet.

### Command

```bash
wget https://example.com/file.zip
```

### Example

```bash
wget https://example.com/index.html
```

### Difference Between `curl` and `wget`

| Command | Purpose            |
| ------- | ------------------ |
| curl    | View or fetch data |
| wget    | Download files     |

---

## 4. `ip a`

### Purpose

Displays IP addresses and network interfaces.

### Command

```bash
ip a
```

### Example Output

```text
192.168.1.10
```

### Why Important?

One of the most frequently used networking commands on Linux servers.

---

## 5. `ip route`

### Purpose

Displays the system routing table.

### Command

```bash
ip route
```

### Example Output

```text
default via 192.168.1.1
```

### Used When

* Troubleshooting connectivity
* Verifying network routes

---

## 6. `hostname -I`

### Purpose

Displays only the system's IP address.

### Command

```bash
hostname -I
```

### Example Output

```text
192.168.1.10
```

### Useful When

You need a quick IP lookup without extra details.

---

## 7. `ifconfig`

### Purpose

Displays network interface information.

### Command

```bash
ifconfig
```

### Note

This is an older networking command.

Modern Linux systems prefer:

```bash
ip a
```

---

## 8. `nslookup`

### Purpose

Checks DNS resolution.

### Command

```bash
nslookup google.com
```

### Example Output

```text
google.com
142.250.x.x
```

### Interview Question

**How do you verify DNS is working?**

Answer:

```bash
nslookup google.com
```

---

## 9. `dig`

### Full Form

```text
Domain Information Groper
```

### Purpose

Performs advanced DNS lookups.

### Command

```bash
dig google.com
```

### Example

```bash
dig openai.com
```

### Displays

```text
A Record
MX Record
TTL
DNS Server
```

### Used When

* DNS troubleshooting
* Email configuration checks
* Advanced network diagnostics

---

## 10. `netstat`

### Purpose

Displays network connections and listening ports.

### Command

```bash
netstat
```

---

### Show Listening Ports

```bash
netstat -tuln
```

### Example Output

```text
22
80
443
```

### Important Ports

| Port | Service |
| ---- | ------- |
| 22   | SSH     |
| 80   | HTTP    |
| 443  | HTTPS   |

---

## 11. `ss`

### Purpose

Modern replacement for `netstat`.

### Command

```bash
ss -tuln
```

### Interview Question

**Which command shows open ports?**

Answer:

```bash
ss -tuln
```

or

```bash
netstat -tuln
```

---

## 12. `traceroute`

### Purpose

Shows the path packets take through the network.

### Command

```bash
traceroute google.com
```

### Example

```text
Laptop
 ↓
Router
 ↓
ISP
 ↓
Google
```

### Used When

* Diagnosing slow networks
* Finding routing issues

---

## 13. `ssh`

### Full Form

```text
Secure Shell
```

### Purpose

Connects to remote Linux servers securely.

### Command

```bash
ssh user@server-ip
```

### Example

```bash
ssh ubuntu@34.100.x.x
```

### Why Important?

You will use SSH constantly when working with:

* Cloud VMs
* Linux Servers
* GCP Compute Engine
* AWS EC2
* Azure Virtual Machines

---

## 14. `ssh-keygen`

### Purpose

Generates SSH key pairs.

### Command

```bash
ssh-keygen
```

### Creates

```text
Private Key
Public Key
```

### Used For

Secure passwordless authentication.

---

## 15. `scp`

### Full Form

```text
Secure Copy
```

### Purpose

Transfers files securely between systems.

### Command

```bash
scp file.txt user@server:/home/ubuntu
```

### Example

```bash
scp app.py ubuntu@34.x.x.x:/home/ubuntu
```

### Used When

* Uploading code to servers
* Copying logs
* Transferring configuration files

---

## 16. `telnet`

### Purpose

Tests whether a port is reachable.

### Command

```bash
telnet google.com 80
```

### Used When

Checking if services are listening on a specific port.

---

## 17. `nmap`

### Purpose

Scans open ports and services.

### Command

```bash
nmap localhost
```

### Example Output

```text
22/tcp open ssh
80/tcp open http
```

### Used When

* Security testing
* Network discovery
* Troubleshooting services

---

# Quick Revision Table

| Command     | Purpose                    |
| ----------- | -------------------------- |
| ping        | Check connectivity         |
| curl        | Fetch website/API data     |
| wget        | Download files             |
| ip a        | Show IP addresses          |
| ip route    | Show routing table         |
| hostname -I | Show system IP             |
| ifconfig    | Show network interfaces    |
| nslookup    | Check DNS                  |
| dig         | Advanced DNS lookup        |
| netstat     | View connections and ports |
| ss          | Modern network statistics  |
| traceroute  | Trace packet path          |
| ssh         | Connect to remote servers  |
| ssh-keygen  | Generate SSH keys          |
| scp         | Secure file transfer       |
| telnet      | Test port connectivity     |
| nmap        | Scan ports and services    |

---

# Most Frequently Used Commands

```bash
ping
curl
ip a
hostname -I
nslookup
dig
ss -tuln
ssh
ssh-keygen
scp
```

These commands are used daily in Cloud Engineering, DevOps, SRE, and Infrastructure roles.

---

# Interview Questions

### Q1. Difference between `ping` and `curl`?

**Answer**

```text
ping → Tests network connectivity

curl → Fetches HTTP/API data
```

---

### Q2. Difference between `curl` and `wget`?

**Answer**

```text
curl → View or fetch data

wget → Download files
```

---

### Q3. How do you check your IP address?

**Answer**

```bash
ip a
```

or

```bash
hostname -I
```

---

### Q4. How do you verify DNS resolution?

**Answer**

```bash
nslookup google.com
```

or

```bash
dig google.com
```

---

### Q5. Which command is used to connect to a remote Linux server?

**Answer**

```bash
ssh user@server-ip
```
