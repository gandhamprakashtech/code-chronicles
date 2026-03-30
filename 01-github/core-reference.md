# Git Foundational Reference

A practical reference for day-to-day Git usage. Beginner to intermediate.

---

## 1. Standard Workflow

### Check status

git status

Shows modified/untracked files and current branch.

### Stage changes
git add <file>           # stage one file
git add .                # stage all changes in current 

### Commit

git commit -m "Your message"


### Pull before push

git pull                  # pull from default remote/branch
git pull origin main      # pull from specific remote and branch

Resolve any merge conflicts, then commit.

### Push

git push                  # push to default remote/branch
git push origin main      # push to specific remote and branch
git push -u origin main   # push and set upstream (first-time push for branch)


**Typical sequence:** `git status` → `git add .` → `git commit -m "..."` → `git pull` → `git push`

---

## 2. Branching Basics

### Create a branch

git branch feature-x              # create branch (does not switch)
git checkout -b feature-x         # create and switch in one step


### Switch branch
`
git checkout main
git switch main


### Merge a branch

git checkout main                 # switch to target branch
git merge feature-x               # merge feature-x into main

Resolve conflicts if any, then `git add` and `git commit`.


### want to completely remove all local modifications:
git reset --hard

### also want to remove untracked files
git clean -fd


### differences between the branches
git diff  origin/main prakash --name-only
to just displapy only file names

