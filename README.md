Git Instructions (VS Code → GitHub)
=====================================
1.first connect your git account to VS-CODE
Sign in to GitHub in VS Code
Option 1: Easiest way (built-in)
In VS Code sidebar, click Source Control icon (it looks like a branch icon)
At the top → click “Sign in to GitHub”
A browser window will open → click Authorize Visual Studio Code
=====================
Option 2: Use Personal Access Token (manual way)
If you want to push via terminal (first time GitHub login):
Go to GitHub → click your profile → Settings → Developer settings → Personal access tokens → Tokens (classic)
Click Generate new token (classic)
Select scopes:
✅ repo
✅ workflow
Copy the token (keep it safe!)
Later, when you push from VS Code, it will ask:
Username: your_github_username
Password: your_token_here
Paste the token (not your password).
====================================
STEP 5 — Connect your local repo to GitHub
1️⃣ Go to GitHub → click New Repository
Name it something like my-static-website
Don’t initialize with README (you already have files locally)
Click Create repository
2️⃣ Copy the HTTPS URL (looks like this):
https://github.com/your-username/my-static-website.git
====================================
Check if Git is installed:
Open VS Code terminal (Ctrl + ~ or View → Terminal) and run:
git --version
=================================
Initialize Git in your project folder:
git init
=================================
Add GitHub remote:
git remote add origin https://github.com/your-username/my-static-website.git
====================================================
Add, Commit, and Push
Stage & commit files:
git add .
git commit -m "Initial commit - static website with buildspec and appspec"
Push to GitHub:
git branch -M main
git push -u origin main
====================================
⚠️ Git Line Ending Warning (LF ↔ CRLF)
On Windows, Git may show warnings:
warning: LF will be replaced by CRLF
This is normal.
Recommended for Linux deployment:
git config --global core.autocrlf input
