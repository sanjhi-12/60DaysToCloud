# 06 Merging

## What is Merging?

Merging combines changes from one branch into another.

---

## Branch Structure

```text
main
 │
 └── feature-login
         ↓
       Merge
         ↓
main
```

---

## Types of Merge

### Fast Forward Merge

Moves branch pointer forward.

### Three-Way Merge

Creates a merge commit.

---

## Commands Practiced

### Switch Branch

```bash
git switch feature-login
```

### Merge Branch

```bash
git merge feature-login
```

### View Commit History

```bash
git log --oneline
```

### View Graph

```bash
git log --oneline --graph --all
```

---

## Interview Questions

### What is merging?

Merging combines changes from one branch into another.

### What is a Fast Forward Merge?

A merge in which Git simply moves the branch pointer forward.

### What is a Three-Way Merge?

A merge that creates a merge commit when both branches contain unique commits.

---

## Key Takeaways

- Merging combines branch histories.
- Fast Forward merges don't create merge commits.
- Three-Way merges create merge commits.
- git merge integrates branches.