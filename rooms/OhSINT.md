
# TryHackMe – OhSINT Walkthrough

> **Room**: [TryHackMe – OhSINT](https://tryhackme.com/room/ohsint)  
> **Difficulty**: Beginner  
> **Skills**: OSINT (metadata analysis, Google search, Wi‑Fi mapping)  
This is the walkthrough for the [OhSINT room](https://tryhackme.com/room/ohsint) on TryHackMe.

### Task 1:

All I have is a photo. I used exiftool to see what starting information I could get of the photo. (`exiftool WindowsXP.jpg`).

<img width="668" alt="Screenshot 2025-06-17 at 3 22 57 PM" src="https://github.com/user-attachments/assets/e061cf1a-53ea-4c27-8223-2d9f1b312333" />

Notice that the Copyright value is OWoodflint. Next, I searched good ol' google to see what I could find on OWoodflint.

I found their twitter page (answering question 1),

<img width="725" alt="Screenshot 2025-06-17 at 3 23 14 PM" src="https://github.com/user-attachments/assets/e192a99f-51f9-4279-9439-15dcdf54333c" />


their blog (answering questions 6 & 7, if you inspect the blog's HTML),

<img width="725" alt="Screenshot 2025-06-17 at 3 23 55 PM" src="https://github.com/user-attachments/assets/8de8a6fe-656c-4d49-91ec-39d16e7b8083" />

and their github (answering questions 2, 4 & 5).

<img width="726" alt="Screenshot 2025-06-17 at 3 24 22 PM" src="https://github.com/user-attachments/assets/7758d7f6-3bf2-4918-905b-e220b37df0ac" />

1. What is this user's avatar of?

   > cat

2. What city is this person in?

   > London

3. What's the SSID of the WAP he connected to?

   The hint for question 2 mentions *BSSID + Wigle.net*. So, I accessed [Wigle.net](https://wigle.net/) and, plugging in the BSSID found OWoodflint's twitter page, I found the exact location of the WAP and its SSID. Yikes!
   
<img width="696" alt="Screenshot 2025-06-17 at 3 24 44 PM" src="https://github.com/user-attachments/assets/27220385-8bb3-44fa-ba6f-20235281f8e5" />


   *Notice the purple circle on the map and zoom in really really close on it.*

   > UnileverWiFi

5. What is his personal email address?

   > OWoodflint@gmail.com

6. What site did you find his email address on?

   > github

7. Where has he gone on holiday?

   > New York

8. What is this persons password?

   > pennYDr0pper.!
