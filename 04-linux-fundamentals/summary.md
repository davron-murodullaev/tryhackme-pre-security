# SECTION 4: Linux Fundamentals

## 1. Objectives
In this section you will learn:
- **Basic Shell Usage:** navigating the filesystem and handling files  
- **Permissions & Ownership:** controlling access with `chmod` and `chown`  
- **Process Management:** listing, monitoring, and terminating processes  
- **Package Management:** installing and updating software with `apt`  
- **User & Group Management:** creating users and assigning groups

## 2. Key Commands & Concepts

| Command / Concept                | Description                                                   |
|----------------------------------|---------------------------------------------------------------|
| `ls -la`                         | List all files (including hidden) with detailed information   |
| `cd /path/to/dir`                | Change current working directory                             |
| `chmod 755 file`                 | Set owner rwx, group/others rx permissions                    |
| `chown user:group file`          | Change file owner and group                                  |
| `ps aux`                         | Display all running processes                                 |
| `kill <PID>`                     | Terminate a process by its PID                                |
| `sudo apt update`                | Refresh package lists (Debian/Ubuntu)                         |
| `sudo apt install <package>`     | Install a package                                            |
| `sudo useradd -m <username>`     | Create a new user with home directory                         |
| `sudo usermod -aG sudo <user>`   | Add an existing user to the `sudo` group                      |

## 3. Hands-On Example

1. **Task:** Create a new user and grant sudo privileges  
2. **Steps:**  
   ```bash
   # Create user 'hacker'
   sudo useradd -m hacker

   # Set a password
   sudo passwd hacker

   # Add to sudo group
   sudo usermod -aG sudo hacker

   # Verify the user info
   id hacker
   ps aux | grep hacker
