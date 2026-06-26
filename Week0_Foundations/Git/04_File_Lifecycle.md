# 04 File Lifecycle

## What is File Lifecycle?

Git tracks files through different states.

---

## File Lifecycle Diagram

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

---

## Untracked State

Git sees the file but does not track it.

### Command

```bash
git status
```

---

## Staged State

Files are prepared for commit.

### Commands

```bash
git add file1.txt
git add .
```

---

## Tracked State

Files become part of Git history.

### Command

```bash
git commit -m "message"
```

---

## Modified State

Tracked files with changes are marked as Modified.

### Command

```bash
git diff
```

---

## Commands Practiced

```bash
git status
git add file1.txt
git add .
git commit -m
git diff
git log --oneline
```

---

## Interview Questions

### What are the states of a file in Git?

- Untracked
- Staged
- Tracked
- Modified

### What is an Untracked file?

A file that exists in the Working Directory but is not monitored by Git.

### What is a Staged file?

A file prepared for the next commit.

### What is a Modified file?

A tracked file whose contents have changed since the last commit.

---

## Key Takeaways

- Every file follows a lifecycle.
- git add moves files to the Staging Area.
- git commit saves snapshots.
- git diff compares changes.
- Git tracks modifications efficiently.