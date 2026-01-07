# ⚡ GIT CHEAT SHEET (1-PAGE QUICK REFERENCE)

A minimal, practical Git reference for daily use, revision, and interviews.

------------------------------------------------------------

## 🔹 BASIC SETUP

Initialize repository:
git init

Set default branch (one-time):
git config --global init.defaultBranch main

------------------------------------------------------------

## 🔹 STAGING & COMMITS

Check status:
git status

Stage all changes:
git add .

Commit changes:
git commit -m "message"

------------------------------------------------------------

## 🔹 BRANCHES

List branches:
git branch

Rename branch to main:
git branch -m master main

Create new branch:
git branch <branch-name>

Switch branch:
git checkout <branch-name>
or
git switch <branch-name>

------------------------------------------------------------

## 🔹 REMOTE REPOSITORY

Add remote:
git remote add origin <repo-url>

View remotes:
git remote -v

------------------------------------------------------------

## 🔹 PUSH & PULL

First push:
git push -u origin main

Regular push:
git push

Pull changes (safe):
git pull origin main --rebase

------------------------------------------------------------

## 🔹 COMMON ERRORS & FIXES

src refspec main does not match any:
→ Branch does not exist
Fix:
git branch -m master main

origin does not appear to be a git repository:
→ Remote not added
Fix:
git remote add origin <repo-url>

push rejected (fetch first):
→ Remote has commits you don’t
Fix:
git pull origin main --rebase
git push

------------------------------------------------------------

## 🔹 CLEANUP

Delete remote branch:
git push origin --delete <branch>

------------------------------------------------------------

## 🔹 DAILY WORKFLOW

git status
git add .
git commit -m "message"
git push

------------------------------------------------------------

## 🔹 GOLDEN RULES

• Branches are pointers, not copies
• Commits are immutable snapshots
• origin is just a remote name
• First commit creates the branch
• Rebase keeps history clean
• Avoid --force unless necessary

------------------------------------------------------------

## 📌 RECOMMENDED FILE NAME

GIT_CHEAT_SHEET.md

------------------------------------------------------------

END
