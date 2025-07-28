# SECTION 1: Introduction to Cyber Security

## 1. Objectives
In this section you will learn:
- **Offensive Security:** basic principles of simulating an attacker to find vulnerabilities
- **Defensive Security:** fundamental ideas for protecting systems and detecting intrusions
- **Careers in Cyber:** common job roles, paths and skill requirements

## 2. Key Commands & Concepts

| Command / Concept         | Description                                              |
|---------------------------|----------------------------------------------------------|
| Offensive Security        | Simulating hacker tactics to identify weaknesses         |
| Defensive Security        | Techniques and tools to block, log, and respond to attacks|
| `nmap -sC -sV TARGET_IP`  | Default script scan + version detection on target host   |
| `gobuster -u URL -w WORDLIST dir` | Brute-forces directories/pages on a web server       |

## 3. Hands-On Example

1. **Task:** Hack FakeBank web app to find a hidden transfer page  
2. **Steps:**  
   ```bash
   # 1. Start the VM and split view in TryHackMe
   # 2. Open terminal, run Gobuster:
   gobuster -u http://fakebank.thm -w wordlist.txt dir

   # 3. Observe output, find /bank-transfer (Status 200)
   # 4. Browse to http://fakebank.thm/bank-transfer
   # 5. Transfer $2000 from account 2276 to 8881
