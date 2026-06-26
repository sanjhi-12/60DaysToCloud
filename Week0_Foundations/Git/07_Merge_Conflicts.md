# 07 Merge Conflicts

## What is a Merge Conflict?

A merge conflict occurs when Git cannot automatically combine changes.

---

## Why Do Conflicts Occur?

- Same file modified in multiple branches.
- Same lines changed differently.
- Delete vs modify operations.

---

## Conflict Markers

```text
<<<<<<< HEAD
Current branch
=======
Incoming branch
>>>>>>> branch-name
```

---

## Commands Practiced

### Create Branch

```bash
git branch feature-auth
```

### Switch Branch

```bash
git switch feature-auth
```

### Merge Branch

```bash
git merge feature-auth
```

### Resolve Conflict

```bash
git add app.py
git commit -m "Resolved merge conflict"
```

### View Graph

```bash
git log --oneline --graph --all
```

---

## Interview Questions

### What is a merge conflict?

A merge conflict occurs when Git cannot automatically combine changes.

### How do you resolve merge conflicts?

Open the conflicted file, remove markers, keep required code, stage the file, and commit.

### What are conflict markers?

Special markers inserted by Git to indicate conflicting code sections.

---

## Key Takeaways

- Merge conflicts are normal.
- Git never overwrites code automatically.
- Conflict markers help identify differences.
- Developers manually resolve conflicts.