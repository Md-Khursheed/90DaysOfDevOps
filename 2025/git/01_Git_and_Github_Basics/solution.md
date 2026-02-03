# Week 4 Challenge - Git & GitHub
## Introduction

This document contains a step-by-step guide on completing the Week 4 Challenge of the #90DaysOfDevOps program. It includes essential Git operations, branching, authentication methods, and advanced tasks like SSH setup. Each step is accompanied by images to help visualize the process.

---

## 🚀 Task 1: Fork and Clone the Repository
### 1️⃣ Fork the Repository

- Navigate to the 90DaysOfDevOps Repository and click Fork.

- This creates a copy under your GitHub account.

### 🖼 Example of Your Forked Repo:

![Forked Repository](images/Screenshot 2026-02-02 203840.png)

### 2️⃣ Clone the Forked Repository

```bash
# Replace <your-fork-url> with your forked repository link
git clone <your-fork-url>
cd 90DaysOfDevOps/2025/git/01_Git_and_Github_Basics
```

## 🏗️ Task 2: Initialize a Git Repository & Create a File
### 1️⃣ Initialize Git Repository

```bash
mkdir week-4-challenge
cd week-4-challenge
git init
```

### 2️⃣ Create and Commit a File

```bash
echo "Hello, this is my Git challenge!" > info.txt
git add info.txt
git commit -m "Initial commit: Add info.txt"
```

## 🔗 Task 3: Configure Remote & Push Changes
### 1️⃣ Configure Remote URL with PAT

```bash
# Replace <your-username> and <your-PAT> with actual values
git remote add origin https://USERNAME:TOKEN@github.com/USERNAME/90DaysOfDevOps.git
git push -u origin main
```

## 🔍 Task 4: View Git Commit History
### Check Commit Logs

```bash
git log
```

## 🌿 Task 5: Branching & Merging
### 1️⃣ Create and Switch to a New Branch

```bash
git branch feature-update
git switch feature-update
```

### 2️⃣ Modify and Commit Changes in New Branch

```bash
echo "Adding more details to the file." >> info.txt
git add info.txt
git commit -m "Feature update: Enhance info.txt"
git push origin feature-update
```

### 3️⃣ Merge Feature Branch to Main
- Create a Pull Request (PR) on GitHub and merge changes.
- Optionally you can Delete the feature branch after merging (I didn't do that for now).

🖼 Example of Opening a Pull Request:

![Opening Pull Request](images/Screenshot 2026-02-02 223659.png)

🖼 Example of Merging a PR:

![PR Merge Step 1](images/Screenshot 2026-02-02 223840.png)

![PR Merge Step 2](images/Screenshot 2026-02-02 223925.png)

## 🔒 Task 6: SSH Authentication
### 1️⃣ Generate SSH Key

```bash
ssh-keygen -t ed25519 -C "your-email@example.com"
```

### 2️⃣ Add SSH Key to GitHub
- copy the key:

```bash
cat ~/.ssh/id_ed25519.pub
```

- Go to GitHub Settings > SSH Keys, add the key.

### 3️⃣ Update Remote URL to SSH

```bash
git remote set-url origin git@github.com:<your-username>/90DaysOfDevOps.git
git push origin feature-update
```

## 🎯 Conclusion

🎉 Successfully completed Week 4 Challenge of #90DaysOfDevOps! This challenge deepened my understanding of Git workflows, remote configurations, authentication, and branching strategies.
