# 🪟 Windows Commands Cheat Sheet (CMD)

## 📁 File & Directory

`dir                     # List contents of directory   cd <dir>                # Change directory   cd ..                   # Go up one directory   mkdir <dir>             # Create a new directory   del <file>              # Delete a file   rmdir <dir>             # Remove a directory   copy <src> <dest>       # Copy files   move <src> <dest>       # Move or rename files   type <file>             # Display contents of a file`  

## 📄 File Viewing & Editing

`type <file>             # Display file content   more <file>             # Paginate file content   notepad <file>          # Open file in Notepad`  

## 🧮 System Info

`systeminfo              # Detailed system info   hostname                # Computer name   ver                     # OS version   tasklist                # Running processes   taskkill /PID <pid>     # Kill process`  

## 👤 User Management

`net user                        # List users   net user <username> /add        # Add a user   net user <username> /delete     # Delete a user   net localgroup administrators <username> /add  # Add to admin group`  

## 🔐 Permissions

`icacls <file>           # View or modify file permissions   takeown /F <file>       # Take ownership of file`  

## 🌐 Networking

`ipconfig                # Show IP configuration   ipconfig /all           # Detailed network info   ping <host>             # Ping a host   tracert <host>          # Trace route to host   netstat -an             # Active connections`  

## 🧰 System Tools

`chkdsk                  # Check disk for errors   sfc /scannow            # System File Checker   diskpart                # Disk partition tool   shutdown /s /t 0        # Shutdown immediately   shutdown /r /t 0        # Restart immediately`  

## 📜 Useful Shortcuts

cmd

CopyEdit

`cls                     # Clear screen   exit                    # Exit CMD   help                    # List help for commands   <command> /?            # Help for a specific command`  

## 💡 Tips

- Run CMD as Administrator for full access.
    
- Use `PowerShell` for more advanced scripting and features.