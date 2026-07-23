<div align="center">

# THM Walkthroughs

### Breaking machines. Learning techniques. Building skills.

*A living journal of my journey through **TryHackMe** — where every room is a chance to think like an attacker, investigate like a defender, and grow as a cybersecurity professional.*

![GitHub Repo stars](https://img.shields.io/github/stars/r1tv1kx/THM_Walkthroughs?style=for-the-badge&color=e05d44)
![GitHub forks](https://img.shields.io/github/forks/r1tv1kx/THM_Walkthroughs?style=for-the-badge&color=orange)
![GitHub last commit](https://img.shields.io/github/last-commit/r1tv1kx/THM_Walkthroughs?style=for-the-badge&color=yellow)
![GitHub repo size](https://img.shields.io/github/repo-size/r1tv1kx/THM_Walkthroughs?style=for-the-badge&color=brightgreen)
![License](https://img.shields.io/github/license/r1tv1kx/THM_Walkthroughs?style=for-the-badge&color=blue)

`Nmap` · `Burp Suite` · `Gobuster` · `Hydra` · `John the Ripper` · `Hashcat` · `Netcat` · `Bash` · `Python`

</div>

<br>

## 🧭 Contents

- [🧩 Rooms](#-rooms)
- [👋 Welcome](#-welcome)
- [🔍 What You'll Discover](#-what-youll-discover)
- [🗺️ The Methodology](#-the-methodology)
- [🛠️ Technologies & Tools](#-technologies--tools)
- [📁 Repository Structure](#-repository-structure)
- [💭 Why This Repository Exists](#-why-this-repository-exists)
- [🚀 Learning Never Stops](#-learning-never-stops)
- [⚠️ Disclaimer](#-disclaimer)
- [🤝 Contributing](#-contributing)
- [👤 About Me](#-about-me)

<br>

## 🧩 Rooms

| Room | Difficulty | Topics |
|---|---|---|
| [Basic Pentesting](rooms/Basic%20Pentesting.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | Enumeration, Brute Forcing, SMB, Privilege Escalation |
| [Vulnversity](rooms/Vulnversity.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | Enumeration, File Upload, SUID Privilege Escalation |
| [RootMe](rooms/rootme.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | Web Enumeration, File Upload, Command Injection |
| [Simple CTF](rooms/Simple_CTF.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | CVE Exploitation, Password Cracking, Privilege Escalation |
| [Hydra](rooms/Hydra.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | Brute Forcing, Web Login Forms, SSH |
| [Pentesting Fundamentals](rooms/Pentesting%20Fundamentals.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | Methodology, Ethics, Testing Scopes |
| [Crack the Hash — Level 1](rooms/Crack%20the%20hash%20Level%201.md) | ![Easy](https://img.shields.io/badge/-Easy-brightgreen) | Hash Identification, Hash Cracking |
| [Crack the Hash — Level 2](rooms/Crack%20the%20hash%20Level-2.md) | ![Medium](https://img.shields.io/badge/-Medium-yellow) | Hash Cracking, Custom Wordlists, Mangling Rules |
| [OhSINT](rooms/OhSINT.md) | ![Beginner](https://img.shields.io/badge/-Beginner-blue) | OSINT, Metadata Analysis, Wi‑Fi Mapping |
| [Tor for Beginners](rooms/Tor.md) | ![Beginner](https://img.shields.io/badge/-Beginner-blue) | Tor, Proxychains, Hidden Services |

<br>

## 👋 Welcome

Cybersecurity isn't learned by watching — it's learned by **breaking, fixing, failing, and trying again**. This repository captures that journey.

Inside, you'll find detailed walkthroughs of **TryHackMe** rooms covering reconnaissance, service enumeration, web exploitation, and Linux privilege escalation — with Active Directory and Windows privilege escalation next on the roadmap (see [🚀 Learning Never Stops](#-learning-never-stops)). Every challenge is documented with a focus on understanding the *why* behind each step, not just collecting flags.

Whether you're just starting your cybersecurity journey or looking for another perspective on solving a room, I hope these notes help you learn something new.

<br>

## 🔍 What You'll Discover

<table>
<tr>
<td width="50%" valign="top">

**🕵️ Recon & Enumeration**
- Web, SMB, FTP, and SSH service enumeration
- Enumeration techniques that uncover hidden attack surfaces
- OSINT and metadata analysis

**💥 Exploitation**
- Web application exploitation
- File upload bypasses and CVE-based attacks

</td>
<td width="50%" valign="top">

**🔓 Privilege Escalation**
- SUID binaries and sudo misconfigurations
- Weak/reused credentials chained across services

**🔑 Password & Hash Cracking**
- Brute forcing with Hydra
- Hash cracking with John the Ripper and Hashcat

</td>
</tr>
</table>

Plus: real commands, useful one-liners, and the lessons learned from every challenge — not just the flags.

<br>

## 🗺️ The Methodology

Every walkthrough follows a structured approach:

<div align="center">

**Recon** → **Enumeration** → **Vulnerability Discovery** → **Exploitation** → **Privilege Escalation** → **Flags** → **Lessons Learned**

</div>

The objective isn't just to solve the room — it's to understand the mindset behind every decision.

<br>

## 🛠️ Technologies & Tools

<details>
<summary><b>Tools you'll regularly see used throughout these walkthroughs</b></summary>
<br>

| Category | Tools |
|---|---|
| Recon & Enumeration | Nmap, Gobuster, dirsearch, ffuf, smbclient |
| Exploitation | Burp Suite, custom PHP/Bash reverse shells |
| Credential Attacks | Hydra, John the Ripper, Hashcat |
| Privilege Escalation | GTFOBins, manual SUID/sudo enumeration |
| Shells & Access | Netcat, SSH |
| Scripting | Bash, Python |

</details>

<br>

## 📁 Repository Structure

<details>
<summary><b>How this repo is laid out</b></summary>
<br>

```text
THM_Walkthroughs/
│
├── rooms/
│   ├── Room Name.md
│   ├── Room Name.md
│   └── ...
│
├── LICENSE
└── README.md
```

Each walkthrough typically contains:

- Room overview & difficulty
- Reconnaissance
- Enumeration
- Exploitation
- Privilege escalation
- Commands used
- Screenshots
- Key takeaways

</details>

<br>

## 💭 Why This Repository Exists

This repository is more than a collection of notes — it's a record of my progress as I explore offensive security, document methodologies, and sharpen the skills required for real-world penetration testing.

> Every room solved adds another technique. Every mistake becomes another lesson. Every walkthrough is another step forward.

<br>

## 🚀 Learning Never Stops

Current areas of focus include:

| Focus Area | Tools / Concepts |
|---|---|
| Active Directory attacks | BloodHound, CrackMapExec, Impacket |
| Windows privilege escalation | WinPEAS |
| Web application security | — |
| Red team techniques | — |
| Network security | — |
| Offensive security methodology | — |

As I continue learning, this repository will continue to grow.

<br>

## ⚠️ Disclaimer

All content in this repository is provided for **educational purposes only**.

These walkthroughs are intended for authorized labs and training environments such as TryHackMe. Never use these techniques against systems without explicit permission.

<br>

## 🤝 Contributing

Have a better approach? Found a mistake? Want to share an alternative solution?

Contributions, suggestions, and discussions are always welcome — open an issue or a pull request.

<br>

## 👤 About Me

<div align="center">

**Ritvik Singh**

Cyber Security Analyst • Penetration Tester • Security Research Enthusiast

---

*"Every machine tells a story. Every exploit teaches a lesson. Every walkthrough is one more step toward mastering cybersecurity."*

</div>
