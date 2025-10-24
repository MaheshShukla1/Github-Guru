# 🪄 02 – Git Basics  

Welcome back, developer! 👋  
Now that you know **what Git is** and **why it matters**, it’s time to actually **use it like a pro**.  

This chapter is all about the **core Git commands** every developer lives on:  
`init`, `add`, `commit`, `status`, `log`, and `diff`.  

By the end, you’ll not just *know* Git — you’ll *feel it in your fingers*. 🧠⚡  

---

## ⚙️ 1. Installing Git (Windows / Mac / Linux)

Before you can Git things done — you need Git installed! 😎

### 🪟 Windows
1. Go to 👉 [git-scm.com/download/win](https://git-scm.com/download/win)
2. Download and run the setup.  
3. Accept all defaults (don’t overthink).  
4. Open **Git Bash** and run:

   ```bash
   git --version
   ```

✅ If you see something like `git version 2.xx.x`, you’re all set!

### 🍎 macOS

```bash
brew install git
```

Or, simply install **Xcode Command Line Tools**:

```bash
xcode-select --install
```

### 🐧 Linux (Debian/Ubuntu)

```bash
sudo apt update
sudo apt install git -y
```

### 🎯 Verify Installation

```bash
git --version
```

💡 _Pro Tip:_ Configure your identity once:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

This makes every commit traceable — your personal developer fingerprint. 🔍

## 🚀 2. `git init` — Create a New Repository

Imagine you’ve just started your next million-dollar project 💼 —  
to make Git start tracking it, run this inside your project folder:

```bash
git init
```

What happens:

- Git creates a hidden folder `.git/`
    
- It starts tracking all changes in that folder
    
- Your project just became a **version-controlled repository**

✅ You’ll see:

```swift
	Initialized empty Git repository in /path/to/project/.git/
```

💡 **Mental Model:**  
Think of `git init` as pressing **"Start Recording"** 🎥 on your project’s timeline.

---

## 📦 3. `git add` — Stage Your Changes

Git doesn’t auto-track every change you make.  
You decide _which_ changes are worth saving using `git add`.

```bash
git add <file-name>
```

or to add _everything_:

```bash
git add .
```

💡 **Staging Area = The “Ready to Commit” Box**

Example:

```bash
echo "console.log('Hello World');" > app.js
git add app.js
```

✅ Git has now “noticed” that file and marked it for the next snapshot.

🧠 **Pro Tip:**  
Always double-check what you’re adding with:

```bash
git status
```

## 💾 4. `git commit` — Save Your Code Snapshot

Once changes are staged, commit them to permanently save in Git’s history:

```bash
git commit -m "Added app.js with Hello World script"
```


💡 Think of a commit as a checkpoint in your project timeline.
If your code breaks later, you can always jump back to this commit.

### 🧠 Commit Message Wisdom:

Good messages = good project health.  
Bad messages = chaos in production 😬

✅ **Good:**

```bash
git commit -m "Add user login validation"
```

❌ **Bad:**

```bash
git commit -m "changes"
```

🪄 _Rule of thumb:_

> Every commit should tell a mini-story of progress.

## 🔍 5. `git status` — Check What’s Going On

Before you commit, always run:

```bash
git status
```

This shows:

- Which files are **tracked**
    
- Which ones are **modified**
    
- Which ones are **staged**
    
- Which ones are **untracked**
    

Example output:

```yaml
On branch main
Changes to be committed:
  new file:   app.js
Changes not staged for commit:
  modified:   index.html
```

💡 **Why it matters:**  
Think of `git status` like your daily project dashboard. Don’t fly blind. 🧭

## 🕒 6. `git log` — View Commit History

Want to see how your project evolved?  
Run:

```bash
git log
```

You’ll see something like:

```sql
commit a1b2c3d4e5f6g7
Author: Mahesh Shukla <you@example.com>
Date:   Fri Oct 25 18:00:00 2025 +0530

    Added app.js with Hello World script
```

💡 Too long? Simplify it:

```bash
git log --oneline
```

Output:

```sql
a1b2c3d Initial commit
c4d5e6f Added Hello World script
```

🎯 _Use this to quickly navigate your version history and identify stable states._

---

## ⚔️ 7. `git diff` — See What’s Changed

Before committing, always check what exactly changed:

```bash
git diff
```

This shows the **line-by-line difference** between your last commit and your current edits.

Example:

```diff
+ console.log("Hello Git!");
- console.log("Hello World!");
```

🧠 **Pro Tip:**  
Run this before `git add` to avoid committing accidental changes.  
It’s your built-in **error radar** 🛫

---

## 🧩 Real-World Example: Your First Git Flow

Let’s tie everything together 👇

```bash
# Step 1: Initialize repo
git init

# Step 2: Create a file
echo "Hello Git!" > hello.txt

# Step 3: Stage it
git add hello.txt

# Step 4: Commit it
git commit -m "Initial commit with hello.txt"

# Step 5: Modify file
echo "Learning Git feels awesome!" >> hello.txt

# Step 6: Check changes
git diff

# Step 7: Stage + commit again
git add hello.txt
git commit -m "Updated hello.txt with learning message"

# Step 8: Review your history
git log --oneline
```


🧠 You’ve just performed a **complete Git workflow** from scratch —  
the same foundation used by Google, Netflix, and every major tech company. 🚀

---

## 🎯 Summary Cheatsheet

|Command|Purpose|Analogy|
|---|---|---|
|`git init`|Start a new repo|Press “Record”|
|`git add`|Stage changes|Put items in cart|
|`git commit`|Save snapshot|Checkout and store receipt|
|`git status`|Check repo state|Look at your to-do list|
|`git log`|View commit history|Read your timeline|
|`git diff`|Compare changes|Spot what’s new or broken|

---

## 🧠 Brain Hack

- Every commit = a checkpoint in your project’s time machine
    
- `add` before `commit` = _pack before you save_
    
- `status` + `diff` = your debugging radar
    
- `log` = your memory lane
    

The more you visualize these metaphors, the faster Git feels **natural**. 💪

---

## 🪄 Next Up: “Branching Magic” 🌳

In the next chapter, you’ll learn:

> How to use `git branch`, `checkout`, and `merge`  
> to experiment fearlessly — just like parallel universes in your code.

🧭 Continue your journey → 03-Git-Branching

✍️ Written with ❤️ by [Mahesh Shukla](https://github.com/MaheshShukla1) — keep committing, keep growing!
