# THM Walkthroughs

> **Breaking machines. Learning techniques. Building skills.**
>
> This repository is a living journal of my journey through **TryHackMe**, where every room is an opportunity to think like an attacker, investigate like a defender, and grow as a cybersecurity professional.

![GitHub Repo stars](https://img.shields.io/github/stars/r1tv1kx/THM_Walkthroughs?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/r1tv1kx/THM_Walkthroughs?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/r1tv1kx/THM_Walkthroughs?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/r1tv1kx/THM_Walkthroughs?style=for-the-badge)
![License](https://img.shields.io/github/license/r1tv1kx/THM_Walkthroughs?style=for-the-badge)

---

# Contents

- [Rooms](#rooms)
- [Welcome](#welcome)
- [What You'll Discover](#what-youll-discover)
- [The Methodology](#the-methodology)
- [Technologies & Tools](#technologies--tools)
- [Repository Structure](#repository-structure)
- [Why This Repository Exists](#why-this-repository-exists)
- [Learning Never Stops](#learning-never-stops)
- [Disclaimer](#disclaimer)
- [Contributing](#contributing)
- [About Me](#about-me)

---

# Rooms

| Room | Difficulty | Topics |
|---|---|---|
| [Basic Pentesting](rooms/Basic%20Pentesting.md) | Easy | Enumeration, Brute Forcing, SMB, Privilege Escalation |
| [Vulnversity](rooms/Vulnversity.md) | Easy | Enumeration, File Upload, SUID Privilege Escalation |
| [RootMe](rooms/rootme.md) | Easy | Web Enumeration, File Upload, Command Injection |
| [Simple CTF](rooms/Simple_CTF.md) | Easy | CVE Exploitation, Password Cracking, Privilege Escalation |
| [Hydra](rooms/Hydra.md) | Easy | Brute Forcing, Web Login Forms, SSH |
| [Pentesting Fundamentals](rooms/Pentesting%20Fundamentals.md) | Easy | Methodology, Ethics, Testing Scopes |
| [Crack the Hash — Level 1](rooms/Crack%20the%20hash%20Level%201.md) | Easy | Hash Identification, Hash Cracking |
| [Crack the Hash — Level 2](rooms/Crack%20the%20hash%20Level-2.md) | Medium | Hash Cracking, Custom Wordlists, Mangling Rules |
| [OhSINT](rooms/OhSINT.md) | Beginner | OSINT, Metadata Analysis, Wi‑Fi Mapping |
| [Tor for Beginners](rooms/Tor.md) | Beginner | Tor, Proxychains, Hidden Services |

---

# Welcome

Cybersecurity isn't learned by watching—it's learned by **breaking, fixing, failing, and trying again**.

This repository captures that journey.

Inside, you'll find detailed walkthroughs of **TryHackMe** rooms covering reconnaissance, service enumeration, web exploitation, and Linux privilege escalation — with Active Directory and Windows privilege escalation next on the roadmap (see [Learning Never Stops](#learning-never-stops)). Every challenge is documented with a focus on understanding the *why* behind each step—not just collecting flags.

Whether you're a beginner starting your cybersecurity journey or someone looking for another perspective on solving a room, I hope these notes help you learn something new.

---

# What You'll Discover

- Practical walkthroughs with clear explanations
- Real-world penetration testing methodology
- Enumeration techniques that uncover hidden attack surfaces (web, SMB, FTP, SSH)
- Web application exploitation, including file upload bypasses and CVE-based attacks
- Linux privilege escalation via SUID binaries, sudo misconfigurations, and weak credentials
- Password and hash cracking with Hydra, John the Ripper, and Hashcat
- OSINT and metadata analysis
- Scripts, commands, and useful one-liners
- Lessons learned from every challenge

---

# The Methodology

Every walkthrough follows a structured approach:

```text
Recon
   ↓
Enumeration
   ↓
Vulnerability Discovery
   ↓
Exploitation
   ↓
Privilege Escalation
   ↓
Root/User Flags
   ↓
Lessons Learned
```

The objective isn't just to solve the room—it's to understand the mindset behind every decision.

---

# Technologies & Tools

Tools you'll regularly see used throughout these walkthroughs:

- Nmap — port and service enumeration
- Gobuster / dirsearch / ffuf — directory and content discovery
- Hydra — credential brute forcing
- Burp Suite — intercepting and manipulating web requests
- John the Ripper / Hashcat — hash and key cracking
- smbclient — SMB share enumeration
- Netcat — reverse and bind shells
- GTFOBins — SUID/sudo privilege escalation research
- Bash / Python — scripting and one-off tooling

---

# Repository Structure

```text
THM_Walkthroughs/
│
├── rooms/
│   ├── Room Name.md
│   ├── Room Name.md
│   └── ...
│
└── README.md
```

Each walkthrough typically contains:

- Room Overview
- Reconnaissance
- Enumeration
- Exploitation
- Privilege Escalation
- Commands Used
- Screenshots
- Key Takeaways
- References

---

# Why This Repository Exists

This repository is more than a collection of notes.

It's a record of my progress as I continue exploring offensive security, documenting methodologies, and sharpening the skills required for real-world penetration testing.

Every room solved adds another technique.
Every mistake becomes another lesson.
Every walkthrough is another step forward.

---

# Learning Never Stops

Current areas of focus include:

- Active Directory attacks (BloodHound, CrackMapExec, Impacket)
- Windows privilege escalation (WinPEAS)
- Web application security
- Red team techniques
- Network security
- Capture The Flag challenges
- Offensive security methodology

As I continue learning, this repository will continue to grow.

---

# Disclaimer

All content in this repository is provided for **educational purposes only**.

These walkthroughs are intended for authorized labs and training environments such as TryHackMe. Never use these techniques against systems without explicit permission.

---

# Contributing

Have a better approach? Found a mistake? Want to share an alternative solution?

Contributions, suggestions, and discussions are always welcome.

---

# About Me

**Ritvik Singh**

Cyber Security Analyst • Penetration Tester • Security Research Enthusiast

---

> **"Every machine tells a story. Every exploit teaches a lesson. Every walkthrough is one more step toward mastering cybersecurity."**
