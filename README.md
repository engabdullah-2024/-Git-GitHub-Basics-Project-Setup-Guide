# Git & GitHub — Beginner Guide 🚀

A simple beginner-friendly guide to understanding **Git**, **GitHub**, and the most commonly used Git commands.

## 📌 What is Git?

**Git** is a distributed version control system that helps developers track changes in their code.

With Git, you can:

* Track changes
* Create checkpoints with commits
* Work with branches
* Go back to previous versions
* Collaborate with other developers

## 🌐 What is GitHub?

**GitHub** is a platform for hosting Git repositories online.

In simple terms:

> **Git = Version Control**
> **GitHub = Online platform for Git repositories**

---

## ⚙️ Git Setup

Check if Git is installed:

```bash
git --version
```

Configure your username:

```bash
git config --global user.name "Your Name"
```

Configure your email:

```bash
git config --global user.email "you@example.com"
```

Check your configuration:

```bash
git config --list
```

---

## 🚀 Start a Git Repository

Navigate to your project:

```bash
cd my-project
```

Initialize Git:

```bash
git init
```

Check the repository status:

```bash
git status
```

---

## ➕ Stage Changes

Add a specific file:

```bash
git add filename
```

Add all changes:

```bash
git add .
```

---

## 💾 Commit Changes

Create a commit:

```bash
git commit -m "Initial commit"
```

Example:

```bash
git commit -m "Add landing page"
```

---

## 🌐 Connect to GitHub

Add your GitHub repository as a remote:

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

Check the remote:

```bash
git remote -v
```

Rename the current branch to `main`:

```bash
git branch -M main
```

---

## ⬆️ Push to GitHub

Push your project for the first time:

```bash
git push -u origin main
```

After that, you can simply use:

```bash
git push
```

---

## ⬇️ Pull Changes

Get the latest changes from GitHub:

```bash
git pull
```

---

## 📥 Clone a Repository

Download an existing GitHub repository:

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

Then enter the project:

```bash
cd REPOSITORY
```

---

## 🌿 Branches

Create and switch to a new branch:

```bash
git switch -c feature-name
```

See all branches:

```bash
git branch
```

Switch back to `main`:

```bash
git switch main
```

---

## 🔀 Merge Branches

Switch to `main`:

```bash
git switch main
```

Merge your feature branch:

```bash
git merge feature-name
```

---

## 📜 Git History

View commit history:

```bash
git log
```

View a shorter version:

```bash
git log --oneline
```

---

## 🔄 Common Git Workflow

Most of the time, your workflow will look like this:

```bash
git status
git add .
git commit -m "Describe your changes"
git push
```

### The workflow:

```text
Write Code
    ↓
git status
    ↓
git add .
    ↓
git commit
    ↓
git push
    ↓
GitHub
```

---

## 🧠 Quick Reference

| Command      | Purpose                  |
| ------------ | ------------------------ |
| `git init`   | Initialize a repository  |
| `git status` | Check changes            |
| `git add .`  | Stage all changes        |
| `git commit` | Save a checkpoint        |
| `git push`   | Upload changes to GitHub |
| `git pull`   | Download latest changes  |
| `git clone`  | Clone a repository       |
| `git branch` | Manage branches          |
| `git switch` | Switch branches          |
| `git merge`  | Merge branches           |
| `git log`    | View commit history      |

---

## 🎥 Video

This repository accompanies my **Git & GitHub beginner tutorial**, where I explain these concepts and demonstrate the commands practically.

---

## ⭐ Support

If this guide helped you understand Git and GitHub, consider giving the repository a ⭐.

Happy coding! 🚀
