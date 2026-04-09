
# Module: Network Fundamentals

## Topics
- What is Networking?
- Intro to LAN
- OSI Model
- Packets & Frames
- Extending Your Network

---

## Objective
The goal of this module is to understand how networks work from the ground up covering how devices communicate, how data travels across a network, and the models and protocols that make it all possible.

---

## Key Concepts

- **Networking** is basically how devices talk to each other, whether it's two computers in the same room or millions of devices across the internet.
- **LAN (Local Area Network)** is a network that connects devices in a small area like a home or office. Devices on a LAN can communicate directly with each other.
- **The OSI Model** is a 7-layer framework that explains how data moves from one device to another. Each layer has a specific job:

| Layer | Name | What It Does |
|-------|------|--------------|
| 7 | Application | Interface for apps to send/receive data |
| 6 | Presentation | Formats, encrypts, or compresses data |
| 5 | Session | Manages and maintains connections |
| 4 | Transport | Chooses TCP or UDP; breaks data into segments |
| 3 | Network | Handles IP addressing and routing |
| 2 | Data Link | Uses MAC addresses for physical delivery |
| 1 | Physical | Sends raw binary data as electrical signals |

- **TCP vs UDP** — TCP is connection-based and reliable (used for file transfers, web pages), while UDP is faster but less reliable (used for video streaming, gaming).
- **Packets & Frames** — Data gets wrapped in different formats as it travels through the OSI layers. This process is called **encapsulation**. At Layer 4 it's a *segment* (TCP) or *datagram* (UDP), at Layer 3 it's a *packet*, and at Layer 2 it's a *frame*.
- **DNS (Domain Name System)** converts domain names like `google.com` into IP addresses so your computer knows where to send requests.
- **The TCP/IP Model** is the real-world version of the OSI model, condensed into 4 layers: Application, Transport, Internet, and Network Interface.
- **Three-Way Handshake** — Before TCP sends any data, it establishes a connection using SYN → SYN/ACK → ACK.

---

## Activity / What I Did

In this module, I went through a series of hands-on tasks on TryHackMe that covered both the theory and practical side of networking. I learned how data travels across networks and practiced using real networking tools in the terminal.

### Commands I Used

#### `ping` — Test if a connection to a host is possible
```bash
ping <target>
ping bbc.co.uk
ping -4 <target>   # Force IPv4
ping -i 2 <target> # Change interval between requests
ping -v <target>   # Verbose output
```

#### `traceroute` — Map the path your request takes to a destination
```bash
traceroute <destination>
traceroute -i eth0 <destination>  # Specify an interface
traceroute -T <destination>       # Use TCP SYN requests
```

#### `whois` — Look up who owns a domain
```bash
whois <domain>
whois facebook.com
whois microsoft.com
```

#### `dig` — Manually query DNS servers for domain information
```bash
dig <domain> @<dns-server-ip>
dig google.com @8.8.8.8
```

> **Useful to know:** DNS TTL is measured in seconds. A TTL of 24 hours = **86400 seconds**.

### Key Answers from the Tasks

| Question | Answer |
|----------|--------|
| Which layer chooses TCP or UDP? | Layer 4 (Transport) |
| What is data called at Layer 2? | Frames |
| What is data called at Layer 4 (UDP)? | Datagrams |
| What is the second step of the three-way handshake? | SYN/ACK |
| Where does your computer look first for a domain's IP? | Hosts File |
| What does TTL stand for? | Time To Live |
| Google's two public DNS servers | 8.8.8.8 and 8.8.4.4 |

---

## What I Learned

This module gave me a solid foundation in how networks actually work. Before this, I kind of just knew that "data goes through the internet" but now I understand the actual steps involved. The OSI model was the most interesting part for me because it broke everything down layer by layer, and it finally made sense why things like IP addresses and MAC addresses are different things. Using tools like `ping`, `traceroute`, `whois`, and `dig` in the terminal made it feel real instead of just textbook stuff. It also helped me see how networking knowledge connects directly to cybersecurity knowing how data travels is the first step to understanding how it can be intercepted or protected.
