# 05 Branching

## What is a Branch?

A branch is an independent line of development.

---

## Why Use Branches?

Branches allow developers to work independently without affecting the main project.

---

## Branch Structure

```text
main
 │
 ├── feature-login
 │
 ├── feature-payment
 │
 └── bug-fix
```

---

## Commands Practiced

### Show Branches

```bash
git branch
```

---

### Create Branch

```bash
git branch feature-login
```

---

### Switch Branch

```bash
git switch feature-login
```

or

```bash
git checkout feature-login
```

---

## Real World Example

A developer creates a feature-login branch to implement authentication without affecting the stable main branch.

---

## Interview Questions

### What is a branch?

A branch is an independent line of development in Git.

### Why are branches important?

They allow parallel development and protect stable code.

### What is the default branch?

main

### Difference between git branch and git switch?

git branch creates branches.

git switch changes branches.

---