# 03 Git Workflow

## What is Git Workflow?

Git Workflow is the process through which changes move from the Working Directory to the Staging Area, then to the Local Repository, and finally to a Remote Repository such as GitHub. It provides a structured approach to tracking changes and maintaining project history.

---

## Git Architecture

Git consists of four major components:

```text
Working Directory
        ↓
Staging Area
        ↓
Local Repository
        ↓
Remote Repository (GitHub)
```

---

## Working Directory

The Working Directory is the place where developers create and modify files. Changes made in the Working Directory are not automatically stored in Git history. These changes remain local until they are staged and committed.

Example files in the Working Directory:

* app.py
* notes.txt
* README.md

---

## Staging Area

The Staging Area acts as an intermediate layer between the Working Directory and the Local Repository. It allows developers to prepare selected changes before creating a commit. Files are moved into the Staging Area using the `git add` command.

---

## Local Repository

The Local Repository stores snapshots of the project in the form of commits. Each commit represents a saved version of the project and allows developers to return to previous states if necessary.

---

## Remote Repository

A Remote Repository stores the project online and enables collaboration among developers. GitHub is the most popular remote repository platform used with Git.

---

## File States in Git

A file in Git can exist in different states:

```text
Untracked
     ↓
git add
     ↓
Staged
     ↓
git commit
     ↓
Tracked
     ↓
Modify File
     ↓
Modified
```

### Untracked

Git can see the file, but it is not yet being monitored.

### Staged

The file has been selected for the next commit.

### Tracked

The file has been committed and is now part of Git history.

### Modified

Changes have been made to a tracked file but those changes have not yet been committed.

---

## Commands Practiced

### Check Repository Status

```bash
git status
```

Displays the current state of files.

---

### Add Files to Staging Area

```bash
git add notes.txt
```

Stages a specific file.

```bash
git add .
```

Stages all files.

---

### Create a Commit

```bash
git commit -m "Added notes file"
```

Creates a snapshot of the current state.

---

### View Commit History

```bash
git log
```

Displays detailed commit history.

```bash
git log --oneline
```

Displays commit history in a compact form.

---

### Compare Changes

```bash
git diff
```

Shows modifications made to files.

---

## Real World Example

Consider writing a report. The Working Directory is your desk where you write content. The Staging Area acts like a tray where you collect pages before submitting them. The Local Repository is your diary where each submitted version is saved permanently. GitHub acts as cloud storage where your report can be shared and accessed by others.

---

## Interview Questions

### Explain Git Workflow.

Git Workflow consists of four stages: Working Directory, Staging Area, Local Repository, and Remote Repository. Changes are moved to the Staging Area using `git add`, saved in the Local Repository using `git commit`, and uploaded to GitHub using `git push`.

### What is the purpose of the Staging Area?

The Staging Area acts as a buffer between the Working Directory and the Local Repository and allows developers to selectively prepare changes before committing them.

### Difference between git add and git commit?

`git add` moves changes to the Staging Area, while `git commit` permanently saves those changes inside the Local Repository.

### What does git diff do?

The `git diff` command displays differences between file versions and helps developers understand what changes have been made.
