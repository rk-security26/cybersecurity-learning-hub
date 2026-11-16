# TryHackMe: Cat Pictures 2

![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Platform](https://img.shields.io/badge/Platform-TryHackMe-red)
![Difficulty](https://img.shields.io/badge/Difficulty-Easy-blue)

**Room:** Cat Pictures 2 ("Now with more Cat Pictures!")
**Link:** https://tryhackme.com/room/catpictures2
**Duration:** ~60 min
**Type:** Offensive / CTF-style machine
**Tasks:** 2 (Deploy the VM, Flags)
**Result:** Room completed, 3 flags captured, 90 points earned

---

## 1. Overview

A boot-to-root style room where the goal is to compromise a web server and capture three flags. No hints are given beyond the flag questions, so the room tests your own enumeration and research skills.

## 2. Skills Practiced

- Network and service enumeration
- Web application enumeration
- File and image metadata analysis
- Finding and using exposed credentials
- Researching known vulnerabilities
- Privilege escalation basics

## 3. Tools Used

| Tool | Purpose |
|------|---------|
| Nmap | Port and service scan |
| Browser | Manual web enumeration |
| Gobuster / ffuf | Directory discovery |
| ExifTool | Reading image metadata |
| SSH | Remote access |
| Searchsploit / Google | Finding known exploits |

> Edit this table: keep only the tools you actually used.

## 4. Methodology

### Step 1: Deploy the machine
Started the target VM from the room and connected through the AttackBox / VPN.

### Step 2: Enumeration
Scanned the target to find open ports and services.

```bash
nmap -sC -sV -p- <TARGET_IP>
```

**Findings:**
- Open ports: `<add ports>`
- Services running: `<add services>`

### Step 3: Web enumeration
Browsed each web service and checked for hidden directories and useful information.

```bash
gobuster dir -u http://<TARGET_IP> -w /usr/share/wordlists/dirb/common.txt
```

**Findings:** `<add what you found>`

### Step 4: Initial access
`<Explain in 2-3 lines how you got your first foothold, e.g. found credentials, used an exposed service.>`

### Step 5: Flags
| Flag | Where it was found | Method |
|------|-------------------|--------|
| Flag 1 | `<location>` | `<short method>` |
| Flag 2 | `<location>` | `<short method>` |
| Flag 3 | `<location>` | `<short method>` |

> Flag values are not shared here, so the room stays fun for others.

## 5. Key Takeaways

- Always enumerate fully before trying to exploit anything.
- Small details (like file metadata) can leak useful information.
- Exposed credentials and misconfigured services are a common way in.
- Researching a service's version often leads straight to a known weakness.

## 6. Defensive Notes

How to prevent what I exploited here:
- Strip metadata from files before publishing them.
- Never leave credentials or notes in publicly reachable places.
- Restrict access to internal services and keep software updated.
- Use strong, unique passwords and limit privileges.

## 7. Proof of Completion

Room completed on TryHackMe, 2/2 tasks, 31-day streak.

**TryHackMe profile:** https://tryhackme.com/p/irizwankhan55

---

*Part of my [cybersecurity portfolio](https://github.com/rk-security26).*
