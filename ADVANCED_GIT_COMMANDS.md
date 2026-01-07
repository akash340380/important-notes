# 🚀 Advanced Git Commands Guide

This document explains advanced Git commands for power users,
safe recovery, and complex workflows.

------------------------------------------------------------

## 🔹 1️⃣ Stash

**Purpose:** Temporarily save uncommitted changes without committing.

- Save changes:
git stash

- Save with message:
git stash save "work-in-progress"

- List stashes:
git stash list

- Apply last stash:
git stash apply

- Apply specific stash:
git stash apply stash@{2}

- Apply and drop stash:
git stash pop

- Drop stash without applying:
git stash drop stash@{0}

- Clear all stashes:
git stash clear

💡 Use case: Switching branches without committing unfinished work.

------------------------------------------------------------

## 🔹 2️⃣ Reset

**Purpose:** Undo commits or changes in working directory.

- Soft reset (keep changes staged):
git reset --soft <commit-hash>

- Mixed reset (unstage changes, keep working directory):
git reset --mixed <commit-hash>
or
git reset <commit-hash>  # default is mixed

- Hard reset (discard changes, move branch pointer):
git reset --hard <commit-hash>

- Reset specific file:
git checkout <commit-hash> -- <file>

⚠️ Warning: Hard reset permanently discards uncommitted changes!

------------------------------------------------------------

## 🔹 3️⃣ Reflog

**Purpose:** View all changes to branch references, even deleted commits.

- Show reflog:
git reflog

- Recover lost commit:
git checkout <commit-hash>
or
git reset --hard <commit-hash>

💡 Use case: Recover commits after accidental reset or force push.

------------------------------------------------------------

## 🔹 4️⃣ Revert

**Purpose:** Create a new commit that undoes changes in a previous commit.

- Revert a commit:
git revert <commit-hash>

- Revert multiple commits:
git revert <oldest>^..<newest>

💡 Safer than reset for shared branches (does not rewrite history).

------------------------------------------------------------

## 🔹 5️⃣ Cherry-Pick

**Purpose:** Apply a commit from another branch to current branch.

- Apply a commit:
git cherry-pick <commit-hash>

- Apply multiple commits:
git cherry-pick <hash1> <hash2> <hash3>

💡 Use case: Picking hotfixes or bug fixes into main branch.

------------------------------------------------------------

## 🔹 6️⃣ Interactive Rebase

**Purpose:** Edit commit history (combine, reorder, modify commits).

- Start interactive rebase for last N commits:
git rebase -i HEAD~N

- Commands in editor:
  - pick → keep commit
  - reword → change commit message
  - squash → combine with previous commit
  - edit → modify commit
  - drop → delete commit

💡 Use case: Clean commit history before pushing to remote.

------------------------------------------------------------

## 🔹 7️⃣ Tagging

**Purpose:** Mark important commits (release points, versions).

- Create tag:
git tag v1.0

- Annotated tag:
git tag -a v1.0 -m "Release version 1.0"

- Push tags:
git push origin v1.0
or
git push origin --tags

- Delete tag:
git tag -d v1.0
git push origin --delete v1.0

------------------------------------------------------------

## 🔹 8️⃣ Resetting Files to Remote Version

- Reset a single file to match remote:
git fetch origin
git checkout origin/main -- <file>

- Reset entire branch to remote (dangerous):
git fetch origin
git reset --hard origin/main

------------------------------------------------------------

## 🔹 9️⃣ Bisect

**Purpose:** Find the commit that introduced a bug.

- Start bisect:
git bisect start

- Mark bad commit:
git bisect bad

- Mark good commit:
git bisect good <commit-hash>

- Git will checkout midpoints automatically.  
- After finding the culprit:
git bisect reset

------------------------------------------------------------

## 🔹 10️⃣ Summary Table of Advanced Commands

| Command                  | Purpose                                      |
|---------------------------|----------------------------------------------|
| git stash                 | Temporarily save uncommitted changes        |
| git reset --soft/mixed/hard | Undo commits, control staging/workdir     |
| git reflog                | Recover lost commits or branch pointers     |
| git revert <commit>       | Undo commit without rewriting history       |
| git cherry-pick <commit>  | Apply commit from another branch            |
| git rebase -i HEAD~N      | Edit, squash, reorder commits               |
| git tag -a v1.0           | Annotate release points                      |
| git bisect                | Find commit that introduced a bug           |

------------------------------------------------------------

END
