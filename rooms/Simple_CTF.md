# Simple CTF - TryHackMe Walkthrough
<img width="270" alt="Screenshot 2025-06-17 at 2 44 52 PM" src="https://github.com/user-attachments/assets/5ed4d768-9916-4a0e-85f0-8ea6fca1b284" />

Simple CTF on TryHackMe is a beginner-friendly room that teaches basic enumeration, exploitation, and privilege escalation techniques. It involves capturing user and root flags using tools like `nmap`, `gobuster`, and `hydra`.

---

## Step 1: Nmap Scan

We begin by scanning the given IP address to identify open ports and services.

![Nmap Scan Result](https://github.com/user-attachments/assets/d6cf96ba-d9c5-4a12-8cc8-21d4f0344b95)

📌 **Task:** *How many services are running under port 1000?*  
Inspect the results to answer.

---

## Step 2: Directory Enumeration

Use `dirsearch` to find hidden directories:

```bash
python3 dirsearch.py -u http://10.10.248.5
```
<img width="548" alt="Screenshot 2025-06-17 at 2 32 10 PM" src="https://github.com/user-attachments/assets/b892e796-34fd-4aec-a2d0-10915d9e925b" />

We discover:

```
http://10.10.248.5/simple/
```

Visiting this page reveals: ```This site is powered by CMS Made Simple version 2.2.8```

## Step 3: CVE Discovery
You can manually Google known vulnerabilities for CMS Made Simple 2.2.8.

Alternatively, use exploit scripts. For example:
```
vim 46635.py
```
<img width="547" alt="Screenshot 2025-06-17 at 2 33 02 PM" src="https://github.com/user-attachments/assets/a0c2dae0-46da-46d0-861f-686edc95f9f6" />

You can find the CVE manually or by using Exploit-DB or searchsploit.

## Step 4: Exploitation
We exploit the CMS using a script (e.g., ```exploit.py```).

After running the script and using a password cracking method (e.g., with ```rockyou.txt```), we discover the password:
```
secret
```
## Step 5: SSH Access
Use the credentials to log in via SSH:
```
ssh mitch@<target-ip> -p 2222
```
<img width="396" alt="Screenshot 2025-06-17 at 2 40 40 PM" src="https://github.com/user-attachments/assets/32045a71-050a-47c4-a456-96c274d21e47" />

Read the user flag:
```
nano user.txt
```
Also, you will discover the name of the second user:
```
sunbath
```
## Step 6: Privilege Escalation
Check the current user’s sudo privileges:
```
sudo -l
```
<img width="358" alt="Screenshot 2025-06-17 at 2 41 39 PM" src="https://github.com/user-attachments/assets/09c09c60-dc44-40f6-9136-3590233c5059" />

We see that we can run vim with sudo.
Use the following command to escalate privileges:
```
sudo vim -c ':!/bin/sh'
```
<img width="339" alt="Screenshot 2025-06-17 at 2 42 37 PM" src="https://github.com/user-attachments/assets/bb55c4f7-d608-4127-936c-58bdd3beabea" />

Once you have root access, read the ```root.txt``` file to capture the root flag.
