# 02 Git Basics

## What is Git?

Git is a Distributed Version Control System (DVCS) used to track changes made to files and manage project history efficiently. It allows developers to collaborate, maintain different versions of projects, recover previous versions, and work independently through branching and merging. Git was created by Linus Torvalds in 2005 for managing Linux kernel development.

---

## Features of Git

Git provides several powerful features including distributed architecture, speed, lightweight operation, branching support, merging capabilities, complete history tracking, and efficient collaboration. These features make Git the most widely used Version Control System in the software industry.

### Major Features

* Distributed Architecture
* High Speed
* Lightweight
* Complete History Tracking
* Branching and Merging
* Collaboration Support
* Open Source

---

## Git vs GitHub

Git is a Version Control System that works locally on a computer and tracks changes in files. GitHub is a cloud platform used to store Git repositories online and facilitate collaboration among developers. Git can function without GitHub, but GitHub relies on Git repositories.

| Git                       | GitHub              |
| ------------------------- | ------------------- |
| Version Control System    | Cloud Platform      |
| Works Locally             | Works Online        |
| Tracks Changes            | Stores Repositories |
| Created by Linus Torvalds | Owned by Microsoft  |
| Can Work Offline          | Requires Internet   |

---

## What is a Repository?

A repository is a project folder managed by Git. It contains project files, commit history, branches, and configuration information. Repositories can be local or remote.

Example:

```text
Cloud-App
│
├── app.py
├── README.md
├── requirements.txt
└── .git
```

---

## Types of Repositories

### Local Repository

A Local Repository exists on the developer's computer and allows work to continue even without internet connectivity.

### Remote Repository

A Remote Repository is hosted on services like GitHub and enables collaboration and backup.

---

## What is the .git Folder?

The `.git` folder is a hidden directory created when a repository is initialized using Git. It stores commit history, branches, references, logs, and configuration files. Without this folder, Git cannot track changes or maintain version history.

---

## Git Configuration

Git configuration stores information such as username and email address. This information is attached to every commit and helps identify the author of changes.

---

## Local vs Global Configuration

### Global Configuration

Global configuration applies to all repositories on a system.

Example:

```bash
git config --global user.name "Sanjhi Agarkar"
```

### Local Configuration

Local configuration applies only to a specific repository.

Example:

```bash
git config user.name "ProjectUser"
```

---

## Commands Practiced

### Check Git Installation

```bash
git --version
```

Displays the installed Git version.

---

### Display Configuration

```bash
git config --list
```

Shows all Git settings.

---

### Display Username

```bash
git config --global user.name
```

Displays the configured username.

---

### Display Email

```bash
git config --global user.email
```

Displays the configured email address.

---

### Configure Username

```bash
git config --global user.name "Your Name"
```

Sets the username globally.

---

### Configure Email

```bash
git config --global user.email "your@email.com"
```

Sets the email globally.

---

### Initialize Repository

```bash
git init
```

Creates a new Git repository.

---

## Real World Example

Suppose a developer creates a project folder called Cloud-App. Initially, it is just a normal folder. After executing the `git init` command, Git creates a hidden `.git` directory inside the project. This transforms the folder into a Git repository capable of tracking changes and maintaining project history.

---

## Interview Questions

### What is Git?

Git is a Distributed Version Control System used to track changes made to files and maintain project history.

---

### Who created Git?

Git was created by Linus Torvalds in 2005.

---

### What is a Repository?

A repository is a project folder managed by Git that contains project files and version history.

---

### What is the .git Folder?

The `.git` folder stores commits, branches, logs, references, and configuration information required by Git.

---

### Difference Between Git and GitHub?

Git is a Version Control System, whereas GitHub is a cloud platform used to host Git repositories.
