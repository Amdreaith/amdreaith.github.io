---
title: CTF Industrial Intrusion Participant (TryHackMe)
description: My first Capture the Flag (CTF) experience with a team, where we explored an industrial-themed environment, solved real-world cybersecurity challenges, and learned the value of teamwork.
author: TryHackMe
date: 2025-06-26 20:55:00 +0800
categories: [CTF, TryHackMe]
tags: [CTF, TryHackMe, Cybersecurity, Industrial Intrusion, OSINT]
pin: true
image:
  path:  /assets/img/favicons/2.png
  alt: "TryHackMe Industrial Intrusion CTF"


---

## Overview

In June 2025 I joined my **first-ever Capture the Flag (CTF)** competition: **Industrial Intrusion** on TryHackMe.  
The challenge simulated an **industrial control system (ICS)** environment. Our small team worked together to discover vulnerabilities, exploit services, and dig through clues. I was hesitant at first—I wasn’t sure what I could contribute as a beginner—but the experience turned out to be rewarding and motivating. As someone who learns best by *seeing* things, I naturally gravitated toward **OSINT** and cryptography.

---

## Key experiences

- Gained **hands-on experience** in ICS-style scenarios.  
- Practiced **team collaboration**: dividing tasks, sharing findings, and coordinating next steps.  
- Focus areas in the room: **OSINT**, **web enumeration**, and **cryptography**.

---

## Example Challenge — Web Enumeration & Forensics

**Challenge (short):** Find a way to bypass the badge authentication system by interacting with an exposed web UI and uncover the hidden flag.

### Reproduction steps (what I did)

1. **Port scan the target**
   ```bash
   nmap -sC -sV -p- 10.10.154.123
2. Directory enumeration

gobuster dir -u "http://10.10.154.123:1880" \
  -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt \
  -x .txt,.html,.php,.bak -t 50


Gobuster returned several directories. Notably, there were two /ui-style directories that differed only by case: /ui and /UI. Case differences can expose alternate resources; I tried both.

3. Open the UI
Visit:

http://10.10.154.123:1880/ui


The UI presented controls (toggles) for systems such as a motion detector and a badge.

4. Interact with the interface
Toggle off the motion detector and the badge control, then refresh the page to confirm the new state. The UI reflected the changes and the backend accepted the new state.

5. Result
After disabling those features and refreshing, the gate authentication was effectively bypassed and the challenge revealed the flag.


![GIF](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExYzVrYWRxZzlxNjkwYWlkMHp4em8xNHB6OHYwM3BldXg3czJqdWFjNyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/KMgPHp5bI60qDWPy1A/giphy.gif){: .w-80 .shadow .rounded-3 }

### Reflection

This was my first practical CTF and it taught me confidence: try things, document steps, and communicate with teammates. I still have a lot to learn , but this experience motivated me to continue practicing.

