
# Module: How The Web Works

## Topics
- DNS in Detail
- HTTP in Detail
- How Websites Work
- Putting It All Together

---

## Objective
The goal of this module is to understand how the web actually works behind the scenes from how domain names get translated into IP addresses, to how browsers communicate with web servers, and how websites are built and delivered to users.

---

## Key Concepts

### DNS in Detail
- **DNS (Domain Name System)** is like the internet's phone book — it converts a domain name like `google.com` into an IP address your computer can use.
- **Domain Hierarchy** — Domains are structured in levels: TLD (Top-Level Domain) → Second-Level Domain → Subdomain. Example: `sub.tryhackme.com`
- There are two types of TLDs: **gTLD** (generic, like `.com`, `.org`) and **ccTLD** (country code, like `.co.uk`, `.ca`)
- **DNS Record Types:**

| Record | Purpose |
|--------|---------|
| A | Maps a domain to an IPv4 address |
| AAAA | Maps a domain to an IPv6 address |
| CNAME | Points one domain to another domain |
| MX | Directs email to the correct mail server |
| TXT | Stores text data (used for verification, spam prevention, etc.) |

- The DNS lookup process goes: Local Cache → Hosts File → Recursive DNS Server → Root Name Server → TLD Server → Authoritative Name Server

### HTTP in Detail
- **HTTP (HyperText Transfer Protocol)** is the protocol browsers and web servers use to communicate. **HTTPS** is the encrypted, secure version.
- A **URL** is made up of several parts:
  - `scheme` (http/https)
  - `host` (domain name or IP)
  - `port` (80 for HTTP, 443 for HTTPS)
  - `path` (the resource location)
  - `query string` (extra parameters, e.g. `?id=1`)
  - `fragment` (section reference, e.g. `#task3`)
- **HTTP Methods:**

| Method | What It Does |
|--------|-------------|
| GET | Retrieve data from the server |
| POST | Send data to the server |
| PUT | Update existing data |
| DELETE | Remove data |

- **HTTP Status Codes:**

| Code | Meaning |
|------|---------|
| 200 | OK — request successful |
| 301 | Moved Permanently — redirect |
| 404 | Not Found |
| 403 | Forbidden |
| 500 | Internal Server Error |

### How Websites Work
- Websites have two sides: **Front End** (what the user sees — HTML, CSS, JavaScript) and **Back End** (the server that processes requests — PHP, Python, Node.js, etc.)
- **HTML** defines the structure of a webpage. **JavaScript** makes it interactive and dynamic.
- **Sensitive Data Exposure** happens when a developer accidentally leaves private info (like passwords or API keys) visible in the page's source code.
- **HTML Injection** is a vulnerability where unsanitised user input gets rendered as actual HTML on the page, which an attacker can exploit.

### Putting It All Together
- When you visit a website, here's what happens step by step:
  1. Your browser checks the **DNS** to get the IP address of the domain
  2. A connection is made to the **web server** using HTTP/HTTPS
  3. The server processes the request and sends back a response
  4. Your browser renders the **HTML, CSS, and JavaScript**

- Other important components:
  - **Load Balancers** — distribute traffic across multiple servers to prevent crashes
  - **CDN (Content Delivery Network)** — serves static files (images, videos, JS) from the nearest server to the user
  - **Databases** — store and retrieve user data (MySQL, MongoDB, PostgreSQL, etc.)
  - **WAF (Web Application Firewall)** — sits between the user and server, blocking malicious requests and bot traffic

---

## Activity / What I Did

In this module, I worked through four TryHackMe rooms that covered how the web works from start to finish. Here's a breakdown of what I did in each:

- **DNS in Detail** — I learned how DNS resolves domain names and practiced using `nslookup` to query different DNS record types like A, CNAME, MX, and TXT records.

```bash
nslookup --type=A tryhackme.com
nslookup --type=CNAME shop.website.thm
nslookup --type=MX website.thm
nslookup --type=TXT website.thm
```

- **HTTP in Detail** — I made different types of HTTP requests (GET, POST, PUT, DELETE) to a practice web server and observed the responses and status codes.

- **How Websites Work** — I inspected HTML source code to find sensitive data, fixed broken HTML, and practiced an HTML injection attack by inserting a malicious link through an unsanitised input field.

```html
<!-- HTML Injection Example -->
<a href="http://hacker.com">Click Here</a>
```

- **Putting It All Together** — I completed a quiz that walked through the full process of what happens when you load a webpage, covering DNS, HTTP, load balancers, CDNs, and WAFs.

---

## What I Learned

This module really filled in a lot of gaps for me. I use websites every day but never thought about all the steps happening in the background just to load a single page. The DNS section was especially interesting 
the fact that there's this whole layered system of servers just to convert a domain name into an IP is something I never thought about before. The HTTP section also made me realize how much information is exchanged just in a single request and response. The HTML injection exercise was a good eyecopener too it showed how something as simple as a text input can become a security risk if a developer isn't careful. Overall, this module connected a lot of dots and made me see the web very differently.
