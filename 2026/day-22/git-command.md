# Git Complete Cheatsheet

A practical and structured reference covering Git concepts and commonly used commands — from beginner to advanced.

---

# 1️⃣ Core Git Concepts

### Repository
A Git-tracked project directory.

### Working Directory
The files you are currently editing.

### Staging Area (Index)
Files marked to be included in the next commit.

### Commit
A snapshot of staged changes.

### Branch
An independent line of development.

### Remote
A version of your repo hosted elsewhere (e.g. GitHub).

### HEAD
Pointer to the current branch/commit.

---

# 2️⃣ Setup & Configuration

### git config
**Concept:** Configure Git behavior  
**What it does:** Sets user info and preferences  
**Example:**
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

### git init
**Concept:** Start tracking a project  
**What it does:** Creates a new Git repository  
**Example:**
```bash
git init
```

### git clone
**Concept:** Copy remote repo locally  
**What it does:** Downloads repository with history  
**Example:**
```bash
git clone https://github.com/user/repo.git
```

---

# 3️⃣ Basic Workflow

### git status
**Concept:** Check repo state  
**What it does:** Shows modified, staged, untracked files  
```bash
git status
```

### git add
**Concept:** Stage changes  
**What it does:** Adds files to staging area  
```bash
git add file.txt
git add .
```

### git commit
**Concept:** Save snapshot  
**What it does:** Records staged changes  
```bash
git commit -m "Commit message"
```

### git commit --amend
**Concept:** Modify last commit  
**What it does:** Edits previous commit  
```bash
git commit --amend -m "Updated message"
```

---

# 4️⃣ Viewing Changes & History

### git log
**Concept:** View history  
```bash
git log
git log --oneline
git log --graph
```

### git diff
**Concept:** Compare changes  
```bash
git diff
git diff --staged
```

### git show
**Concept:** Inspect commit  
```bash
git show <commit-hash>
```

---

# 5️⃣ Branching

### git branch
**Concept:** Manage branches  
```bash
git branch
git branch new-branch
git branch -d branch-name
```

### git checkout
**Concept:** Switch branches  
```bash
git checkout branch-name
```

### git switch (modern alternative)
```bash
git switch branch-name
git switch -c new-branch
```

### git merge
**Concept:** Combine branches  
```bash
git merge branch-name
```

### git rebase
**Concept:** Reapply commits on another base  
```bash
git rebase main
```

---

# 6️⃣ Remote Repositories

### git remote
**Concept:** Manage remote connections  
```bash
git remote -v
git remote add origin https://github.com/user/repo.git
```

### git push
**Concept:** Upload commits  
```bash
git push origin main
```

### git push -u
**Concept:** Set upstream branch  
```bash
git push -u origin main
```

### git pull
**Concept:** Fetch + merge  
```bash
git pull origin main
```

### git fetch
**Concept:** Download changes without merging  
```bash
git fetch
```

---

# 7️⃣ Undo & Reset

### git restore
**Concept:** Restore file content  
```bash
git restore file.txt
```

### git reset
**Concept:** Move HEAD / unstage changes  
```bash
git reset file.txt
git reset --soft HEAD~1
git reset --hard HEAD~1
```

### git revert
**Concept:** Safely undo commit  
```bash
git revert <commit-hash>
```

---

# 8️⃣ Stashing

### git stash
**Concept:** Temporarily save changes  
```bash
git stash
git stash pop
git stash list
```

---

# 9️⃣ Tagging

### git tag
**Concept:** Mark release points  
```bash
git tag v1.0
git tag -a v1.0 -m "Version 1.0"
git push origin v1.0
```

---

# 🔟 Inspection & Debugging

### git blame
**Concept:** See who changed what  
```bash
git blame file.txt
```

### git reflog
**Concept:** View HEAD movement history  
```bash
git reflog
```

### git bisect
**Concept:** Find buggy commit  
```bash
git bisect start
```

---

# 1️⃣1️⃣ Cleanup

### git rm
**Concept:** Remove tracked files  
```bash
git rm file.txt
```

### git clean
**Concept:** Delete untracked files  
```bash
git clean -f
```

---

# 1️⃣2️⃣ Advanced

### git cherry-pick
**Concept:** Apply specific commit to current branch  
```bash
git cherry-pick <commit-hash>
```

### git squash (via rebase)
```bash
git rebase -i HEAD~3
```

### git submodule
**Concept:** Include another repository  
```bash
git submodule add <repo-url>
```

---

# 🚀 Common Workflows

### New Feature Workflow
```bash
git checkout -b feature-x
git add .
git commit -m "Add feature"
git push -u origin feature-x
```

### Sync with Main
```bash
git checkout main
git pull origin main
git checkout feature-x
git rebase main
```

---

# 🧠 Best Practices

- Commit small, focused changes
- Write meaningful commit messages
- Pull before pushing
- Never `reset --hard` on shared branches
- Use branches for features

---

# 📌 Git States Diagram (Mental Model)

Working Directory  
→ git add → Staging Area  
→ git commit → Repository  
→ git push → Remote  

---

End of Cheatsheet.
