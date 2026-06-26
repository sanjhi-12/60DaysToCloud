# 08 Remote Repositories

## What is a Remote Repository?

A Remote Repository is a repository stored on a remote server such as GitHub.

---

## Why Use Remote Repositories?

- Backup
- Collaboration
- Accessibility
- Synchronization

---

## Local vs Remote Repository

| Local Repository | Remote Repository |
|-----------------|----------------|
| Stored Locally | Stored Online |
| Offline Work | Collaboration |
| Faster | Shared |

---

## Commands Practiced

### View Remote

```bash
git remote
```

### View URLs

```bash
git remote -v
```

### Add Remote

```bash
git remote add origin <repo-url>
```

### Push Changes

```bash
git push -u origin main
```

### Download Changes

```bash
git pull
```

### Fetch Changes

```bash
git fetch
```

### Clone Repository

```bash
git clone <repo-url>
```

---

## Interview Questions

### What is a Remote Repository?

A repository stored on a remote server.

### Difference between git fetch and git pull?

git fetch downloads changes without merging.

git pull downloads and merges changes.

### What does git clone do?

Creates a local copy of a remote repository.

---

## Key Takeaways

- GitHub hosts remote repositories.
- git push uploads changes.
- git pull downloads and merges changes.
- git fetch only downloads.
- git clone creates a local copy.