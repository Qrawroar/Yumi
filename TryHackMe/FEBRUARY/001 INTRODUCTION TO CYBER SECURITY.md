
# Module: Introduction to Cyber Security

## Topics
- Offensive Security Intro
- Defensive Security Intro
- Careers in Cyber

---

## Key Concepts

- **Offensive Security** is the "hacker side" of cybersecurity. The idea is to find weaknesses in a system before the bad guys do, using techniques like penetration testing.
- **Defensive Security** is all about keeping systems safe monitoring for threats, stopping attacks, and responding when something goes wrong.
- **SOC (Security Operations Center)** is basically a team that watches over a network 24/7 looking for anything suspicious.
- **SIEM Tools** help SOC teams by collecting and analyzing data from across a network to spot threats in real time.
- **Malware** is malicious software that can damage or take over systems things like viruses, trojans, and ransomware.
- There are tons of career options in cyber from Penetration Testers and Red Teamers on the offensive side, to Security Analysts and Incident Responders on the defensive side.

---

## Activity / What I Did

For this module, I did a hands on activity on TryHackMe where I got to hack into a fake website in a safe environment. Also I hack a bank account using the virtual machine as a simulation and I used some basic Linux commands and a tool called Gobuster to find hidden pages on the site. Here's a quick breakdown of what I used:

### Linux Commands

| Command | Description |
|--------|-------------|
| `ls` | Shows what files and folders are in your current location |
| `ls -l` | Gives a detailed view with permissions |
| `ls -a` | Shows hidden files too |
| `cat filename.txt` | Opens and reads a single file |
| `cat file1 file2` | Reads two files at once |
| `dirb http://website.com` | list of potential page names |

### Gobuster

`gobuster` scans a website for hidden directories or pages.

```bash
gobuster dir -u <target-url> -w <wordlist>
```

| Flag | Description |
|------|-------------|
| `-u` | The target website URL you want to scan |
| `-w` | Points to a wordlist used to guess hidden page names |

### HTTP Status Codes to Know

| Code | Meaning |
|------|---------|
| 200  | Page exists and is working ✅ |
| 300  | Redirect ↪️ |
| 400  | Error ❌ |

It was a pretty eye opening experience seeing how these tools actually work in practice.

---

## What I Learned

Honestly, this module was a solid intro to cybersecurity. I went in not knowing much, and came out with a clearer goal of how both sides attacking and defending actually work together. Using real tools like Gobuster made it way more interesting than just reading about it. I also didn't realize how many different career paths there are in this field. Theres something for everyone. It's definitely got me curious to keep going and learn more.
