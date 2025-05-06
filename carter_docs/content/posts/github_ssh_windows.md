
---
title: Setup GitHub With SSH (Windows)
date: 2025-05-06
author: Carter Keel
description: 
isStarred: false
---

Follow these steps to generate and use SSH keys on Windows for secure access to remote servers and services like GitHub, GitLab, or your own SSH server.

---

## ✅ Prerequisites

- Windows 10 or later
    
- Access to **Command Prompt** or **PowerShell**
    
- [Git for Windows](https://git-scm.com/download/win) (includes `ssh` and `ssh-keygen`)
    

---

## 1. 🧰 Generate a New SSH Key

Open your terminal and run:

`ssh-keygen -t ed25519 -C "your_email@example.com"`

If your system doesn’t support `ed25519`, use:

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

### When prompted:

- **Save location**: Press `Enter` to accept the default (`C:\Users\<YourUser>\.ssh\id_ed25519`)
    
- **Passphrase** (optional but recommended): Enter a secure passphrase
    

---

## 2. 🔑 Add Your SSH Key to the Agent

Start the SSH agent

`eval $(ssh-agent -s)`

Add your private key to the agent:

`ssh-add ~/.ssh/id_ed25519`

> 💡 Replace `id_ed25519` with your key file if you named it differently.

---

## 3. 📋 Add Your Public Key to the Remote Server

Copy your public key to clipboard:

`clip < ~/.ssh/id_ed25519.pub`

Then, add it to:

- **GitHub**: [Settings → SSH and GPG keys](https://github.com/settings/keys)
    
- **GitLab**: [Preferences → SSH Keys](https://gitlab.com/-/profile/keys)
    
- **Remote Server**: Add the contents to the `~/.ssh/authorized_keys` file
    

---

## 4. 🧪 Test Your Connection

Test the connection:

`ssh -T git@github.com`

If successful, you'll see a welcome message:

> Hi `username`! You've successfully authenticated.
