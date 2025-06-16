<div align='center'>
  <img width="301" alt="Screenshot 2025-06-13 at 2 18 03 PM" src="https://github.com/user-attachments/assets/1f09acf9-5777-4362-819e-344c28d0f68a" />
</div>
Simple CTF on TryHackMe is a beginner-friendly room that teaches basic enumeration, exploitation, and privilege escalation techniques. It involves capturing user and root flags using tools like `nmap`, `gobuster`, and `hydra`.

Step 1:

<img width="479" alt="Screenshot 2025-06-13 at 2 28 06 PM" src="https://github.com/user-attachments/assets/d6cf96ba-d9c5-4a12-8cc8-21d4f0344b95" />

First we will scan the given ip address and check the available/open ports.
Here we completed our first task, "How many services are running under port 1000?"
Observe the available ports and then fill the answer.

Step 2:

When we run the command 
```
python3 dirsearch.py -u http://10.10.248.5
```
<img width="893" alt="Screenshot 2025-06-13 at 2 54 06 PM" src="https://github.com/user-attachments/assets/75847cd0-e1a8-4cf4-a8dc-f414774ac783" />

Here we found out that, there is a page named ` http://10.10.248.5/simple/ ` .
When we visit this page and scroll down, we find that ` This site is powered by CMS Made Simple version 2.2.8 `, this statement is written.
If we google the vulnerability of this website, we will find out the vulnerability of this website.

We can also use the below method to find the CVE.
<img width="893" alt="Screenshot 2025-06-13 at 3 21 13 PM" src="https://github.com/user-attachments/assets/0ba17bbf-f9a3-4038-8263-8fd33fc2d9d9" /> <br>

By using the command `vim 46635.py `
![2025-06-13_15-52](https://github.com/user-attachments/assets/641a3cb9-bb93-4827-a762-47ff83670de2)

We can check the CVE of this vulnerability.

Or we can directly google the vulnerability and check the CVE.

<img width="1173" alt="Screenshot 2025-06-13 at 3 00 19 PM" src="https://github.com/user-attachments/assets/2f20b06a-b94a-486b-b83a-d838077b7309" />
By this information, we get to know the CVE of the vulnerability and the kind of vulnerability is the application vulnerable.
(I am not giving the answers here for self exploring purposes.)




