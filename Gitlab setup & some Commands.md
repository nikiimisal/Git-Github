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




