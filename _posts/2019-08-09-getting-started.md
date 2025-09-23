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

In June 2025, I joined my **first-ever Capture the Flag (CTF)** competition: **Industrial Intrusion** on TryHackMe.  
The challenge simulated an **industrial control system (ICS)** environment. Our small team worked together to discover vulnerabilities, exploit services, and dig through clues. I was hesitant at first—I wasn't sure what I could contribute as a beginner but the experience turned out to be rewarding and motivating. As someone who learns best by *seeing* things, I naturally gravitated toward **OSINT** and cryptography.

---

## Key Experiences

- Gained **hands-on experience** in ICS-style scenarios  
- Practiced **team collaboration**: dividing tasks, sharing findings, and coordinating next steps  
- Focus areas in the room: **OSINT**, **web enumeration**, and **cryptography**

---

## Example Challenge  

OSINT 1

During the challenge, a critical piece of information was identified: a link to a GitHub repository, https://github.com/solstice-tech1/ot-auth-mirror/blob/main/index.html. This suggested that the website's source code, or at least a relevant part of it, was hosted there.
<img width="484" height="225" alt="image" src="https://github.com/user-attachments/assets/42af9184-66cf-410e-8c3a-70f6bb48b0af" />


Initially, an attempt was made to directly paste or interact with this source on a live website, but it yielded no functional results. This indicated that the raw HTML was not intended for direct use in its current form.
<img width="573" height="323" alt="image" src="https://github.com/user-attachments/assets/45c14fb1-3989-4e34-8e16-287597c363a9" />


Recognizing this, the next step involved examining the content for encoding. Upon closer inspection, the data appeared to be in a hexadecimal format, prompting an attempt to decode it from hexadecimal, which proved to be the correct approach for revealing the underlying information.




![GIF](https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExYzVrYWRxZzlxNjkwYWlkMHp4em8xNHB6OHYwM3BldXg3czJqdWFjNyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/KMgPHp5bI60qDWPy1A/giphy.gif){: .w-80 .shadow .rounded-3 }


### Reflection

This was my first practical CTF and it taught me confidence: try things, document steps, and communicate with teammates. I still have a lot to learn, but this experience motivated me to continue practicing.