
# Module: Computer Fundamentals

## Topics
- Inside a Computer System
- Computer Types
- Client-Server Basics
- Virtualisation Basics
- Cloud Computing Fundamentals

---
## Objective
The goal of this module is to build a solid foundation in how computers work from the physical components inside a machine, to the different types of computers that exist, how they communicate with each other through the client server model, and how modern technology like virtualisation and cloud computing have changed the way we use and deploy systems.

---
## Key Concepts

### Inside a Computer System
- Every computer is made up of core hardware components that work together to process, store, and output data.
- **CPU (Central Processing Unit)** — the "brain" of the computer; it processes all instructions and calculations.
- **RAM (Random Access Memory)** — short-term memory that temporarily holds data the CPU is actively using. It's fast but loses everything when the power is off.
- **Storage (HDD/SSD)** — long-term memory that keeps data even when the computer is off. SSDs are faster than HDDs.
- **Motherboard** — the main circuit board that connects all components together.
- **PSU (Power Supply Unit)** — converts electricity from the wall into usable power for the computer's components.
- **GPU (Graphics Processing Unit)** — handles visuals and display output; also used for heavy computational tasks like AI and gaming.

### Computer Types
There is no single "best" computer — each type is built for a specific purpose:

| Computer Type | Has Screen/Keyboard | Main Purpose |
|---------------|-------------------|--------------|
| Laptop | Yes | Portable everyday computing |
| Desktop | Yes | Sustained performance at a fixed location |
| Workstation | Yes | High-precision professional tasks |
| Server | No | Provides services to many users over a network |
| Smartphone | Yes | Mobile communication and computing |
| IoT Device | Usually No | Internet-connected smart devices (fridges, locks, etc.) |
| Embedded System | No | Single-purpose computing inside machines (e.g. car brakes, coffee machines) |

- **IoT vs Embedded** — both are small and purpose-built, but IoT devices connect to a network while embedded systems often work completely offline inside a machine.

### Client-Server Basics
- Early computers worked alone — they didn't talk to each other. Networks like **ARPANET** were early steps toward connecting systems globally.
- The **client-server model** is how most internet communication works today:
  - The **client** is the one that always initiates the request (e.g. your browser)
  - The **server** receives the request, processes it, and sends back a response
- Think of it like ordering pizza: you (the client) place an order, and the pizza shop (the server) prepares and delivers it.
- **Protocols** define the rules for how clients and servers communicate for example, HTTP is used for websites.
- **Ports** are numbered entry points that tell a computer which service a request is for (e.g. port 80 for HTTP, port 443 for HTTPS).

### Virtualisation Basics
- Before virtualisation, the rule was: **one server = one application**. This was expensive and wasteful.
- **Virtualisation** allows one physical machine to act like many separate computers, each running independently.
- A **Hypervisor** is the software that manages virtual machines it acts as a "referee" between them and the physical hardware.

| Hypervisor Type | How It Works | Best Used For |
|----------------|-------------|---------------|
| Type 1 | Runs directly on hardware | Servers, enterprise environments |
| Type 2 | Runs inside an existing OS | Home labs, testing, learning |

- A **Virtual Machine (VM)** is a complete virtual computer with its own OS, apps, and settings all running on shared hardware.
- **Containers** are a lighter alternative to VMs. Instead of virtualising a whole OS, they isolate just the application and share the host system's core making them faster and more efficient.

### Cloud Computing Fundamentals
- **Cloud Computing** is built on top of virtualisation and containers. Instead of buying and maintaining your own physical servers, you rent computing resources over the internet.
- Key benefits of cloud computing:
  - **Scalability** — easily increase or decrease resources based on demand
  - **On-demand self-service** — spin up servers instantly without waiting for hardware
  - **Pay-as-you-go** — only pay for what you actually use
  - **High availability** — systems keep running even if part of the infrastructure fails
  - **Security** — cloud providers maintain strong infrastructure protection

- **Cloud Service Models:**

| Model | Who Manages What | Example |
|-------|-----------------|---------|
| IaaS (Infrastructure as a Service) | You manage the OS and apps; provider manages hardware | AWS EC2 |
| PaaS (Platform as a Service) | You manage the app; provider manages everything else | Google App Engine |
| SaaS (Software as a Service) | You just use the software; provider manages everything | Gmail, Dropbox |

- **Major Cloud Providers:**
  - **AWS (Amazon Web Services)** — industry leader with the widest range of services
  - **Microsoft Azure** — strong in enterprise and hybrid cloud environments
  - **Google Cloud Platform (GCP)** — known for AI, machine learning, and data analytics
  - **Alibaba Cloud** — major player across Asia
  - **IBM Cloud** — focused on hybrid cloud and AI-driven business solutions

---
## Activity / What I Did

In this module, I completed five TryHackMe rooms that built on each other logically starting from what's physically inside a computer and working all the way up to cloud infrastructure.

- **Inside a Computer System** — I learned about the core hardware components (CPU, RAM, storage, motherboard, GPU, PSU) and how they interact to make a computer function.

- **Computer Types** — I worked through an interactive challenge that introduced different types of computers from everyday laptops and desktops to servers, IoT devices, and embedded systems and learned what makes each one suited to its role.

- **Client-Server Basics** — I inspected a real HTTP GET request using a split-screen virtual machine, where I could see exactly what a client sends to a server and what the server sends back. It made the theory feel very concrete.

- **Virtualisation Basics** — I helped a simulated manager improve hardware utilisation by setting up virtual machines on a single physical server. I learned the difference between Type 1 and Type 2 hypervisors and when to use containers vs VMs.

- **Cloud Computing Fundamentals** — I worked through scenarios comparing IaaS, PaaS, and SaaS to understand which cloud service model fits different situations, and calculated basic instance costs to understand the pay as you go model.

---
## What I Learned

This module gave me a much clearer picture of how modern computing infrastructure is built layer by layer. Before this, I thought of "the cloud" as something vague and magical, but now I understand it's basically virtualisation at a massive scale, rented out over the internet. The client server section also helped me connect dots from earlier modules now when I think about DNS, HTTP, and web browsing, I can see the full picture of a client making a request and a server responding. The computer types room was surprisingly interesting too; I didn't realise how many types of computers exist beyond the ones you can see, like embedded systems quietly running inside everyday machines. Overall, this module made everything feel a lot more connected.
