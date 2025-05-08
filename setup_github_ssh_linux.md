---
date: '2025-05-01T17:42:19-05:00'
draft: false
title: 'GitHub SSH Setup (Linux)'
---

Follow these steps to securely connect to GitHub using SSH on a Linux system.

## 📌 Prerequisites

- A GitHub account
    
- Git installed (`sudo apt install git`)
    
- OpenSSH client installed (`sudo apt install openssh-client`)
    

---

## 🔑 Step 1: Check for Existing SSH Keys

`ls -al ~/.ssh`

Look for files like `id_rsa.pub` or `id_ed25519.pub`. If they exist, you might already have an SSH key.

---

## 🛠️ Step 2: Generate a New SSH Key

`ssh-keygen -t ed25519 -C "your_email@example.com"`

If you're using an older system that doesn't support Ed25519:

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

- When prompted to "Enter a file in which to save the key," press Enter to accept the default.
    
- Set a secure passphrase (optional, but recommended).
    

---

## 📂 Step 3: Add Your SSH Key to the SSH Agent

Start the SSH agent:

`eval "$(ssh-agent -s)"`

Add your SSH key:

`ssh-add ~/.ssh/id_ed25519`

> Replace `id_ed25519` with your actual key file if you used a different name.

---

## 📋 Step 4: Copy SSH Key to Clipboard

If you have `xclip` installed:

`xclip -selection clipboard < ~/.ssh/id_ed25519.pub`

Or use:

`cat ~/.ssh/id_ed25519.pub`

Then manually copy the output.

---

## 🌐 Step 5: Add SSH Key to GitHub

1. Go to [GitHub SSH settings](https://github.com/settings/keys)
    
2. Click **New SSH Key**
    
3. Paste your public key
    
4. Give it a descriptive title
    
5. Click **Add SSH key**
    

---

## ✅ Step 6: Test Your SSH Connection

`ssh -T git@github.com`

You should see a message like:

`Hi your_username! You've successfully authenticated...`