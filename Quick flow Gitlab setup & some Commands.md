# 🦊 GitLab Setup Guide for Beginners

Welcome to this simple step-by-step guide to get started with **GitLab** — from creating your account to pushing your first project using SSH!  
No fancy jargon, just clean steps and screenshots 🎯

---

## 🌍 1. Create Your GitLab Account

👉 Go to [https://gitlab.com](https://gitlab.com)  
Click **"Register"** → Sign up using **Google**, **GitHub**, or **email**.


---

## 💻 2. Install Git on Your System

If you haven’t installed Git yet, here’s how:

**For Windows:**
- Download from [https://git-scm.com/downloads](https://git-scm.com/downloads)
- Run installer → Keep default settings.

**For macOS:**

    brew install git

For Linux (Ubuntu/Debian):

    sudo apt update
    sudo apt install git -y


Verify installation:

    git --version

## 🔑 3. Create SSH Key (Secure Login to GitLab)

We’ll use SSH instead of HTTPS for smoother push/pull access.

Open Git Bash or your terminal and run:

    ssh-keygen -t ed25519 -C "your_email@example.com"

 Press Enter for default path → no password needed.

Then copy your SSH key:

    cat ~/.ssh/id_ed25519.pub

📋 Copy the full key shown on screen.

## ⚙️ 4. Add SSH Key to GitLab

Now go to your GitLab account:

1. Click on your Profile Picture → Edit Profile

2. In sidebar → Access → SSH Keys

3. Paste your copied key into the field.

4. Give it a title (like “My Laptop Key”)

5. Click Add key



## 🧩 5. Configure Git

Set your username and email (same as GitLab):

    git config --global user.name "Your Name"
    git config --global user.email "your_email@example.com"


Check:

    git config --list

## 📂 6. Create a New Repository on GitLab

1. Click New Project → Create Blank Project

2. Enter:

 • Project Name (e.g., `my-first-gitlab`)

 • Visibility: `Public` or `Private`

3. Click Create Project


## 🔄 7. Push Your First Code to GitLab

In your terminal:

    cd path/to/your/project
    git init
    git add .
    git commit -m "Initial commit"
    git remote add origin git@gitlab.com:username/my-first-gitlab.git
    git push -u origin main


(Replace `username` with your GitLab username)

🎉 Congrats! Your code is now live on GitLab.

## 🧠 8. Verify SSH Connection (Optional but Helpful)

To check your SSH setup:

    ssh -T git@gitlab.com


If you see something like 👇

    Welcome to GitLab, @yourusername!


you’re good to go! ✅

## 🚀 9. Basic Git Commands Reference

| Command               | Description              |
| --------------------- | ------------------------ |
| `git add .`           | Add all files for commit |
| `git commit -m "msg"` | Save changes locally     |
| `git push`            | Upload to GitLab         |
| `git pull`            | Get updates from GitLab  |
| `git status`          | See changed files        |


## 🧭 10. Done & Explore More!

You’ve now set up your GitLab from scratch, connected via SSH, and pushed your first code!
Try exploring:

• CI/CD Pipelines

• Issue Boards

• Merge Requests

💡 GitLab is not just hosting — it’s a full DevOps powerhouse.

## ❤️ Support & Connect

If you liked this guide, give it a ⭐ on your repo or share it!
Happy coding 🧑‍💻

<br>
<br>
<br>

## Some Commands

# 🦊 Git + GitLab Complete Beginner Command Table

---

## ⚙️ Git Setup Commands

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git --version` | Check installed Git version | `git --version` |
| `git config --global user.name "Your Name"` | Set global username | `git config --global user.name "Niikii"` |
| `git config --global user.email "you@example.com"` | Set global email | `git config --global user.email "niikii@example.com"` |
| `git config --list` | View current Git settings | `git config --list` |
| `git help <command>` | Get help for a specific command | `git help commit` |

---

## 🧠 Basic Git Commands

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git init` | Create new local repo | `git init` |
| `git clone <repo-url>` | Clone repo from GitLab | `git clone git@gitlab.com:user/project.git` |
| `git status` | Check file changes | `git status` |
| `git add .` | Add all files for commit | `git add .` |
| `git add <file>` | Add specific file | `git add index.html` |
| `git commit -m "msg"` | Save local changes | `git commit -m "Initial commit"` |
| `git log` | Show commit history | `git log` |
| `git diff` | Show changes before committing | `git diff` |
| `git show <commit-id>` | View details of a specific commit | `git show a1b2c3d` |

---

## 🧩 Branching & Merging

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git branch` | List all local branches | `git branch` |
| `git branch <name>` | Create a new branch | `git branch feature-login` |
| `git checkout <branch>` | Switch to branch | `git checkout main` |
| `git checkout -b <name>` | Create and switch branch | `git checkout -b dev` |
| `git merge <branch>` | Merge a branch into current one | `git merge dev` |
| `git branch -d <name>` | Delete local branch | `git branch -d dev` |
| `git push origin --delete <name>` | Delete remote branch | `git push origin --delete dev` |

---

## 🔄 Remote Repository Commands (GitLab Connection)

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git remote -v` | Show linked remote repos | `git remote -v` |
| `git remote add origin <url>` | Link local repo to GitLab | `git remote add origin git@gitlab.com:user/repo.git` |
| `git remote remove origin` | Remove existing remote | `git remote remove origin` |
| `git remote set-url origin <url>` | Change GitLab remote URL | `git remote set-url origin git@gitlab.com:user/newrepo.git` |
| `git push -u origin main` | Push main branch to GitLab | `git push -u origin main` |
| `git pull` | Fetch and merge changes from GitLab | `git pull` |
| `git fetch` | Download commits without merging | `git fetch` |

---

## 🗃️ Staging, Reset, and Cleanup

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git reset <file>` | Unstage file | `git reset index.html` |
| `git reset --hard` | Remove all uncommitted changes | `git reset --hard` |
| `git stash` | Temporarily save uncommitted work | `git stash` |
| `git stash pop` | Reapply last stash | `git stash pop` |
| `git clean -fd` | Remove untracked files | `git clean -fd` |
| `git gc` | Clean and optimize repo | `git gc` |
| `git reflog` | Show all history of HEAD changes | `git reflog` |

---

## 🧾 Tagging & Version Control

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git tag <tagname>` | Create new tag | `git tag v1.0` |
| `git tag -a <tagname> -m "msg"` | Annotated tag | `git tag -a v1.0 -m "Stable release"` |
| `git push origin <tagname>` | Push tag to GitLab | `git push origin v1.0` |
| `git push origin --tags` | Push all tags | `git push origin --tags` |
| `git tag -d <tagname>` | Delete tag locally | `git tag -d v1.0` |

---

## 🧱 SSH Setup Commands (GitLab Connection)

| Command | Description | Example |
| -------- | ------------ | -------- |
| `ssh-keygen -t ed25519 -C "email@example.com"` | Generate SSH key | `ssh-keygen -t ed25519 -C "niikii@example.com"` |
| `cat ~/.ssh/id_ed25519.pub` | Display public key | `cat ~/.ssh/id_ed25519.pub` |
| `ssh -T git@gitlab.com` | Test SSH connection | `ssh -T git@gitlab.com` |

---

## 🦊 GitLab CLI Commands (GLab Tool)

| Command | Description | Example |
| -------- | ------------ | -------- |
| `glab auth login` | Login to GitLab via terminal | `glab auth login` |
| `glab repo create` | Create new GitLab repo | `glab repo create` |
| `glab mr create` | Create a Merge Request | `glab mr create` |
| `glab mr list` | List all Merge Requests | `glab mr list` |
| `glab issue create` | Create a new Issue | `glab issue create` |
| `glab issue list` | List open issues | `glab issue list` |
| `glab release create v1.0 -t "Release notes"` | Create release tag | `glab release create v1.0 -t "First release"` |
| `glab ci status` | Show latest CI/CD pipeline status | `glab ci status` |
| `glab pipeline list` | List recent pipelines | `glab pipeline list` |
| `glab pipeline view <id>` | View specific pipeline | `glab pipeline view 102` |

---

## 🧩 Common GitLab Workflows (Steps)

| Step | Command / Action | Description |
|------|------------------|--------------|
| 1️⃣ | `git checkout -b feature-login` | Create a new feature branch |
| 2️⃣ | Make code changes | Update your project files |
| 3️⃣ | `git add .` | Stage changes |
| 4️⃣ | `git commit -m "Added login feature"` | Commit changes |
| 5️⃣ | `git push origin feature-login` | Push branch to GitLab |
| 6️⃣ | GitLab → “Create Merge Request” | Merge to main after review |
| 7️⃣ | `git pull origin main` | Update your main branch |

---

## ⚡ GitLab CI/CD Example (Bonus)

| File | Content |
|------|----------|
| `.gitlab-ci.yml` | ```yaml<br>stages:<br>  - build<br>  - deploy<br><br>build-job:<br>  stage: build<br>  script:<br>    - echo "Building app..."<br><br>deploy-job:<br>  stage: deploy<br>  script:<br>    - echo "Deploying..."<br>``` |

---

## 🧹 Maintenance & Cleanup

| Command | Description | Example |
| -------- | ------------ | -------- |
| `git fetch --prune` | Clean deleted remote branches | `git fetch --prune` |
| `git remote prune origin` | Remove stale remote refs | `git remote prune origin` |
| `git gc` | Compress & optimize | `git gc` |

---

## ❤️ Summary Table

| Category | Purpose |
|-----------|----------|
| 🧠 Git Basics | Track and commit changes |
| 🧩 Branching | Work on multiple features safely |
| 🦊 GitLab Remote | Host and collaborate online |
| ⚙️ SSH | Secure authentication |
| 🔄 CI/CD | Automate build and deploy |
| 📦 GLab CLI | Manage GitLab from terminal |

---

### ✨ Pro Tip
👉 Always run `git status` before committing — it shows what’s staged and what’s not.  
👉 Use branches for every new feature.  
👉 Commit often, with clear messages.  

---

### 🦊 Happy Coding on GitLab!
You now know every command needed to work confidently with **Git + GitLab** 🚀  
Keep experimenting, keep learning!





