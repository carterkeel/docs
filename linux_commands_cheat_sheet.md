
# 🐧 Linux Commands Cheat Sheet

## 📂 File & Directory
```bash
ls                      # List directory contents
ls -l                   # Long listing format
cd <dir>                # Change directory
pwd                     # Print working directory
mkdir <dir>             # Create directory
rm <file>               # Delete file
rm -r <dir>             # Delete directory
cp <src> <dest>         # Copy file or directory
mv <src> <dest>         # Move or rename
touch <file>            # Create an empty file
find . -name "*.txt"    # Find files
```

## 📄 File Viewing & Editing
```bash
cat <file>              # View file content
less <file>             # View file page by page
head <file>             # First 10 lines
tail <file>             # Last 10 lines
nano <file>             # Edit file with Nano
vim <file>              # Edit file with Vim
```

## 🧮 System Info
```bash
uname -a                # System info
top                     # Real-time process monitor
htop                    # Interactive process viewer
df -h                   # Disk usage
du -sh *                # Directory sizes
free -h                 # RAM usage
uptime                  # System uptime
whoami                  # Current user
```

## 👤 User Management
```bash
adduser <username>      # Add user
passwd <username>       # Change password
su - <username>         # Switch user
id                      # Show current UID/GID
who                     # Who is logged in
```

## 🔐 Permissions
```bash
chmod +x <file>         # Make file executable
chmod 755 <file>        # Set permissions
chown user:group <file> # Change owner
```

## 📦 Package Management

### Debian/Ubuntu
```bash
sudo apt update         # Update repo list
sudo apt upgrade        # Upgrade packages
sudo apt install <pkg>  # Install package
sudo apt remove <pkg>   # Remove package
```

### RedHat/CentOS
```bash
sudo yum install <pkg>
sudo dnf install <pkg>
```

## 🌐 Networking
```bash
ping <host>             # Ping host
ifconfig                # Network interfaces
ip a                    # Show IP addresses
curl <url>              # Fetch web content
wget <url>              # Download files
```

## 📜 Process Management
```bash
ps aux                  # Show running processes
kill <pid>              # Kill process
kill -9 <pid>           # Force kill
```

## 🧰 Useful Shortcuts
```bash
Ctrl + C                # Cancel command
Ctrl + D                # Logout/EOF
Ctrl + Z                # Suspend
!!                      # Repeat last command
history                 # Command history
```
