# Version-Controlled DevOps Project Using Git & GitHub

## 1. Project Overview

This project demonstrates how to manage a DevOps project using Git and GitHub version control best practices.

The main objective is to understand how developers manage source code, track changes, create branches, collaborate through Pull Requests, resolve merge conflicts, and maintain project versions.

## 2. Objective

- Understand Git and GitHub.
- Manage project code using version control.
- Create and manage multiple branches.
- Practice Git commits and pushes.
- Merge code using Pull Requests.
- Resolve merge conflicts.
- Use Git tags and `.gitignore`.
- Maintain proper project documentation.

## 3. Tools and Technologies

| Tool | Purpose |
|---|---|
| Git | Version control system |
| GitHub | Remote code repository |
| Git Bash | Execute Git commands |
| Markdown | Project documentation |

## 4. Project Structure

```text
version-controlled-devops-project/
│
├── README.md
├── .gitignore
│
├── src/
│   └── app.txt
│
├── docs/
│   └── workflow.md
│
└── dev-update.txt
```

## 5. Git Branching Strategy

This project uses three main branches.

### Main Branch
- Contains stable and production-ready code.
- Final development changes are merged here.

### Dev Branch
- Used for development and testing.
- Receives completed feature changes.

### Feature Branch
- Used to develop new features.
- Changes are committed and pushed separately.
- Merged into the dev branch through Pull Requests.

### Branching Workflow

```text
          main
            |
            |
           dev
            |
            |
     feature branch
            |
       Code Changes
            |
       Git Commit
            |
       Git Push
            |
      Pull Request
            |
       Merge into dev
            |
        Testing
            |
      Pull Request
            |
       Merge into main
```

## 6. Project Implementation Steps

### Step 1: Configure Git

```bash
git config --global user.name "Aman Maniyar"
git config --global user.email "your-email@gmail.com"
```

### Step 2: Initialize Repository

```bash
mkdir version-controlled-devops-project
cd version-controlled-devops-project
git init
git branch -M main
```

### Step 3: Create Project Files

```bash
mkdir src docs
touch README.md .gitignore
touch src/app.txt
touch docs/workflow.md
```

### Step 4: Add and Commit Files

```bash
git add .
git commit -m "Initial project setup"
```

### Step 5: Connect GitHub Repository

```bash
git remote add origin https://github.com/YOUR_USERNAME/version-controlled-devops-project.git
git push -u origin main
```

### Step 6: Create Dev Branch

```bash
git checkout -b dev
git push -u origin dev
```

### Step 7: Create Feature Branch

```bash
git checkout -b feature/update-documentation
```

### Step 8: Commit and Push Changes

```bash
git add .
git commit -m "Update Git workflow documentation"
git push -u origin feature/update-documentation
```

### Step 9: Create Pull Request

1. Open the GitHub repository.
2. Navigate to Pull Requests.
3. Click New Pull Request.
4. Select `dev` as the base branch.
5. Select `feature/update-documentation` as the compare branch.
6. Create and review the Pull Request.
7. Merge the Pull Request into dev.

### Step 10: Merge Dev into Main

1. Open Pull Requests.
2. Select `main` as the base branch.
3. Select `dev` as the compare branch.
4. Create a Pull Request.
5. Review the changes.
6. Merge the Pull Request into main.

Note: A Pull Request is only available when the source branch contains changes not already present in the target branch.

### Step 11: Create Git Tag

```bash
git checkout main
git pull origin main
git tag -a v1.0 -m "Version 1.0 release"
git push origin v1.0
```

### Step 12: Verify Git History

```bash
git status
git branch
git log --oneline
git tag
git remote -v
```

## 7. Merge Conflict Resolution

A merge conflict occurs when Git cannot automatically combine changes from different branches, for example, when two branches modify the same lines of a file.

Steps to resolve:

1. Identify the conflicted file.
2. Open the file.
3. Review both changes.
4. Select the correct content.
5. Remove conflict markers.
6. Save the file.
7. Add and commit the resolved file.

Commands:

```bash
git status
git add .
git commit -m "Resolve merge conflict"
```

## 8. Git .gitignore

The `.gitignore` file tells Git which files and directories should not be tracked.

Example:

```gitignore
*.log
*.tmp
.env
node_modules/
dist/
build/
.DS_Store
Thumbs.db
.vscode/
.idea/
```

Never commit passwords, access keys, or other sensitive credentials.

## 9. Git Tags

Git tags identify specific commits, usually for software releases.

Example:

```bash
git tag -a v1.0 -m "First release"
git push origin v1.0
git tag
```

## 10. Important Git Commands

| Command | Description |
|---|---|
| `git init` | Initialize repository |
| `git clone URL` | Clone repository |
| `git status` | Check repository status |
| `git add .` | Stage changes |
| `git commit -m "message"` | Commit changes |
| `git push` | Upload changes |
| `git pull` | Download and integrate changes |
| `git fetch` | Fetch remote updates |
| `git branch` | List branches |
| `git checkout -b dev` | Create and switch branch |
| `git switch main` | Switch branch |
| `git merge dev` | Merge dev branch |
| `git log --oneline` | View commit history |
| `git stash` | Temporarily save changes |
| `git tag` | List tags |

## 11. Interview Questions and Answers

### Q1. What is Git?
Git is a distributed version control system used to track code changes and manage different versions of a project.

### Q2. What is GitHub?
GitHub is a cloud-based platform used to host Git repositories and collaborate with developers.

### Q3. What is the difference between Git and GitHub?
- Git is a version control tool.
- GitHub is a platform for hosting and managing Git repositories.

### Q4. What is a Git repository?
A Git repository is a location where project files and their version history are stored.

### Q5. What is a Git branch?
A branch is an independent line of development that allows developers to work on different features without directly changing the main code.

### Q6. What is the difference between merge and rebase?
- Merge combines changes from two branches and preserves their branch history.
- Rebase moves commits onto a new base commit and creates a more linear history.

### Q7. What is a Pull Request?
A Pull Request is a request to review code changes and merge them from one branch into another.

### Q8. What is a merge conflict?
A merge conflict happens when Git cannot automatically combine changes from different branches.

### Q9. How do you resolve merge conflicts?
I open the conflicted file, review the changes, select the correct code, remove conflict markers, save the file, and commit the resolution.

### Q10. What are Git tags?
Git tags are used to mark specific commits, usually for software releases such as v1.0 and v2.0.

### Q11. What is Git stash?
Git stash temporarily saves uncommitted changes so that I can work on another task without committing those changes.

### Q12. What is the use of .gitignore?
The `.gitignore` file tells Git which files and folders should not be tracked.

### Q13. What is the difference between git pull and git fetch?
- `git fetch` downloads remote updates without merging them into the current branch.
- `git pull` fetches remote changes and integrates them into the current branch.

### Q14. What is the difference between git add and git commit?
- `git add` stages changes.
- `git commit` saves staged changes in the repository history.

### Q15. What is the difference between main, dev, and feature branches?
- Main: Production-ready code.
- Dev: Development and testing.
- Feature: Development of individual features.

## 12. Challenges Faced

- Understanding Git branching and branch switching.
- Managing local and remote repositories.
- Understanding Pull Requests and merge workflows.
- Handling situations where there were no changes to compare.
- Practicing merge conflict resolution.
- Maintaining a clean commit history.

## 13. Learning Outcomes

Through this project, I learned:

- Git and GitHub fundamentals.
- Version control and source code management.
- Branching and merging strategies.
- Pull Request workflows.
- Merge conflict resolution.
- Git tags and version management.
- Documentation using Markdown.

## 14. Conclusion

This project helped me understand how Git and GitHub are used in real-world DevOps workflows. I gained practical experience in managing code, maintaining branches, tracking changes, reviewing code through Pull Requests, and managing project versions.

---

**Project:** Version-Controlled DevOps Project

**Author:** Aman Maniyar

**Tools:** Git | GitHub | Git Bash

**Repository:** 
