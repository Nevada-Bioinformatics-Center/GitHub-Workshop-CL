# Hands-On Git Command Line Tutorial
Welcome to the basics of Git using the command line! By the end, you'll have a local Git repository, make some changes, and commit them—all from your terminal.

## Prerequisites
- Git installed (run `git --version` to check).
- A terminal: Git Bash (Windows) or Terminal (Mac/Linux).

## Step 1: Set Up Your Environment
1. **Open your terminal.**
2. **Create a new folder for your project:**

```
mkdir git-practice
cd git-practice
```

3. **Initialize a Git repository:**

```
git init
```
- You’ll see: `Initialized empty Git repository in .../git-practice/.git/`.

## Step 2: Create and Track a File
1. **Create a text file:**

```
echo "Hello, Git!" > hello.txt
```

2. **Check the status:**

```
git status
```
- You’ll see `hello.txt` listed as an untracked file.

## Step 3: Stage and Commit Changes
1. **Stage the file:**

```
git add hello.txt
```
- This tells Git to track `hello.txt`.
2. **Commit the file:**

```
git commit -m "Add hello.txt with a greeting"
```

- This saves your change with a message.
3. **Check status again:**

```
git status
```

- It should say “nothing to commit, working tree clean.”

## Step 4: Make a Change
1. **Edit the file:**
- Add a new line manually (open `hello.txt` in any text editor) or use:

```
echo "Learning Git is fun!" >> hello.txt
```

2. **Check the status:**

```
git status
```

- You’ll see `hello.txt` modified.
3. **Stage and commit again:**

```
git add hello.txt
git commit -m "Update hello.txt with a new line"
```


## Step 5: View Your History
1. **See your commits:**

```
git log
```


- Lists all commits with messages, dates, and more.
- Press `q` to exit.

## Bonus: Connect to GitHub (Optional)
1. **Create a repository on GitHub** (online, call it `git-practice`).
2. **Link your local repo:**

```
git remote add origin <your-repo-url>
git branch -M main
git push -u origin main
```

3. Check GitHub—your commits are live!

## What’s Next?
- You’ve just used the command line to manage a Git project!
- In the workshop, we’ll switch to GitHub Desktop to see how it simplifies these steps.
- Questions? Experiment with `git status` or `git log` again!