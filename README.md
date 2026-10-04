# 🚀 Git & GitHub Basics – Project Setup Guide

A simple step-by-step guide to put your project on GitHub.
Every command is explained in plain, easy words.

---

## 🤔 What is Git?

**Git** is a tool on your computer that **saves the history of your project**.

Think of it like a **save button in a video game** 🎮. Every time you save (commit), Git remembers exactly how your files looked at that moment. If you break something later, you can go back to an older save.

**Why use Git?**
- ⏪ **Go back in time** — undo mistakes and return to a working version
- 📜 **See history** — know what changed, when, and who changed it
- 🌿 **Try new ideas safely** — use branches to experiment without breaking your main code
- 👥 **Work in a team** — many people can work on the same project without overwriting each other

> 💡 Git works **offline** on your own computer. You don't need the internet to use it.

---

## 🌐 What is GitHub?

**GitHub** is a **website** that stores your Git projects **online** (in the cloud) ☁️.

Think of it like **Google Drive for code**. Git saves your history on your computer, and GitHub keeps a copy on the internet.

**Why use GitHub?**
- 💾 **Backup** — if your laptop breaks, your code is still safe online
- 🤝 **Teamwork** — share code with teammates and review each other's work
- 🌍 **Portfolio** — show your projects to employers and clients
- 🚀 **Deploy** — connect to services like Vercel or Netlify to put your website live

---

## ⚖️ Git vs GitHub — What's the Difference?

| | **Git** | **GitHub** |
|---|---|---|
| What is it? | A tool (program) | A website (service) |
| Where does it live? | On your computer 💻 | On the internet ☁️ |
| Needs internet? | ❌ No | ✅ Yes |
| Main job | Track and save changes | Store and share projects online |
| Made by | Linus Torvalds (2005) | GitHub Inc. (owned by Microsoft) |

**Simple way to remember:**

```
Git    = the camera 📷  (takes snapshots of your code)
GitHub = the photo album online 🖼️  (stores and shares those snapshots)
```

You use **Git** to save your work, then **push** it to **GitHub** to keep it online.

---

## 📖 Words You Will See

| Word | Simple meaning |
|---|---|
| **Repository (repo)** | Your project folder that Git is tracking |
| **Commit** | A saved snapshot of your project |
| **Staging area** | The "waiting room" for files before you commit them |
| **Branch** | A separate copy of your code to work on new features safely |
| **Remote** | The online version of your repo (on GitHub) |
| **Push** | Upload your commits to GitHub |
| **Pull** | Download new changes from GitHub |
| **Clone** | Copy a whole project from GitHub to your computer |
| **Merge** | Combine changes from one branch into another |

---

## 📦 Step 0: Install Git and Check It

Download Git from: https://git-scm.com/downloads

Then check that it works:

```bash
git --version
```

**What it does:** Shows which Git version is installed. If you see something like `git version 2.x.x`, you're ready.

---

## 👤 Step 1: Tell Git Who You Are (one time only)

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

**What it does:** Saves your name and email. Every time you save work (commit), Git writes your name on it.

> 💡 Use the **same email** as your GitHub account.
> `--global` means this setting works for **all** your projects on this computer.

Check your settings:

```bash
git config --list
```

---

## 📁 Step 2: Go to Your Project Folder

```bash
cd path/to/your-project
```

**What it does:** `cd` means "change directory". It moves you into your project folder.

Example:

```bash
cd Desktop/my-app
```

---

## 🎬 Step 3: Start Git in Your Project

```bash
git init
```

**What it does:** Turns your normal folder into a Git project. Git creates a hidden `.git` folder that tracks all your changes.

> ⚠️ Run this **only once** per project.

---

## 🔍 Step 4: Check the Status

```bash
git status
```

**What it does:** Shows what's happening in your project:
- 🔴 **Red files** → changed but not added yet
- 🟢 **Green files** → added and ready to commit

> 💡 Use `git status` a lot. It's your best friend.

---

## 🙈 Step 5: Create a `.gitignore` File (recommended)

Create a file named `.gitignore` in your project folder and list files Git should **ignore**:

```
node_modules/
.env
.DS_Store
dist/
build/
```

**What it does:** Stops Git from uploading big or secret files (like passwords in `.env` or the huge `node_modules` folder).

---

## ➕ Step 6: Add Files

Add **all** files:

```bash
git add .
```

Add **one** file:

```bash
git add index.html
```

**What it does:** Puts your files in the "staging area" — like putting items in a box before you seal it.
The `.` means "everything in this folder".

---

## 💾 Step 7: Commit (Save a Snapshot)

```bash
git commit -m "Initial commit"
```

**What it does:** Saves a snapshot of your added files with a message.
`-m` means "message" — write a short note about what you changed.

✅ Good messages:
- `"Add login page"`
- `"Fix navbar bug"`
- `"Update README"`

❌ Bad messages:
- `"stuff"`
- `"asdf"`

---

## 🌿 Step 8: Name Your Main Branch

```bash
git branch -M main
```

**What it does:** Renames your main branch to `main` (GitHub's default name).
`-M` forces the rename even if a branch already has a different name.

---

## 🌐 Step 9: Create a Repository on GitHub

1. Go to https://github.com and log in
2. Click the **+** button (top right) → **New repository**
3. Type a name (example: `my-app`)
4. Choose **Public** or **Private**
5. ❗ **Don't** tick "Add a README" (you already have files)
6. Click **Create repository**

Copy the link GitHub gives you. It looks like:

```
https://github.com/your-username/my-app.git
```

---

## 🔗 Step 10: Connect Your Project to GitHub

```bash
git remote add origin https://github.com/your-username/my-app.git
```

**What it does:** Links your local project to your GitHub repo.
`origin` is just a nickname for that GitHub link (so you don't type the full URL every time).

Check the connection:

```bash
git remote -v
```

---

## ⬆️ Step 11: Push (Upload) Your Code

```bash
git push -u origin main
```

**What it does:** Uploads your commits to GitHub.
- `origin` → where to send (GitHub)
- `main` → which branch to send
- `-u` → remembers this, so next time you only type `git push`

🎉 Refresh your GitHub page — your code is online!

---

## 🔁 Daily Workflow (After First Setup)

Every time you make changes, just do these 3 commands:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

That's it! 🙌

---

## ⬇️ Other Useful Commands

### Download someone's project

```bash
git clone https://github.com/username/project.git
```

**What it does:** Copies a full project from GitHub to your computer.

### Get the latest changes

```bash
git pull
```

**What it does:** Downloads new changes from GitHub (for example, work your teammate pushed) and merges them into your code.

### See your history

```bash
git log --oneline
```

**What it does:** Shows a short list of all your commits.

### See what you changed

```bash
git diff
```

**What it does:** Shows the exact lines you changed but haven't added yet.

---

## 🌱 Branches (Work Without Breaking Main)

Create and switch to a new branch:

```bash
git checkout -b feature-login
```

**What it does:** Makes a new branch called `feature-login` and moves you to it. Your `main` code stays safe while you experiment.

Switch back to main:

```bash
git checkout main
```

List all branches:

```bash
git branch
```

Push your branch to GitHub:

```bash
git push -u origin feature-login
```

Merge a branch into main:

```bash
git checkout main
git merge feature-login
```

**What it does:** Brings the changes from `feature-login` into `main`.

---

## 🧯 Fixing Small Mistakes

| Problem | Command | What it does |
|---|---|---|
| Added a file by mistake | `git restore --staged file.txt` | Removes it from the staging area (your changes stay) |
| Want to undo changes in a file | `git restore file.txt` | Goes back to the last saved version ⚠️ changes are lost |
| Wrong commit message | `git commit --amend -m "New message"` | Fixes the last commit message (only before pushing) |
| Undo last commit, keep changes | `git reset --soft HEAD~1` | Removes the commit but keeps your files |

---

## 📋 Quick Cheat Sheet

| Command | Meaning |
|---|---|
| `git init` | Start Git in a folder |
| `git status` | See what changed |
| `git add .` | Add all files |
| `git commit -m "msg"` | Save a snapshot |
| `git branch -M main` | Name branch `main` |
| `git remote add origin URL` | Connect to GitHub |
| `git push -u origin main` | First upload |
| `git push` | Upload changes |
| `git pull` | Download changes |
| `git clone URL` | Copy a project |
| `git log --oneline` | See history |
| `git checkout -b name` | New branch |
| `git merge name` | Merge a branch |

---

## 🧠 Remember

```
Edit files  →  git add  →  git commit  →  git push
  (work)       (pack)      (save)        (upload)
```

Happy coding! 💻✨
