---
date: '2025-05-01T17:42:19-05:00'
draft: false
title: 'GitHub SSH Setup (Linux)'
---

✅ Prerequisites
A Linux system (Ubuntu, Debian, Fedora, Arch, etc.)

Access to a terminal

OpenSSH installed (usually preinstalled)

1. 🧰 Generate a New SSH Key
In your terminal, run:

ssh-keygen -t ed25519 -C "your_email@example.com"
If ed25519 is not supported, use:

ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
When prompted:
Save location: Press Enter to use the default (/home/youruser/.ssh/id_ed25519)

Passphrase: (optional but recommended) Enter a secure passphrase

2. 🔑 Add Your SSH Key to the SSH Agent
Start the agent (if it’s not running):

eval "$(ssh-agent -s)"
Add your key:

ssh-add ~/.ssh/id_ed25519
💡 Replace id_ed25519 if your key has a different filename.

3. 📋 Add Your Public Key to the Remote Service
Copy your public key to the clipboard:

cat ~/.ssh/id_ed25519.pub
Then copy the output manually and add it to:

GitHub: Settings → SSH and GPG keys

GitLab: Preferences → SSH Keys

Remote server: Paste into ~/.ssh/authorized_keys

4. 🧪 Test the Connection
Run the following to test your SSH setup:

ssh -T git@github.com
You should see a message like:

Hi yourusername! You've successfully authenticated.

🔄 Optional: Use a Specific Key for Git
If you're using a custom-named key:

git config --global core.sshCommand "ssh -i ~/.ssh/custom_key"
