# Git and GitHub Practice Guide

A comprehensive reference sheet and practice repository based on the fundamental concepts of version control using **Git** and cloud collaboration via **GitHub**. This guide covers the complete local-to-remote lifecycle, branching workflows, and collaboration mechanisms.

## 📌 Core Concepts Covered
* **Git vs GitHub:** Git is the local version control software; GitHub is the cloud-based hosting service for managing Git repositories.
* **The 3 Stages:** Working Directory ➡️ Staging Area ➡️ Local Repository.
* **Branching & Merging:** Safely isolating new feature development from production code.

---

## 🚀 Main Git Commands Reference

### 1. Configuration & Setup
Run these commands once when you first set up Git on your machine:
```bash
# Set up your identity globally
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Check your configuration details
git config --list
```

### 2. Initializing & Tracking (Local Workflow)
Use these commands to start a local project and track file changes:
```bash
# Initialize a new local Git repository
git init

# Check the status of your working directory (tracked vs untracked files)
git status

# Add a specific file to the Staging Area
git add filename.ext

# Add all modified and untracked files to the Staging Area
git add .

# Save staged changes permanently into the Local Repository
git commit -m "Your descriptive commit message"

# View the commit history log
git log --oneline
```

### 3. Branching & Merging
Isolate workflows and integrate changes securely:
```bash
# List all local branches (current branch highlighted with an asterisk)
git branch

# Create a new branch
git branch branch-name

# Switch to a specific branch
git checkout branch-name

# Shortcut: Create and switch to a new branch instantly
git checkout -b branch-name

# Merge changes from another branch into your current branch
git merge branch-name

# Safe deletion of a branch after successful merging
git branch -d branch-name
```

### 4. Working with Remotes (GitHub Collaboration)
Connect your local development work to a remote cloud repository on GitHub:
```bash
# Download/Copy an existing GitHub repository to your local machine
git clone <REPOSITORY_URL>

# Link your local repository to a remote repository for the first time
git remote add origin <REPOSITORY_URL>

# Verify your remote links
git remote -v

# Push your local commits up to the remote GitHub repository
git push -u origin main

# Pull and integrate the latest remote updates into your local environment
git pull origin main
```

---

## 🛠️ Step-by-Step Practice Workflow

Follow this standard checklist to practice the complete cycle explained in the course:

1. **Create a local folder** on your computer and open it in your terminal or VS Code.
2. Run `git init` to turn it into a Git repository.
3. Create a test file (e.g., `app.js` or `index.html`) and verify with `git status`.
4. Stage the file with `git add .` and commit it using `git commit -m "Initial commit"`.
5. Create a new branch (`git checkout -b feature-test`), modify a file, and commit the changes on that branch.
6. Switch back to your main branch (`git checkout main`) and run `git merge feature-test` to practice merging.
7. Create a clean repository on GitHub, map it using `git remote add origin`, and upload your work with `git push -u origin main`.
