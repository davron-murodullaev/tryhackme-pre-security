# SECTION 5: Windows Fundamentals

## 1. Objectives
In this section you will learn:
- **Windows Command Prompt:** basic file and network commands  
- **PowerShell Basics:** scripting, execution policy, cmdlets  
- **User & System Management:** listing and creating users, services  
- **Networking Tools:** ipconfig, netstat, firewall basics  

## 2. Key Commands & Concepts

| Command / Concept                 | Description                                              |
|-----------------------------------|----------------------------------------------------------|
| `dir`                             | List directory contents                                  |
| `cd`                              | Change current directory                                 |
| `ipconfig /all`                   | Display network adapter configuration                    |
| `netstat -an`                     | Show active connections and listening ports              |
| `Get-LocalUser`                   | List local user accounts (PowerShell)                    |
| `New-LocalUser -Name <User> -Pwd $pw` | Create new user in PowerShell                       |
| `Set-ExecutionPolicy RemoteSigned`| Allow running local scripts in PowerShell                |
| Windows Firewall (Control Panel)  | GUI for managing inbound/outbound rules                  |

## 3. Hands-On Example

1. **Task:** List existing users and create a new administrator user  
2. **Steps (PowerShell):**  
   ```powershell
   # List all local users
   Get-LocalUser

   # Create a secure password object
   $pw = Read-Host -AsSecureString

   # Create new user 'pentester'
   New-LocalUser -Name pentester -Password $pw -FullName "Pentest User"

   # Add user to Administrators group
   Add-LocalGroupMember -Group Administrators -Member pentester

   # Verify creation
   Get-LocalUser -Name pentester
