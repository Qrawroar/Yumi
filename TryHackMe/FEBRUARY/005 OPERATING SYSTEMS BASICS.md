
# Module: Operating Systems Basics

## Topics
- Operating Systems: Introduction
- Windows Basics
- Linux CLI Basics
- Windows CLI Basics
- Operating System Security

---
## Objective

The goal of this module is to understand what an operating system actually does, get hands on experience navigating both Windows and Linux environments, and learn how operating systems are secured against threats like weak passwords, malware, and unauthorized access.

---
## Key Concepts

### Operating Systems: Introduction
- An **Operating System (OS)** is the core software that sits between the user, applications, and the physical hardware it manages everything so things don't conflict or crash.
- Think of the OS like an airport control tower: it coordinates all the "flights" (applications and hardware) so everything runs smoothly without collisions.
- Key responsibilities of an OS:

| Responsibility | What It Does |
|----------------|-------------|
| Process Management | Runs and schedules programs using the CPU |
| Memory Management | Allocates RAM to running applications |
| File System Management | Organises and controls access to files |
| User Management | Handles accounts, authentication, and permissions |
| Security | Enforces access controls and system protection |

- **Kernel Space** — the highly privileged area of the OS with direct hardware access. Only the OS core runs here.
- **User Space** — where regular applications run with limited permissions to keep the system stable and safe.
- Common operating systems include: **Windows, macOS, Linux, Android, iOS, and Chrome OS.**

### Windows Basics
- Windows started as a simple GUI built on top of MS-DOS back in 1985. Today it's the most widely used desktop OS in the world.
- The **Windows Desktop** includes the taskbar, Start menu, system tray, and desktop icons — all familiar visual tools for interacting with the OS.
- **NTFS** is the default Windows file system — it supports permissions, encryption, and large file sizes.
- User accounts come in two types:
  - **Administrator** — full control over the system
  - **Standard User** — restricted; can't make system level changes
- User profiles are stored in `C:\Users`
- **UAC (User Account Control)** is a security feature that prompts for confirmation before allowing changes that affect the system — even admins are restricted until they confirm.
- **Windows Defender** is the built-in antivirus and security tool for scanning and protecting against malware.

### Linux CLI Basics
- Linux is everywhere in cybersecurity — it powers servers, security tools, and hacking environments. Knowing the CLI is essential.
- The **CLI (Command-Line Interface)** lets you interact with the OS purely through text commands, without a GUI.

**Core Linux Commands:**

| Command | What It Does |
|---------|-------------|
| `pwd` | Print working directory — shows where you currently are |
| `ls` | Lists files and folders in the current directory |
| `ls -a` | Shows hidden files too |
| `cd` | Change directory |
| `cat filename` | Reads and displays the contents of a file |
| `find` | Searches for files across the system |
| `whoami` | Shows which user you're currently logged in as |
| `uname -a` | Shows kernel and system version info |
| `df -h` | Shows disk space usage in human-readable format |

**Example usage:**
```bash
pwd                        # Show current directory
ls -a                      # List all files including hidden
cd /etc                    # Navigate to the /etc directory
cat mission_brief.txt      # Read a file
find / -name day1_report.txt   # Search for a specific file
whoami                     # Check current user
uname -a                   # Get kernel version
df -h                      # Check disk space
```

### Windows CLI Basics
- The **Windows Command Prompt (CMD)** is the text-based interface for interacting with Windows it's used daily by cybersecurity professionals to investigate and troubleshoot systems.
- CMD uses fewer resources than the GUI and is great for automation and remote management.

**Core Windows CMD Commands:**

| Command | What It Does |
|---------|-------------|
| `cd` | Change directory |
| `dir` | List files and folders |
| `dir /a` | List all files including hidden |
| `type filename.txt` | Read the contents of a file |
| `tree` | Show the full folder structure |
| `cls` | Clear the screen |
| `hostname` | Display the computer's name |
| `ipconfig /all` | Show full network configuration |
| `netstat -abon` | Show current network connections and listening ports |
| `systeminfo` | Display detailed system and OS information |
| `tasklist` | Show running processes |
| `ping` | Test network connectivity |
| `tracert` | Trace the path to a destination server |
| `nslookup` | Perform a DNS query |

**Example usage:**
```cmd
cd C:\Users\Desktop
dir /a
type flag.txt
ipconfig /all
systeminfo
netstat -abon
tracert tryhackme.com
```

### Operating System Security
- The OS is the foundation of a computer — if it's compromised, everything running on top of it is at risk.
- **Three main areas of OS security:**
  - **User Accounts & Authentication** — weak or shared passwords are one of the most common entry points for attackers
  - **File & Folder Permissions** — controlling who can read, write, or execute files is critical for limiting damage
  - **Malware Protection** — the OS must be protected against viruses, trojans, ransomware, and spyware
- **Principle of Least Privilege** — users and programs should only have the minimum access they need to do their job. This limits the blast radius if something goes wrong.
- Keeping the OS **updated and patched** is one of the most important defensive habits many real world attacks exploit unpatched vulnerabilities.

---
## Activity / What I Did

This module had a lot of hands-on work across five rooms, all running inside virtual machines directly in the browser.

- **Operating Systems: Introduction** — I was given a mystery computer from a "friend" and used the OS to investigate its hardware, check system specs, and explore the file system. It was a fun scenario that made the theory feel practical.

- **Windows Basics** — I played the role of a new employee at a fictional company (TryHatMe) on my first day. I navigated the Windows Desktop, explored system properties, managed files and folders, and ran a **Windows Defender** scan that detected a test malware file.

- **Linux CLI Basics** — I acted as an intern on a cyber security team and was given a mission to find files on a Linux system using only the terminal. I used `find`, `cat`, `pwd`, `ls`, `whoami`, `uname -a`, and `df -h` to complete the tasks and collect system information.

- **Windows CLI Basics** — I continued the intern story but this time on a Windows machine. I navigated through CMD, listed hidden files, read flag files, checked network connections with `netstat`, and gathered system info using `systeminfo` and `ipconfig`.

- **Operating System Security** — I explored how operating systems are secured, looking at user account controls, file permissions, and malware threats. I also practiced identifying security misconfigurations that could leave a system exposed.

---
## What I Learned

This was honestly one of the most useful modules so far. I use Windows every day but never really thought about what's happening underneath the GUI. Getting into CMD and actually navigating with commands made me feel way more in control of the system. The Linux CLI section was challenging at first because the syntax is completely different from Windows, but after a few commands it started to click. The thing that stood out most was the OS Security room I realised how much of cybersecurity comes down to really basic things like setting strong passwords, applying the right permissions, and keeping the system updated. These aren't glamorous skills, but they're the ones that actually prevent most real world attacks.
