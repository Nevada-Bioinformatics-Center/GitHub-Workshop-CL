# Hands-On Git Command Line Tutorial
By the end, you'll have a local Git repository, make some changes, and commit them—all from your terminal.

## Prerequisites
- A terminal.
    
    -**Mac:** Terminal application is fine.
    
    -**Windows (10 or newer):** Open PowerShell or Windows Command Prompt in administrator mode by right-clicking and selecting “Run as administrator”, enter the command, then restart your machine. 
    `wsl --install --distribution ubuntu`


## Step 1: Install and Check Git
1. **Check if Git is installed:**
```bash
git --version
```
- If installed, you'll see something like `git version 2.39.2`

2. **If not installed:**
- **For Mac**: Install using Homebrew:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
brew install git
```
- **For Windows**: Download from [git-scm.com](https://git-scm.com/download/win)


## Step 2: Navigate to a Good Location
1. **Open your terminal.**
2. **Go to your Documents folder:**
```bash
# For Mac/Linux:
cd ~/Documents

# For Windows:
cd %USERPROFILE%\Documents
```
3. **Create and enter a folder for your projects:**
```bash
mkdir GitProjects
cd GitProjects
```

## Step 3: Create Your Project
1. **Create a new folder for this practice:**

```bash
mkdir git-practice
cd git-practice
```

2. **Initialize a Git repository:**

```bash
git init
```
- You’ll see: `Initialized empty Git repository in .../git-practice/.git/`.

## Step 4: Create and Track a File
1. **Create a text file:**

```bash
echo Hello, Git! > hello.txt
```

2. **Check the status:**

```bash
git status
```
- You’ll see `hello.txt` listed as an untracked file.

## Step 5: Stage and Commit Changes
1. **Stage the file:**

```bash
git add hello.txt
```
- This tells Git to track `hello.txt`.
2. **Commit the file:**

```bash
git commit -m "Add hello.txt with a greeting"
```

- This saves your change with a message.
3. **Check status again:**

```bash
git status
```

- It should say “nothing to commit, working tree clean.”

## Step 6: Make a Change
1. **Edit the file:**
- Add a new line manually (open `hello.txt` in any text editor) or use:

```bash
echo Learning Git is fun! >> hello.txt
```

2. **Check the status:**

```bash
git status
```

- You’ll see `hello.txt` modified.
3. **Stage and commit again:**

```bash
git add hello.txt
git commit -m "Update hello.txt with a new line"
```


## Step 7: View Your History
1. **See your commits:**

```bash
git log
```


- Lists all commits with messages, dates, and more.
- Press `q` to exit.

## Bonus: Connect to GitHub
1. **Create a repository on GitHub** (online, call it `git-practice`).
2. **Link your local repo:**

```bash
git remote add origin <your-repo-url> # Example: https://github.com/username/git-practice.git
git branch -M main
git push -u origin main
```

3. **Check GitHub—your commits are live!**

## What’s Next?
- You’ve just used the command line to manage a Git project!
- In the workshop, we’ll switch to GitHub Desktop to see how it simplifies these steps.
- Questions? Experiment with `git status` or `git log` again!