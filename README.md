<div align="center">
  <img src="./assets/typewriter-cameroncodesstuff.gif" alt="Typewriter Animation" />

  <h1>Hacking Guide</h1>

  <p>
    A beginner-friendly guide to Linux, cybersecurity, penetration testing,
    networking, web security, wireless security, scripting and security labs.
  </p>
</div>

---

## Table of Contents

* [About](#about)
* [Important: Read This First](#important-read-this-first)
* [What You Will Learn](#what-you-will-learn)
* [Distro](#distro)

  * [ParrotOS](#parrotos)
  * [Kali Linux](#kali-linux)
  * [BlackArch](#blackarch)
  * [Ubuntu](#ubuntu)
  * [Quick Comparison](#quick-comparison)
* [Setting Up a Hacking Lab](#setting-up-a-hacking-lab)
* [Linux Fundamentals](#linux-fundamentals)
* [Networking Fundamentals](#networking-fundamentals)
* [Bash](#bash)
* [Python for Cybersecurity](#python-for-cybersecurity)
* [Reconnaissance](#reconnaissance)
* [Scanning and Enumeration](#scanning-and-enumeration)
* [Web Security](#web-security)

  * [HTTP](#http)
  * [Cookies and Sessions](#cookies-and-sessions)
  * [XSS](#xss)
  * [SQL Injection](#sql-injection)
  * [Burp Suite](#burp-suite)
* [Wireless Security](#wireless-security)

  * [Wireless Basics](#wireless-basics)
  * [Aircrack-ng](#aircrack-ng)
  * [Airgeddon](#airgeddon)
  * [Fern WiFi Cracker](#fern-wifi-cracker)
* [Cryptography](#cryptography)
* [Windows and Active Directory](#windows-and-active-directory)
* [Defensive Security](#defensive-security)
* [Reverse Engineering](#reverse-engineering)
* [Binary Exploitation](#binary-exploitation)
* [CTFs and Practice](#ctfs-and-practice)
* [Useful Tools](#useful-tools)
* [Learning Roadmap](#learning-roadmap)
* [Final Advice](#final-advice)

---

## About

This repository is my collection of notes, explanations and resources for learning cybersecurity.

The goal is simple:

> Learn how computers, networks and applications work, understand how they can be attacked, and learn how to secure them.

This guide is written for people who are starting out.

You do not need to know everything before beginning. In fact, you probably won't.

Cybersecurity is a massive field. There are people who spend years focusing on one tiny part of it, so don't worry if some of the advanced sections look confusing at first.

Start with the basics, practise in safe environments, and slowly build from there.

---

## Important: Read This First

Everything in this guide should be used for:

* Your own computers
* Your own networks
* Virtual machines
* Intentionally vulnerable applications
* CTFs
* Cybersecurity training platforms
* Systems where you have explicit permission to test

Do not use security tools against random websites, WiFi networks, servers or devices simply because they are visible.

Having a tool does not mean you have permission to use it against someone else's system.

If you are learning, the easiest option is to build your own lab.

That way you can break things, fix them, break them again and learn without accidentally causing someone else problems.

---

# What You Will Learn

This guide covers:

```text
Linux
  |
  +-- Bash
  |
  +-- Networking
  |
  +-- Python
  |
  +-- Reconnaissance
  |
  +-- Enumeration
  |
  +-- Web Security
  |
  +-- Wireless Security
  |
  +-- Cryptography
  |
  +-- Windows / Active Directory
  |
  +-- Defensive Security
  |
  +-- Reverse Engineering
  |
  +-- Binary Exploitation
  |
  +-- CTFs
```

You don't have to learn all of this.

Cybersecurity has loads of different career paths. Someone interested in web applications does not necessarily need to become an expert in binary exploitation.

---

# Distro

## Linux Distros for Hacking

There are loads of Linux distributions that can be used for cybersecurity.

Some are specifically designed for penetration testing, while others are normal desktop distributions that you can configure yourself.

There isn't one magical "hacking OS".

The operating system is just the environment.

Understanding Linux is much more important than the distro you choose.

---

## ParrotOS

<details>
<summary>Read about ParrotOS</summary>

### What is it?

ParrotOS is a Debian-based Linux distribution designed around security, privacy, development and everyday use.

The Security Edition comes with a large collection of security tools already installed.

Parrot also has a Home Edition aimed more towards everyday computing and development.

### Pros

* Large collection of security tools
* Debian-based
* Good for learning Linux
* Can be used as a normal desktop
* Security and privacy focused
* Works well in virtual machines
* Good choice for people who want security tools without giving up normal desktop functionality

### Cons

* Some tools take time to understand
* You still need to understand Linux
* Having hundreds of tools installed does not mean you know how to use them
* Some tools require additional configuration

### Why I use it

I use ParrotOS because it gives me a comfortable Linux desktop while still giving me access to a large security toolkit.

It feels less like I'm using a computer that exists purely for penetration testing and more like I'm using a normal computer that happens to have a lot of security tools available.

</details>

---

## Kali Linux

<details>
<summary>Read about Kali Linux</summary>

### What is it?

Kali Linux is a Debian-based Linux distribution designed specifically for penetration testing and security auditing.

It is extremely common in cybersecurity labs, CTFs and professional penetration-testing environments.

### Pros

* Huge security-tool ecosystem
* Excellent documentation
* Very popular in cybersecurity
* Lots of tutorials and learning material
* Excellent support for virtual machines
* Designed specifically around security work

### Cons

* Can be confusing for complete Linux beginners
* Many tools have specialised purposes
* Not every tool is useful to every person
* Installing Kali does not automatically teach you penetration testing

### Important

Kali's own documentation assumes some previous Linux knowledge.

Don't feel like you need Kali just because someone online says "real hackers use Kali".

Use the distro that helps you learn.

</details>

---

## BlackArch

<details>
<summary>Read about BlackArch</summary>

### What is it?

BlackArch is an Arch Linux-based distribution focused heavily on penetration testing and security research.

It provides a very large collection of security tools.

### Pros

* Massive tool collection
* Highly customisable
* Arch Linux ecosystem
* Excellent for experienced Linux users
* Good for security research

### Cons

* Steep learning curve
* Requires more Linux knowledge
* Configuration can take time
* Probably unnecessary for someone who is completely new to Linux

### Who is it for?

I'd mainly recommend looking at BlackArch once you are already comfortable with Linux and Arch.

There is no point making life harder just for the sake of it.

</details>

---

## Ubuntu

<details>
<summary>Read about Ubuntu</summary>

### What is it?

Ubuntu is a general-purpose Linux distribution.

It isn't specifically a hacking distro, but that doesn't make it useless for cybersecurity.

In fact, learning cybersecurity on a normal Linux installation can be useful because you learn how to install and configure the tools yourself.

### Pros

* Beginner friendly
* Huge community
* Lots of documentation
* Great for programming
* Great for everyday use
* Easy to turn into a security lab

### Cons

* Security tools aren't installed by default
* You need to configure your environment
* Less security-focused out of the box

### Who is it for?

If you're completely new to Linux, Ubuntu can be a great starting point.

You can learn Linux first and then move to Parrot or Kali later if you actually need them.

</details>

---

## Quick Comparison

| Distro         | Main Focus           | Beginner Friendly |   Security Tools | Daily Use |
| -------------- | -------------------- | ----------------: | ---------------: | --------: |
| **ParrotOS**   | Security + daily use |              High |        Extensive | Excellent |
| **Kali Linux** | Penetration testing  |          Moderate |        Extensive |      Good |
| **BlackArch**  | Security research    |               Low |        Extensive |  Moderate |
| **Ubuntu**     | General computing    |         Excellent | Install yourself | Excellent |

---

# Setting Up a Hacking Lab

Before doing anything serious, build a lab.

A simple setup could look like this:

```text
Your Computer
      |
      +----------------------+
      |                      |
      v                      v
Security VM              Target VM
      |                      |
 Parrot / Kali       Intentionally vulnerable
                         application
```

Your security VM is where you practise.

Your target VM is where you attack.

Keep the lab isolated and only use intentionally vulnerable targets.

---

## Virtualisation

Common virtualisation platforms include:

* VirtualBox
* VMware
* Hyper-V
* UTM
* Proxmox

A VM gives you a safe environment that you can destroy and rebuild whenever you want.

That's extremely useful when learning.

---

## Lab Targets

Good training targets include intentionally vulnerable applications and machines designed for security education.

Examples include:

* OWASP Juice Shop
* DVWA
* Metasploitable
* WebGoat
* CTF machines
* Purpose-built training environments

---

# Linux Fundamentals

If you want to understand hacking, learn Linux.

You don't need to memorise hundreds of commands.

You need to understand what the commands are actually doing.

---

## Files and Directories

Some basic commands:

```bash
pwd
ls
cd
mkdir
touch
cp
mv
rm
cat
less
```

For example:

```bash
pwd
```

shows your current directory.

```bash
ls
```

shows the files in the current directory.

```bash
cd Documents
```

moves into the Documents directory.

---

## Permissions

Linux permissions determine who can read, write and execute files.

You will commonly see something like:

```text
-rwxr-xr--
```

The three main permission groups are:

```text
Owner
Group
Others
```

And the main permissions are:

```text
r = read
w = write
x = execute
```

---

## Users and Groups

Learn:

```bash
whoami
id
groups
sudo
su
```

Understanding users and privileges becomes extremely important later.

A huge amount of security comes down to one question:

> "What is this user actually allowed to do?"

---

## Processes

Useful commands include:

```bash
ps
top
htop
kill
systemctl
```

Processes are simply programs that are currently running.

Understanding processes helps with troubleshooting, system administration and security investigations.

---

# Bash

Bash is the default shell on many Linux systems.

Learning Bash lets you automate repetitive tasks.

Start with:

```bash
echo
variables
if statements
loops
functions
pipes
redirection
```

For example:

```bash
cat access.log | grep "404"
```

This takes the contents of a log file and searches it for HTTP 404 responses.

That's the kind of simple automation that becomes extremely useful in security.

---

# Networking Fundamentals

Before learning penetration testing, learn networking.

Seriously.

If you don't understand networking, security tools will eventually just look like magic commands.

They aren't magic.

They're doing networking.

---

## IP Addresses

An IP address identifies a device on a network.

Example:

```text
192.168.1.20
```

IPv4 addresses contain four numbers separated by dots.

IPv6 uses a different format and provides a much larger address space.

---

## MAC Addresses

A MAC address identifies a network interface at the link layer.

Example:

```text
00:11:22:33:44:55
```

MAC addresses are commonly associated with Ethernet and WiFi interfaces.

---

## Ports

A port helps identify a network service.

Examples:

```text
22   SSH
53   DNS
80   HTTP
443  HTTPS
```

A port being open does not automatically mean a machine is vulnerable.

It simply means something is listening there.

---

## TCP and UDP

TCP focuses on reliable, connection-oriented communication.

UDP is connectionless and has less overhead.

You don't need to memorise every detail immediately.

Just understand why different protocols exist and when they are used.

---

## DNS

DNS translates names into addresses.

For example:

```text
example.com
      |
      v
IP address
```

Useful tools include:

```bash
dig
nslookup
host
```

---

## HTTP and HTTPS

HTTP is the protocol used by the web.

HTTPS is HTTP protected using TLS.

Understanding HTTP is extremely important if you want to learn web security.

---

## Useful Networking Commands

```bash
ip
ss
ping
traceroute
curl
dig
nslookup
tcpdump
```

---

# Reconnaissance

Reconnaissance is the information-gathering stage.

The basic idea is:

> Learn what you're dealing with before trying to test it.

There are two broad categories.

### Passive Reconnaissance

You gather information without directly interacting with the target system.

Examples:

* Public DNS information
* Public documents
* Public technology information
* Search engines
* Publicly available records

### Active Reconnaissance

You directly interact with the system.

Examples:

* Service discovery
* Port scanning
* HTTP requests
* Network enumeration

Only perform active reconnaissance against systems you have permission to test.

---

# Scanning and Enumeration

Scanning tells you what is available.

Enumeration goes a step further and tries to understand those services.

For example:

```text
Scan
 |
 +-- Port 22 open
 |
 +-- Port 80 open
 |
 +-- Port 443 open
```

You then investigate what those services actually are.

---

## Nmap

Nmap is one of the most important tools to learn.

It can help identify:

* Hosts
* Open ports
* Services
* Service versions
* Operating-system information

The important thing isn't memorising Nmap commands.

Understand what the scan is telling you.

Only scan systems you own or have permission to test.

---

# Web Security

Web applications are one of the most interesting areas of cybersecurity.

Before learning vulnerabilities, understand how websites actually work.

---

# HTTP

A basic HTTP request looks conceptually like:

```text
Client
  |
  | HTTP Request
  v
Server
  |
  | HTTP Response
  v
Client
```

A request can contain:

* Method
* URL
* Headers
* Cookies
* Parameters
* Body

Common methods include:

```text
GET
POST
PUT
PATCH
DELETE
```

---

# Cookies and Sessions

Websites often need to remember who you are.

Cookies can help with this.

For example:

```text
Login
  |
  v
Server creates session
  |
  v
Browser receives session cookie
  |
  v
Browser sends cookie with future requests
```

Understanding authentication and sessions is essential for understanding web vulnerabilities.

---

# XSS

XSS stands for Cross-Site Scripting.

The basic idea is that an attacker-controlled piece of input ends up being interpreted as JavaScript by another user's browser.

There are several types.

### Reflected XSS

The malicious input is immediately reflected in a response.

### Stored XSS

The malicious content is stored by the application and later shown to users.

### DOM-based XSS

The vulnerability exists in client-side JavaScript and how it handles user-controlled data.

---

## Why XSS Matters

XSS can potentially allow an attacker to perform actions in the context of another user's browser.

The exact impact depends on the application and its security controls.

The best way to learn XSS is through intentionally vulnerable applications such as training labs.

---

## How to Prevent XSS

Common defensive techniques include:

* Context-aware output encoding
* Input validation where appropriate
* Avoiding unsafe DOM APIs
* Content Security Policy
* Secure framework defaults
* Proper handling of HTML, JavaScript and URL contexts

Don't think of XSS as simply "put JavaScript in a textbox".

The real lesson is understanding how untrusted data moves through an application.

---

# SQL Injection

SQL injection happens when untrusted input is incorrectly included in SQL queries.

A simplified vulnerable example might look like:

```text
SELECT * FROM users
WHERE username = 'INPUT';
```

If an application directly inserts user input into SQL, the user may be able to alter the meaning of the query.

---

## Why SQL Injection Matters

Depending on the application and database permissions, SQL injection can potentially affect:

* Authentication
* Data confidentiality
* Data integrity
* Database contents
* Application behaviour

The impact depends heavily on how the application is built.

---

## How to Prevent SQL Injection

The most important defence is:

> Use parameterised queries / prepared statements.

Other useful controls include:

* Least-privilege database accounts
* Input validation
* Safe ORM usage
* Proper error handling
* Security testing

Do not rely on hiding database errors as your main defence.

---

# Burp Suite

Burp Suite is a web security testing platform.

It can help you understand and modify HTTP traffic between a browser and a web application.

Common features include:

* Proxy
* Repeater
* Intruder
* Decoder
* HTTP history
* Site map

If you're learning web security, Burp is worth learning properly.

Don't just copy random payloads from the internet.

Understand the request first.

---

# Wireless Security

Wireless security is another large part of cybersecurity.

Before using wireless tools, understand:

* SSIDs
* Access points
* Clients
* Channels
* 2.4 GHz
* 5 GHz
* 6 GHz
* WPA2
* WPA3
* Authentication
* Encryption
* Monitor mode
* Packet capture

Only test networks you own or have explicit permission to assess.

---

# Aircrack-ng

Aircrack-ng is a suite of tools for assessing WiFi security.

It includes tools for areas such as:

* Wireless monitoring
* Packet capture
* Wireless testing
* Packet injection
* Security assessment
* Password auditing

Some of its tools include:

```text
airmon-ng
airodump-ng
aireplay-ng
aircrack-ng
```

---

## What the Tools Do

<details>
<summary>airmon-ng</summary>

Used to help manage wireless interfaces and monitor-mode configuration.

Monitor mode allows a compatible wireless adapter to observe wireless frames in a way that normal managed mode does not.

</details>

<details>
<summary>airodump-ng</summary>

Used for wireless packet capture and observing nearby wireless networks and clients in an authorised testing environment.

</details>

<details>
<summary>aireplay-ng</summary>

Used for wireless frame injection and replay testing.

This should only be used against networks where you have explicit permission.

</details>

<details>
<summary>aircrack-ng</summary>

Used for auditing captured wireless authentication data and testing password security.

It is not a magic button that instantly cracks every WiFi password.

The results depend on the protocol, capture data, password strength and available resources.

</details>

---

# Airgeddon

Airgeddon is a wireless auditing framework that brings different wireless security tools and workflows together.

It can help automate parts of wireless security assessments.

It is useful for learning because it gives you a more guided interface around techniques that would otherwise involve several different tools.

However, using a menu does not mean you understand what's happening underneath.

If Airgeddon performs an action, learn what that action actually does.

---

# Fern WiFi Cracker

Fern WiFi Cracker is a graphical wireless security auditing tool.

It provides a GUI for working with certain wireless assessment tasks.

It can be useful for beginners who are still getting comfortable with the command line.

Once you understand the concepts, learning the underlying tools is still worthwhile.

---

## Wireless Hardware

A normal laptop's built-in WiFi adapter may not support every feature required for wireless security testing.

Depending on what you're learning, you may need a compatible USB wireless adapter.

Look for hardware that supports the features required by your specific lab.

Don't buy an adapter simply because a random video says it is "the best hacking WiFi adapter".

Check chipset and driver compatibility first.

---

# Cryptography

Cryptography is much bigger than "encryption".

Learn the difference between:

```text
Encoding
Hashing
Encryption
Signing
```

---

## Encoding

Encoding changes data into another representation.

Example:

```text
Base64
```

Base64 is not encryption.

Anyone can decode it.

---

## Hashing

A hash function takes input and produces a fixed-size output.

Example:

```text
password
   |
   v
hash function
   |
   v
hash
```

Common examples include:

```text
SHA-256
SHA-512
```

MD5 and SHA-1 should not be treated as modern choices for security-sensitive cryptographic integrity.

---

## Encryption

Encryption is designed to protect confidentiality.

There are two major categories:

### Symmetric

The same secret key is used for encryption and decryption.

### Asymmetric

A public/private key pair is used.

---

## Digital Signatures

Digital signatures help prove:

* Who signed something
* That the content has not been modified

They are an important part of modern secure communication.

---

# Windows and Active Directory

If you want to work in cybersecurity professionally, learning Windows is important.

Linux is not the entire world.

Learn:

* Windows users
* Groups
* Permissions
* Services
* Registry
* PowerShell
* Event logs
* Windows authentication
* Active Directory
* Kerberos
* LDAP
* SMB
* Group Policy
* Domain Controllers

---

## Active Directory

Active Directory is Microsoft's directory service used to manage identities and resources in many Windows environments.

A simple environment might look like:

```text
Domain Controller
       |
       +-------- Users
       |
       +-------- Groups
       |
       +-------- Computers
       |
       +-------- Policies
```

Understanding how these pieces interact is much more valuable than memorising attack commands.

---

# Defensive Security

Cybersecurity isn't only about attacking.

A good security professional should also understand how defenders detect and prevent attacks.

Learn:

* Logging
* Monitoring
* Authentication
* Access control
* Firewalls
* Endpoint security
* Vulnerability management
* Incident response
* Threat modelling
* Security policies
* Backups
* Hardening

---

## Logs

Logs tell you what happened.

Examples:

```text
Login attempts
Network connections
Application errors
Process creation
File changes
Authentication events
```

Learn how to read logs before trying to automate analysis.

---

## SIEM

A SIEM collects and analyses security-related data.

Examples include:

* Wazuh
* Splunk
* Elastic Security

A simple workflow is:

```text
Machine
   |
   v
Logs
   |
   v
SIEM
   |
   v
Detection
   |
   v
Investigation
```

---

# Reverse Engineering

Reverse engineering is the process of analysing software to understand how it works.

You may not have the source code.

Instead, you might have:

```text
Executable
    |
    v
Disassembler
    |
    v
Assembly
    |
    v
Understanding
```

Learn:

* C
* Assembly basics
* CPU registers
* Memory
* Stack
* Heap
* Functions
* ELF files
* PE files
* Debuggers
* Disassemblers

Useful tools include:

* Ghidra
* GDB
* strings
* objdump
* radare2

---

# Binary Exploitation

Binary exploitation is an advanced area.

Do not start here.

Learn programming, Linux, memory and assembly first.

Topics include:

* Buffer overflows
* Stack memory
* Heap memory
* Memory corruption
* ASLR
* DEP/NX
* Stack canaries
* Return-oriented programming
* Debugging

The goal isn't to memorise exploitation tricks.

The goal is to understand what the computer is doing at a low level.

---

# CTFs and Practice

CTFs are one of the best ways to practise cybersecurity.

They let you work on realistic problems without attacking random systems.

Good areas to practise include:

```text
Linux
Networking
Web Security
Cryptography
Forensics
Reverse Engineering
Binary Exploitation
OSINT
```

Popular learning platforms include:

* OverTheWire
* TryHackMe
* Hack The Box
* PortSwigger Web Security Academy
* picoCTF
* pwn.college

---

# Useful Tools

Here's a basic toolkit to become familiar with.

| Tool            | Purpose                                  | Level        |
| --------------- | ---------------------------------------- | ------------ |
| Nmap            | Network/service discovery                | Beginner     |
| Wireshark       | Packet analysis                          | Beginner     |
| tcpdump         | Command-line packet capture              | Beginner     |
| Burp Suite      | Web application testing                  | Beginner     |
| OWASP ZAP       | Web application testing                  | Beginner     |
| Aircrack-ng     | Wireless security assessment             | Intermediate |
| Airgeddon       | Wireless auditing framework              | Intermediate |
| Fern            | Wireless auditing GUI                    | Beginner     |
| Metasploit      | Security testing framework               | Intermediate |
| Ghidra          | Reverse engineering                      | Advanced     |
| GDB             | Debugging                                | Advanced     |
| Hashcat         | Password auditing                        | Intermediate |
| John the Ripper | Password auditing                        | Intermediate |
| Gobuster        | Content/service discovery                | Intermediate |
| Amass           | Asset discovery                          | Intermediate |
| Nikto           | Web server assessment                    | Beginner     |
| SQLMap          | SQL injection testing in authorised labs | Intermediate |

Tools are not skills.

Knowing what a tool does, why you would use it and how to interpret its output is much more important than having 500 tools installed.

---

# Learning Roadmap

If you're completely new, don't try to learn everything at once.

Use this order.

## Stage 1 — Linux

Learn:

```text
Files
Permissions
Users
Processes
Packages
Networking
Bash
SSH
```

---

## Stage 2 — Networking

Learn:

```text
IP
MAC
TCP
UDP
DNS
DHCP
HTTP
HTTPS
Ports
Subnets
Routing
NAT
Firewalls
```

---

## Stage 3 — Programming

Start with:

```text
Python
Bash
Basic JavaScript
Basic SQL
Basic HTML
```

You don't need to become a software engineer.

You just need to be comfortable reading and writing code.

---

## Stage 4 — Security Fundamentals

Learn:

```text
Authentication
Authorisation
Encryption
Hashing
Vulnerabilities
Threat modelling
Logging
Least privilege
Defence in depth
```

---

## Stage 5 — Recon and Enumeration

Learn:

```text
Nmap
DNS enumeration
Service enumeration
HTTP enumeration
Basic OSINT
```

---

## Stage 6 — Web Security

Learn:

```text
HTTP
Cookies
Sessions
Authentication
Access control
XSS
SQL injection
CSRF
SSRF
Path traversal
File upload vulnerabilities
Security headers
APIs
```

Use dedicated web-security labs.

---

## Stage 7 — Wireless

Learn:

```text
802.11 basics
WiFi authentication
WPA2
WPA3
Packet capture
Monitor mode
Aircrack-ng
Airgeddon
Fern
```

Practise only against your own lab network.

---

## Stage 8 — Windows

Learn:

```text
Windows administration
PowerShell
Users
Groups
Permissions
Event logs
Active Directory
Kerberos
LDAP
SMB
Group Policy
```

---

## Stage 9 — Advanced Topics

Once your fundamentals are solid:

```text
Reverse engineering
Assembly
Binary exploitation
Malware analysis
Exploit development
Advanced Active Directory
Cloud security
Container security
Mobile security
```

---

# A Simple Weekly Plan

If you're learning alongside school, work or life, you don't need to spend twelve hours a day on it.

Something like this is enough:

```text
Monday
Linux

Tuesday
Networking

Wednesday
Python

Thursday
Web security

Friday
Linux / networking revision

Saturday
CTF or security lab

Sunday
Review notes
```

The important bit is consistency.

Doing two hours every week for a year will teach you far more than downloading Kali, watching three "TOP 10 HACKING TOOLS" videos and never touching it again.

---

# Common Beginner Mistakes

<details>
<summary>Installing Kali and thinking you're a hacker</summary>

Installing a security distro doesn't give you cybersecurity knowledge.

It's just an operating system with a collection of tools.

Learn the fundamentals underneath the tools.

</details>

<details>
<summary>Copying commands without understanding them</summary>

If you copy a command from a tutorial, stop and understand each part.

Ask:

```text
What does this command do?
Why am I running it?
What does the output mean?
What could go wrong?
```

</details>

<details>
<summary>Trying to learn everything at once</summary>

Cybersecurity is massive.

You do not need to learn Linux, web security, malware analysis, WiFi, Active Directory, reverse engineering and cloud security in your first month.

Pick one subject and get comfortable with it.

</details>

<details>
<summary>Ignoring networking</summary>

This one will catch you out eventually.

Learn networking properly.

It makes almost every other security topic easier.

</details>

<details>
<summary>Only learning offensive security</summary>

Learn defence too.

Understanding how defenders detect attacks makes you better at understanding attacks in the first place.

</details>

---

# Final Advice

Don't worry about trying to look like a hacker.

You don't need a black terminal, a ridiculous username and twelve monitors.

You need curiosity.

Learn how something works.

Break it in a lab.

Figure out why it broke.

Fix it.

Then try again.

That's basically the entire game.

The tools will change.

The Linux distributions will change.

Vulnerabilities will change.

The fundamentals will stick around.

If you understand operating systems, networking, programming, authentication, web applications and how computers communicate, you'll always have something to build on.

Most importantly, practise legally.

Build your own lab, use CTFs and training platforms, and only test systems when you have permission.

Learn the fundamentals first.

The fancy tools can wait.

---

## Useful Official Documentation

For keeping this guide up to date, check the official documentation for the projects and tools you use.

* ParrotOS documentation
* Kali Linux documentation
* OWASP documentation
* Aircrack-ng documentation
* Burp Suite documentation
* Wireshark documentation
* Ghidra documentation
* Nmap documentation

This README is intended as a learning roadmap rather than a replacement for the documentation of individual projects.
