# 🚀 Git & GitHub DevOps Mastery

*The professional guide that developers actually enjoy using* 🎯

---

## 📋 Quick Navigation

| Icon | Topic                                            | Icon | Topic                                |
| ---- | ------------------------------------------------ | ---- | ------------------------------------ |
| 🏁   | [Initialize Repository](#-initialize-repository) | 📈   | [Check Status](#-check-status)       |
| ↩️   | [Restore Staged](#️-restore-staged)              | 🔄   | [Revert Commit](#-revert-commit)     |
| ⏪    | [Reset Commit](#-reset-commit)                   | 🔄   | [Pull vs Fetch](#-pull-vs-fetch)     |
| 📥   | [Clone Repository](#-clone-repository)           | 🔍   | [Compare Changes](#-compare-changes) |
| 🌿   | [Branch & Merge](#-branch--merge)                | ⚔️   | [Conflict Occur](#️-conflict-occur)  |
| 🤝   | [Conflict Resolved](#-conflict-resolved)         | 🎯   | [Skills Gained](#-skills-gained)     |

---

## 🏁 Initialize Repository

**Launch your project with proper version control from day one**

```bash
git init && git add .
git commit -m "feat: initial project setup"
git remote add origin https://github.com/user/repo.git
git push -u origin main
```

<p align="center">
  <img src="https://github.com/nikiimisal/Git-Github-GitLab/blob/main/img/git1.png?raw=true" width="700" alt="Initialize Repository Screenshot">
</p>

---

## 📈 Check Status

**Keep your finger on the pulse of repository changes**

```bash
echo "<!DOCTYPE html><html><body>Welcome</body></html>" > index.html
git status
```

**Expected Output:**

```
Untracked files:
  index.html
```
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git status
    On branch master
    Your branch is up to date with 'origin/master'.
    
    nothing to commit, working tree clean
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_workspace/git/practical (master)
    $ echo "Hello World" > index.html
    git status
    On branch master
    Your branch is up to date with 'origin/master'.
    
    Changes not staged for commit:
    (use "git add <file>..." to update what will be committed)
    (use "git restore <file>..." to discard changes in working directory)
    modified: index.html
    
    no changes added to commit (use "git add" and/or "git commit -a")


---

## ↩️ Restore Staged

**Fix staging mistakes without losing your work**

```bash
git add file.txt              # Accidentally staged?
git restore --staged file.txt # No problem!
git status                   # Back to clean state
```

o/p except:

    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git add
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git restore --staged about.html
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git status -s
    ?? about.html
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $

---

## 🔄 Revert Commit

**Undo changes safely in team environments**

```bash
git log --oneline    # Review commit history
git revert a1b2c3d   # Create safe undo commit
git log --oneline    # Verify clean history
```
O/P Except :

     nik0m@Nikhil-HD3SE36 MINGW64 ~/Desktop/nik_workspace/git/practical (master)
     $ git commit -m 'revert.html'
     [master bbd1e3d] revert.html
     1 file changed, 1 insertion(+), 1 deletion(-)
     rename about.html => revert.html (88%)
     
     nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git log --oneline
     bbd1e3d (HEAD -> master) revert.html
     645c97e added aboout.html
     9628029 added
     d8d7ad6 (origin/master) added index.html
     
     nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git revert bbd1e3d
    error: there was a problem with the editor 'vi'
    Please supply the message using either -m or -F option.
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_workspace/git/practical (master)
    $ git log --oneline
    bbd1e3d (HEAD -> master) revert.html
    645c97e added aboout.html
    9628029 added
    d8d7ad6 (origin/master) added index.html

---

## ⏪ Reset Commit

**Rewind time with precision and control**

```bash
git reset --hard HEAD~1   # ⚠️ Destructive: removes everything
git reset --soft HEAD~1   # 🛡️ Safe: keeps changes staged
```

O/P Except :

     nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git log oneline
     
     nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git log --oneline
     3b2e4da (HEAD -> master) resethard.html
     bbd1e3d revert.html
     645c97e added aboout.html
     9628029 added
     d8d7ad6 (origin/master) added index.html
     
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git reset --hard bbd1e3d
     HEAD is now at bbd1e3d revert.html
     
     nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git log --oneline
     bbd1e3d (HEAD -> master) revert.html
     645c97e added aboout.html

*🚨 Critical: Never use hard reset on shared branches!*

---

## 🔄 Pull vs Fetch

**Choose the right sync strategy for your workflow**

```bash
# 🎯 Strategic Approach (Teams)
git fetch origin
git merge origin/main

# ⚡ Quick Approach (Solo)
git pull

# 🧹 Clean Approach (Linear History)
git pull --rebase
```

O/P Except :

     nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
     $ git fetch origin
     remote: Enumerating objects: 7, done.
     remote: Counting objects: 100% (7/7), done.
    remote: Compressing objects: 100% (3/3), done.
    remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    Unpacking objects: 100% (6/6), 1.75 KiB | 39.00 KiB/s, done.
    From https://github.com/RajAhire-1/practical
    d8d7ad6..69cd98e master -> origin/master
    * [new branch] main-> origin/main
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git merge origin
    fatal: refusing to merge unrelated histories
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git merge origin master
    fatal: refusing to merge unrelated histories
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git merge
    Merge made by the 'ort' strategy.
    fetch.html 1+
    1 file changed, 1 insertion(+)
    create mode 100644 fetch.html
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git pull
    remote: Enumerating objects: 4, done.
    remote: Counting objects: 100% (4/4), done.
    remote: Compressing objects: 100% (2/2), done.
    remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
    Unpacking objects: 100% (3/3), 968 bytes | 12.00 KiB/s, done.
    From https://github.com/nikiimisal-1/practical
 



*🏆 Recommended: Fetch + Merge for team collaboration*

---

## 📥 Clone Repository

**Get started with any project in seconds**

```bash
git clone https://github.com/user/project.git
cd project
git status
```

*🚀 Pro Tip: Use SSH URLs for faster, more secure authentication*

---

## 🔍 Compare Changes

**Become a code detective with powerful diff tools**

```bash
git diff                    # Unstaged changes
git diff --staged          # Staged changes
git diff HEAD origin/main  # Compare with remote
git diff feature main      # Branch differences
```

O/P Except :

    nik0m@Nikhil MINGW64 ~/Desktop/nik_workspace/git/practical (master|MERGING)
    $ git diff
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master|MERGING)
    $ git diff --staged
    diff --git a/pull.html b/pull.html
    new file mode 100644
    index 0000000..20864b3
    -/dev/null
    +++ b/pull.html
    @@ -0,0 +1 @@
    +<h1>pull operation </h1>

*👀 Use Cases: Code reviews, debugging, change validation*

---

## 🌿 Branch & Merge

**Master professional feature development workflow**

```bash
# Create feature branch
git checkout -b feature-login

# Develop feature
echo "Authentication module" > login.html
git add . && git commit -m "feat: add login system"

# Merge to main
git checkout main
git merge feature-login
git branch -d feature-login
```

O/P Except :


    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master MERGING)
    $ git branch feature-login
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master (MERGING)
    $ git checkout feature-login
    A pull.html
    Switched to branch 'feature-login'
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (feature-login)
    $ echo "Login feature" > login.html
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (feature-login)
    $ git add
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (feature-login)
    $ git commit -m 'added login.html'
    [feature-login 951c0d6] added login.html
    3 files changed, 3 insertions(+)
    create mode 100644 login.html
    create mode 100644 pull.html
    create mode 160000 sample-project
    
    nik0m@Nikhil MINGW64 /Desktop/nik_Workspace/git/practical (feature-login)
    $ git checkout master
    warning: unable to rmdir 'sample-project': Directory not empty
    Switched to branch 'master'
    Your branch and 'origin/master" have diverged,
    and have 4 and 1 different commits each, respectively.
    (use "git pull" if you want to integrate the remote branch with yours)
    
    nik0m@Nikhil MINGW64 ~/Desktop/nik_Workspace/git/practical (master)
    $ git merge feature-login
    Updating eeb9357..951c0d6
    Fast-forward
    login.html  | 1+
    pull.html  | 1+
    sample-project | 1+
    3 files changed, 3 insertions(+)
    create mode 100644 login.html
    create mode 100644 pull.html


*🌊 Professional Practice: One feature per branch, clean merge history*

---

## ⚔️ Conflict Occur

**Understand when and why Git conflicts happen**

```bash
# Simulate a merge conflict
git checkout -b feature-header
echo "Header v1" > header.html
git add . && git commit -m "feat: add header v1"

git checkout main
echo "Header v2" > header.html
git add . && git commit -m "feat: update header v2"

# Now merge conflicting changes
git merge feature-header
```

**Expected Output:**

```
Auto-merging header.html
CONFLICT (content): Merge conflict in header.html
Automatic merge failed; fix conflicts and then commit the result.
```

<p align="center">
  <img src="https://github.com/nikiimisal/Git-Github-GitLab/blob/main/img/git3.png?raw=true" width="700" alt="Conflict Occur Screenshot">
</p>

*⚠️ What Happened: Both branches modified the same file in overlapping lines.*

---

## 🤝 Conflict Resolved

**Turn merge chaos into collaboration success**

```bash
# Open conflicting file
# Resolve manually:
# <<<<<<< HEAD
# Header v2
# =======
# Header v1
# >>>>>>> feature-header

# Keep the correct version, then:
git add header.html
git commit -m "fix: resolve merge conflict in header.html"
```

<p align="center">
  <img src="https://github.com/nikiimisal/Git-Github-GitLab/blob/main/img/git4.png?raw=true" width="700" alt="Conflict Resolved Screenshot">
</p>

*✅ Best Practice: Always discuss conflict resolutions with your teammate before finalizing.*

---

## 🎯 Skills Gained

### Core Competency Matrix

| Skill                | Proficiency | Real-World Impact               |
| -------------------- | ----------- | ------------------------------- |
| **Repository Setup** | 🏆 Expert   | Rapid project initialization    |
| **Change Tracking**  | 🏆 Expert   | Efficient daily workflow        |
| **Undo Operations**  | 🏆 Expert   | Risk-free mistake recovery      |
| **Branch Strategy**  | 🏆 Expert   | Seamless team collaboration     |
| **Remote Workflows** | 🏆 Expert   | Distributed development mastery |

---

## 📁 Documentation Structure

```
screenshots/
├── init-push.png          # Project initialization
├── git-status.png         # Change tracking
├── restore-staged.png     # Staging management
├── revert-commit.png      # Safe undo operations
├── reset-commit.png       # History management
├── pull-fetch.png         # Team synchronization
├── clone-repo.png         # Environment setup
├── git-diff.png           # Code comparison
├── branch-merge.png       # Feature development
├── conflict-occur.png     # Merge conflict simulation
└── conflict-resolved.png  # Conflict resolution demonstration
```

### 🎨 Professional Standards

* **Terminal**: Consistent dark theme (One Dark Pro)
* **Font**: 14pt monospace for readability
* **Layout**: Clear command → output flow
* **Focus**: Highlight key information

---

## 💡 Why This Guide Works

* ✅ **Practical Focus**: Commands you use every day
* ✅ **Visual Learning**: Screenshots provide instant validation
* ✅ **Risk Awareness**: Clear warnings for dangerous operations
* ✅ **Team Ready**: Workflows designed for collaboration
* ✅ **Professional**: Industry-standard practices

---

## 🏆 Career Impact

Mastering these Git skills prepares you for:

* **Senior Developer roles**
* **DevOps Engineering positions**
* **Technical Lead opportunities**
* **Open Source contributions**

---

## 🎯 Next Steps

**Immediate Actions:**

1. Practice each command in a sandbox repository
2. Create your own screenshot library
3. Implement these workflows in current projects

**Professional Growth:**

* Set up Git hooks for code quality
* Master advanced merge strategies
* Contribute to team Git standards
* Mentor junior developers

---

*"Good Git habits are the foundation of professional software development. This guide builds that foundation."*
