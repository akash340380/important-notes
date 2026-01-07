# 💻 IntelliJ IDEA Git Cheat Sheet

A quick reference for using Git efficiently inside IntelliJ IDEA.

------------------------------------------------------------

## 🔹 BASIC GIT SETUP IN INTELLIJ

1. Enable Git in IntelliJ:
   - Settings → Version Control → Git → Path to Git executable
   - Test connection

2. Initialize Git in project:
   - VCS → Enable Version Control Integration → Git

3. Check branch:
   - VCS → Git → Branches
   - Or look at bottom-right branch indicator

------------------------------------------------------------

## 🔹 STAGING & COMMITS

1. Stage files:
   - VCS → Git → Add
   - Or right-click file → Git → Add to VCS
   - Shortcut: `Ctrl + Alt + A` (Windows/Linux), `⌘ + Alt + A` (Mac)

2. Commit changes:
   - VCS → Commit → Commit dialog
   - Enter commit message
   - Options:
     - Commit
     - Commit and Push

3. Commit only staged files:
   - In Commit dialog, check/uncheck files
   - IntelliJ stages automatically if checkbox selected

------------------------------------------------------------

## 🔹 BRANCHES

1. View branches:
   - Bottom-right branch indicator → Click

2. Create branch:
   - Git → Branches → New Branch

3. Switch branch:
   - Git → Branches → Checkout

4. Rename branch:
   - Git → Branches → Rename

5. Delete branch:
   - Git → Branches → Delete

------------------------------------------------------------

## 🔹 REMOTE REPOSITORY

1. Add remote:
   - VCS → Git → Remotes → Add
   - Enter repo URL

2. View remote:
   - Git → Remotes

3. Fetch from remote:
   - Git → Fetch
   - Shortcut: `Ctrl + T` (Windows/Linux), `⌘ + T` (Mac)

4. Pull changes:
   - VCS → Git → Pull
   - Use Rebase option for clean history

5. Push changes:
   - VCS → Git → Push
   - Shortcut: `Ctrl + Shift + K` (Windows/Linux), `⌘ + Shift + K` (Mac)

------------------------------------------------------------

## 🔹 MERGES & REBASE

1. Merge branch:
   - Git → Merge Changes → select branch

2. Rebase branch:
   - Git → Rebase → select branch
   - Use to integrate remote commits cleanly

3. Resolve conflicts:
   - IntelliJ opens merge tool automatically
   - Choose between Accept Yours / Accept Theirs / Merge manually

------------------------------------------------------------

## 🔹 VIEW HISTORY & LOGS

1. View commit history:
   - VCS → Git → Show History
   - Or right-click file → Git → Show History

2. View branch tree:
   - Git → Branches → Show Branches

3. View file history:
   - Right-click file → Git → Show History

------------------------------------------------------------

## 🔹 RESET & RECOVERY

1. Undo changes:
   - Right-click file → Git → Rollback
   - Undo uncommitted changes

2. Reset to commit:
   - Git → Show History → Right-click commit → Reset Current Branch
   - Options: Soft, Mixed, Hard

3. Stash changes:
   - Git → Stash Changes
   - Apply stash later via Git → Unstash Changes

------------------------------------------------------------

## 🔹 DAILY WORKFLOW (INTELLIJ)

1. Stage files → Commit → Push
2. Pull before starting work (use Rebase)
3. Work on feature branches
4. Merge/rebase carefully to main
5. Always check status and branch indicator

------------------------------------------------------------

## 🔹 SHORTCUTS (Windows / Mac)

| Action                  | Windows/Linux        | Mac                   |
|-------------------------|--------------------|---------------------|
| Commit                  | Ctrl + K           | ⌘ + K               |
| Push                    | Ctrl + Shift + K   | ⌘ + Shift + K       |
| Pull                    | Ctrl + T           | ⌘ + T               |
| Add to VCS              | Ctrl + Alt + A     | ⌘ + Alt + A         |
| Show History            | Alt + 9            | ⌥ + 9               |
| Switch Branch           | Ctrl + `           | Ctrl + `            |

------------------------------------------------------------

## 🔹 BEST PRACTICES

- Use `main` as default branch
- Pull before committing
- Commit small, meaningful changes
- Use feature branches for work
- Push frequently to avoid conflicts
- Use IntelliJ merge tool for conflicts

------------------------------------------------------------

## 📌 RECOMMENDED FILE NAME

INTELLIJ_GIT_CHEAT_SHEET.md

------------------------------------------------------------

END
