
# 🐙 Git & GitHub Cheat Sheet

## 🔧 Git Configuration
```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list
```

## 📁 Create & Clone
```bash
git init                    # Initialize a new repo
git clone <url>            # Clone an existing repo
```

## 📄 Basic Workflow
```bash
git status                 # Show changed files
git add <file>             # Stage a file
git add .                  # Stage all changes
git commit -m "message"    # Commit with a message
git push                   # Push to remote repo
git pull                   # Pull latest changes
```

## 🌿 Branching
```bash
git branch                 # List branches
git branch <name>          # Create new branch
git checkout <name>        # Switch branch
git checkout -b <name>     # Create & switch
git merge <name>           # Merge a branch
```

## 🧹 Undo & Reset
```bash
git restore <file>         # Undo changes in working directory
git reset <file>           # Unstage a file
git reset --hard           # Reset everything to last commit
```

## 📌 Stashing
```bash
git stash                  # Save changes
git stash pop              # Reapply stashed changes
git stash list             # Show stash list
```

## 🔍 Logs & Diffs
```bash
git log                    # View commit history
git log --oneline          # Condensed log
git diff                   # Show changes
```

## 🌐 Remotes
```bash
git remote -v              # Show remotes
git remote add origin <url>  # Add remote
git push -u origin main    # Push and set upstream
```

## 🔑 GitHub Authentication
- Use **SSH keys** or **GitHub CLI** for authentication.
```bash
ssh-keygen -t ed25519 -C "you@example.com"
gh auth login              # GitHub CLI login
```

## 🛠️ Miscellaneous
```bash
git tag <tagname>          # Create a tag
git fetch --all            # Fetch all remotes
git cherry-pick <hash>     # Apply a specific commit
```
