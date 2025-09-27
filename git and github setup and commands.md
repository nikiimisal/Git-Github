# 🚀 Git Setup & Workflow Guide & some commands


## 📊 Git &Github Workflow Diagram
![]()

Above diagram shows:

- **Working Directory** → where you edit files  
- **Staging Area (Index)** → use `git add <file>` to stage changes  
- **Local Repository (HEAD)** → use `git commit -m "message"` to commit locally  
- **Remote Repository (Github)** → use `git push` to upload to GitHub  


<h1>Quick Flow</h1>
1. Git install<br>
2. Create a account on github<br>
3. Create a folder<br>
       nikhil workspace<br>
           |
           |-- git
                |--  git bash
                      |
                      |-- code . ; exit

4. Inside VS code<br>
5. Index.html ,login.html<br>
6. Open terminal --> powershell --> git bash<br>
7. git init<br>
8. ls -a<br>
9. Authentaction<br>
<br>
    git config --global user.name "Your Name"<br>
    git config --global user.email "Your email"<br>
    git config --global  --list<br>

10. git status -s<br>
11. git add.
12. git status -s
13. git commit -m "added"
14. git status -s
15. git logs
    git logs --oneline
16. Create repo on github
17. git remote add orgin <url>
    git remote rm origin
18. Come to the terminal --> and past
19. git remote -v
20. git push -u origin master

<h1>Git Status</h1>





<h1>Git and Github Setup</h1>

<h2>🔧 Step 1: Install Git </h2>

<h4>On Windows </h4>

1. Download from https://git-scm.com/download/win.
   
2. Install with default options (make sure “Add Git to PATH” is selected).
   
3. Verify installation:

4. git --version

<h4>On Linux (Ubuntu/Debian)</h4>

• sudo apt update <br>
• sudo apt install git -y <br>
• git --version <br>

<h4>On macOS</h4>

• brew install git <br>
• git --version <br>
 
 <h2> Step 2: Configure Git (one-time only) </h2>
 
➼ Set your Git username & email (must match your GitHub account email for commits to show): <br>

➼ git config --global user.name "Your Name" <br>

➼ git config --global user.email "your-email@example.com" <br>

➼ Check config: <br>

➼ git config --list 
 
  <h2>Step 3: Initialize Git in Your VS Code Project </h2>
  
‣ Open VS Code → Terminal inside your project folder:  <br>

‣ cd path/to/your/project  <br>

‣ git init 
 
  <h2>Step 4: Add & Commit Files </h2>
• git add . <br>

• git commit -m "Initial commit" <br>

• This stages all files and commits them (preserving folder/file sequence). <br>
 
  
  <h2>Step 5: Create Repository on GitHub </h2>
1. Go to GitHub. <br>

2. Click New Repository → name it (e.g., my-project). <br>

3. Don’t initialize with README (since you already have files locally). <br>
 
  <h2>Step 6: Connect Local Project to GitHub</h2> 

Copy repo link (HTTPS or SSH). Example (HTTPS): <br>

git remote add origin https://github.com/username/my-project.git <br>
 
  <h2>Step 7: Push to GitHub</h2> 

git branch -M main      # make sure branch name is 'main' <br>

git push -u origin main <br>

Now your project is on GitHub with the same file/folder structure as in VS Code  <br>       
 
  <h2>Step 8: Verify</h2> 
  
• Open your GitHub repo in the browser → You’ll see all files in the same sequence. <br>

• From now on, just do: <br>

• git add . <br>

• git commit -m "Your changes" <br>

• git push <br>















