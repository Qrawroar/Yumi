
# Module: Attacks and Defenses

## Topics
- The CIA Triad
- Cryptography Concepts
- Become a Hacker
- Become a Defender

---
## Objective
The goal of this module is to understand the core mindset behind cybersecurity what we are actually protecting and why and then see both sides of the field in action: how attackers find and exploit weaknesses, and how defenders detect, prevent, and respond to threats.

---
## Key Concepts

### The CIA Triad
- The **CIA Triad** is the foundation of the cybersecurity mindset. It defines the three things every security professional is trying to protect:

| Pillar | What It Means | Attacked By |
|--------|--------------|-------------|
| **Confidentiality** | Only authorized people can access the data | Disclosure / Data Breach |
| **Integrity** | Data cannot be altered by unauthorized people | Tampering / Modification |
| **Availability** | Systems and data must be accessible when needed | Destruction / DoS Attack |

- Every security incident can be explained in terms of which pillar was affected. For example:
  - A data breach = **Confidentiality** violated
  - A ransomware attack = **Availability** (and sometimes Integrity) violated
  - Someone modifying a database record = **Integrity** violated
- The CIA Triad isn't just a set of definitions it's a **security mindset** that shapes how professionals think about every decision, policy, and tool they use.

### Cryptography Concepts
- **Cryptography** is the practice of securing information by transforming it so only authorized parties can read it.
- It directly supports the **Confidentiality** and **Integrity** pillars of the CIA Triad.
- Core terminology:

| Term | Meaning |
|------|---------|
| **Plaintext** | The original, readable message |
| **Ciphertext** | The scrambled, unreadable version |
| **Key** | The secret that controls the encryption/decryption |
| **Algorithm** | The public method/formula used with the key |

- **Symmetric Encryption** — uses a single key for both encrypting and decrypting. Fast and efficient, but both parties need the same key. Example: **Caesar Cipher** (simple shift of letters).

```
Plaintext:  HELLO
Key:        shift by 3
Ciphertext: KHOOR
```

- **Asymmetric Encryption** — uses a **key pair**: a **public key** (shared with everyone) to encrypt, and a **private key** (kept secret) to decrypt. Solves the problem of how to share keys safely.
- **How HTTPS works** — when you visit a secure website, asymmetric encryption is used first to exchange a shared key, then symmetric encryption takes over for the actual data transfer because it's faster.
- **Digital Certificates** — issued by a trusted **Certificate Authority (CA)**, they verify that a website is who it says it is. You can check these by clicking the padlock icon in your browser.
- Cryptography is a critical layer of defense but not a complete solution on its own  it works alongside strong passwords, patching, monitoring, and user awareness.

### Become a Hacker (Offensive Security)
- Ethical hackers, also called **Red Team**, use the same techniques as real attackers but with permission — to find weaknesses before malicious actors do.
- The goal of offensive security is to **think like an attacker**: understand how systems can be exploited so that defenders can fix those weaknesses.
- The general **hacking methodology** follows a structured process:

| Phase | What Happens |
|-------|-------------|
| **Reconnaissance** | Gathering information about the target (passive or active) |
| **Scanning** | Identifying open ports, services, and vulnerabilities |
| **Exploitation** | Attacking the identified vulnerabilities to gain access |
| **Post-Exploitation** | Maintaining access, escalating privileges, collecting data |
| **Reporting** | Documenting findings and recommending fixes |

- Common offensive tools and techniques include:
  - **nmap** — network scanning to find open ports and running services
  - **Gobuster** — brute-forcing hidden directories and files on web servers
  - **Burp Suite** — intercepting and manipulating HTTP requests
  - **Metasploit** — an exploitation framework for testing known vulnerabilities

### Become a Defender (Defensive Security)
- Defenders, also called the **Blue Team**, focus on protecting systems, detecting threats, and responding to incidents.
- Key defensive concepts:

| Term | Definition |
|------|-----------|
| **Threat** | A potential danger that could harm systems or data |
| **Prevention** | Stopping threats before they cause harm |
| **Detection** | Identifying suspicious activity in networks and systems |
| **Mitigation** | Reducing or stopping the impact of an active threat |
| **Risk** | The likelihood and impact of a threat succeeding |

- **Defence in Depth** — instead of relying on one security layer, defenders build multiple overlapping layers so that if one fails, others are still in place. Think of it like a castle with a moat, walls, guards, and a locked vault inside.
- Key defensive tools and practices:
  - **SIEM (Security Information and Event Management)** — collects and analyzes logs across the network to detect suspicious patterns
  - **Firewalls and WAFs** — block unauthorized traffic and filter malicious requests
  - **IDS/IPS (Intrusion Detection/Prevention Systems)** — monitor for and respond to known attack patterns
  - **Patch Management** — keeping systems updated to close known vulnerabilities
  - **Incident Response Plan** — a predefined process for detecting, containing, and recovering from a security breach
- Defenders need to **understand how attackers think** — that's why studying both sides is so important in cybersecurity.

---
## Activity / What I Did

This module had four connected rooms that took me from understanding core security principles all the way to hands-on offensive and defensive exercises.

- **The CIA Triad** — I worked through an interactive drag-and-drop exercise where I was given nine real-world security incidents and had to classify each one under Confidentiality, Integrity,
- or Availability. It was a good test of understanding because some incidents overlapped multiple pillars.

- **Cryptography Concepts** — I explored how encryption works in practice. I used the Caesar cipher to encrypt and decrypt messages manually, then inspected a real HTTPS certificate in the browser to see how asymmetric encryption is used to verify website identity.

```
# Caesar Cipher - Encrypting with a shift of 3
Plaintext:  TRYHACKME
Ciphertext: WUBKDFNPH
```

- **Become a Hacker** — I took on the role of an ethical hacker and used beginner-level offensive techniques to find and exploit vulnerabilities on a target machine inside a controlled TryHackMe environment.
- I practiced reconnaissance and scanning to understand what was running on the target before attempting to exploit it.

- **Become a Defender** — I switched to the Blue Team perspective and worked through a defensive scenario where I had to identify threats, detect suspicious activity using logs,
- and respond to an active incident. It reinforced how defenders rely on visibility if you can't see what's happening on your network, you can't protect it.

---
## What I Learned

This was probably the most eye opening module in the entire path. The CIA Triad exercise hit different once I had to apply it to real world scenarios it's one thing to memorize the three letters, but classifying actual incidents made the framework feel genuinely useful. The cryptography room also finally made HTTPS click for me; I seen that padlock icon my whole life but never really understood the asymmetric/symmetric handshake happening in the background. Doing both the hacker and defender rooms back to back was a smart design choice you really can't understand one side without the other. I came away from this module more convinced than ever that the best defenders are the ones who think like attackers. 

