<div align="center">
  <img src="./assets/typewriter-cameroncodesstuff.gif" alt="Typewriter Animation" />

  <h1>Hacking & Cybersecurity Guide</h1>

  <p>
    A beginner-friendly guide to Linux, networking, programming,
    cybersecurity, penetration testing, web security, wireless security,
    digital forensics, reverse engineering and defensive security.
  </p>
</div>

---

# Table of Contents

* [About](#about)
* [Important: Read This First](#important-read-this-first)
* [How to Use This Guide](#how-to-use-this-guide)
* [Cybersecurity Fundamentals](#cybersecurity-fundamentals)
* [Computer Fundamentals](#computer-fundamentals)
* [Linux](#linux)

  * [Choosing a Distro](#choosing-a-distro)
  * [Linux Filesystem](#linux-filesystem)
  * [Users and Groups](#users-and-groups)
  * [Permissions](#permissions)
  * [Processes](#processes)
  * [Services](#services)
  * [Packages](#packages)
  * [Logs](#logs)
* [Bash](#bash)
* [Networking](#networking)

  * [IP Addresses](#ip-addresses)
  * [MAC Addresses](#mac-addresses)
  * [Ports](#ports)
  * [TCP and UDP](#tcp-and-udp)
  * [DNS](#dns)
  * [DHCP](#dhcp)
  * [NAT](#nat)
  * [Firewalls](#firewalls)
  * [HTTP and HTTPS](#http-and-https)
  * [Wireshark](#wireshark)
* [Programming](#programming)

  * [Python](#python)
  * [JavaScript](#javascript)
  * [SQL](#sql)
  * [Git and GitHub](#git-and-github)
* [Lab Setup](#lab-setup)
* [Reconnaissance](#reconnaissance)
* [Scanning and Enumeration](#scanning-and-enumeration)
* [Web Security](#web-security)

  * [HTTP](#web-http)
  * [Cookies and Sessions](#cookies-and-sessions)
  * [Authentication](#authentication)
  * [Authorisation](#authorisation)
  * [XSS](#xss)
  * [SQL Injection](#sql-injection)
  * [CSRF](#csrf)
  * [SSRF](#ssrf)
  * [Path Traversal](#path-traversal)
  * [File Upload Security](#file-upload-security)
  * [Security Headers](#security-headers)
  * [API Security](#api-security)
  * [JWT](#jwt)
  * [Burp Suite](#burp-suite)
* [Wireless Security](#wireless-security)

  * [WiFi Fundamentals](#wifi-fundamentals)
  * [WPA2 and WPA3](#wpa2-and-wpa3)
  * [Monitor Mode](#monitor-mode)
  * [Aircrack-ng](#aircrack-ng)
  * [Airgeddon](#airgeddon)
  * [Fern WiFi Cracker](#fern-wifi-cracker)
  * [Wireless Lab](#wireless-lab)
* [Cryptography](#cryptography)
* [Password Security](#password-security)
* [Windows](#windows)
* [Active Directory](#active-directory)
* [PowerShell](#powershell)
* [OSINT](#osint)
* [Vulnerability Management](#vulnerability-management)
* [Threat Modelling](#threat-modelling)
* [MITRE ATT&CK](#mitre-attck)
* [Digital Forensics](#digital-forensics)
* [Malware Analysis](#malware-analysis)
* [YARA](#yara)
* [Sigma](#sigma)
* [Defensive Security](#defensive-security)
* [SIEM](#siem)
* [Incident Response](#incident-response)
* [Reverse Engineering](#reverse-engineering)
* [Assembly](#assembly)
* [Binary Exploitation](#binary-exploitation)
* [Cloud Security](#cloud-security)
* [Container Security](#container-security)
* [Mobile Security](#mobile-security)
* [IoT Security](#iot-security)
* [CTFs and Practice](#ctfs-and-practice)
* [Projects](#projects)
* [Tool Reference](#tool-reference)
* [Troubleshooting](#troubleshooting)
* [Common Beginner Mistakes](#common-beginner-mistakes)
* [Learning Roadmap](#learning-roadmap)
* [Glossary](#glossary)
* [Final Advice](#final-advice)

---

# About

This repository is my collection of notes and resources for learning cybersecurity.

The goal is pretty simple:

> Understand how computers work, understand how security problems happen, learn how to find them in controlled environments, and learn how to fix them.

Cybersecurity is a massive subject.

You can spend years specialising in one tiny area, so don't worry about knowing everything.

This guide starts with the fundamentals and gradually moves towards more advanced subjects.

You don't need to follow every section.

If web security interests you, go deeper into web security.

If reverse engineering interests you, follow that path.

If defensive security interests you, spend more time learning detection and incident response.

The important thing is understanding what you're doing rather than collecting tools.

---

# Important: Read This First

Everything here is intended for **legal and authorised security testing**.

Use these techniques against:

* Your own computers
* Your own networks
* Virtual machines
* Intentionally vulnerable applications
* CTF challenges
* Security training platforms
* Systems where you have explicit permission to test

Do not scan or attack random websites, servers, WiFi networks or devices because they happen to be accessible.

A publicly accessible system is not automatically a system you're allowed to test.

For wireless testing especially, use a dedicated network and equipment you control.

A good cybersecurity learner should be able to experiment without putting other people's systems, data or networks at risk.

---

# How to Use This Guide

Don't try to memorise everything.

For each subject, use this process:

```text
Learn the concept
       |
       v
Understand how it works
       |
       v
Practise in a lab
       |
       v
Break something intentionally
       |
       v
Figure out why it broke
       |
       v
Fix it
       |
       v
Document what happened
```

If you're copying commands without understanding them, slow down.

Ask yourself:

```text
What does this command do?

Why am I running it?

What information does it give me?

What assumptions does it make?

What could go wrong?

How would I defend against the underlying problem?
```

That's where the actual learning happens.

---

# Cybersecurity Fundamentals

Before getting into tools, understand some basic security concepts.

## Asset

Something worth protecting.

Examples:

* A laptop
* A database
* A user account
* Customer information
* Source code
* A server

## Threat

Something that could cause harm.

A threat could be:

* Malware
* A compromised account
* A malicious insider
* A vulnerable application
* A misconfigured service

## Vulnerability

A weakness that could be abused.

## Risk

Risk is about the potential impact and likelihood associated with a threat exploiting a weakness.

A vulnerability doesn't automatically mean a catastrophic incident will happen.

Context matters.

## Attack Surface

The attack surface is the collection of places where a system can potentially be interacted with.

For a web application this might include:

```text
Website
API
Login page
File upload
Admin panel
Third-party integrations
```

Reducing unnecessary attack surface is an important security principle.

---

# Computer Fundamentals

Cybersecurity gets much easier when you understand computers.

Learn these concepts before going deep into exploitation:

* CPU
* RAM
* Storage
* Processes
* Threads
* Operating systems
* Kernels
* Filesystems
* System calls
* Networking
* Compilers
* Interpreters
* Machine code

---

## CPU

The CPU executes instructions.

At a very simplified level:

```text
Instruction
    |
    v
CPU
    |
    +-- Registers
    |
    +-- Arithmetic
    |
    +-- Control
```

You don't need to become an electrical engineer.

You just need to understand what the CPU is doing with the instructions a program gives it.

---

## RAM

RAM is working memory.

Running programs use memory for things such as:

* Code
* Variables
* Objects
* Buffers
* Stack data
* Heap data

This becomes extremely important when learning reverse engineering and binary exploitation.

---

## Processes

A process is a running instance of a program.

A process normally has things such as:

* Memory
* Permissions
* Environment
* Open files
* Network connections
* A user identity

Security tools often inspect processes to understand what a system is doing.

---

## Kernel vs User Space

The kernel is responsible for managing core system resources.

Normal applications generally run in user space.

```text
User Applications
       |
       v
System Calls
       |
       v
Kernel
       |
       v
Hardware
```

This separation is an important security boundary.

---

# Linux

Linux is one of the most useful operating systems to learn for cybersecurity.

You don't need to know every command.

You need to understand the system.

---

# Choosing a Distro

## ParrotOS

ParrotOS is Debian-based and focuses on security, privacy, development and everyday computing.

### Strengths

* Security tools
* Debian ecosystem
* Good desktop experience
* Useful for security labs
* Suitable for everyday use

### Weaknesses

* Some tools need configuration
* Security tools can be confusing at first
* Installing the tools doesn't teach you what they do

### Why I use it

I like ParrotOS because it gives me a practical desktop while still having a security-focused environment.

---

## Kali Linux

Kali Linux is a Debian-based distribution designed around penetration testing and security auditing.

### Strengths

* Large security toolkit
* Extensive documentation
* Popular in training
* Good virtual-machine support

### Weaknesses

* Can be overwhelming for beginners
* Many tools have specialised purposes
* Requires Linux knowledge

Kali is useful, but you don't need it to learn cybersecurity.

---

## BlackArch

BlackArch is an Arch Linux-based security distribution.

### Strengths

* Huge tool collection
* Highly customisable
* Arch ecosystem

### Weaknesses

* Steeper learning curve
* Requires more Linux knowledge
* Can involve more configuration

It makes more sense once you're already comfortable with Linux.

---

## Ubuntu

Ubuntu is a general-purpose Linux distribution.

It doesn't come with a huge security toolkit by default.

That's not necessarily a bad thing.

Learning how to install and configure your own tools can actually teach you more about Linux.

---

## Quick Comparison

| Distro     | Main Focus          | Beginner Friendly |   Security Tools | Daily Use |
| ---------- | ------------------- | ----------------: | ---------------: | --------: |
| ParrotOS   | Security + desktop  |              High |        Extensive | Excellent |
| Kali Linux | Penetration testing |          Moderate |        Extensive |      Good |
| BlackArch  | Security research   |               Low |        Extensive |  Moderate |
| Ubuntu     | General computing   |         Excellent | Install yourself | Excellent |

---

# Linux Filesystem

Important directories:

| Directory | Purpose                        |
| --------- | ------------------------------ |
| `/`       | Root of the filesystem         |
| `/home`   | User home directories          |
| `/etc`    | Configuration                  |
| `/var`    | Variable data and logs         |
| `/tmp`    | Temporary files                |
| `/usr`    | Applications and libraries     |
| `/dev`    | Device files                   |
| `/proc`   | Process and kernel information |

Useful commands:

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
find
```

---

# Users and Groups

Linux uses users and groups to control access.

Useful commands:

```bash
whoami
id
groups
```

The security principle to remember is:

> Give users and programs only the permissions they actually need.

This is called **least privilege**.

---

# Permissions

Linux permissions normally contain:

```text
r = read
w = write
x = execute
```

For:

```text
owner
group
others
```

Example:

```text
-rwxr-xr--
```

The owner can read, write and execute.

The group can read and execute.

Everyone else can read.

---

# Processes

Useful commands:

```bash
ps
top
htop
kill
```

When investigating a system, useful questions include:

* Which processes are running?
* Who owns them?
* What files do they access?
* What network connections do they have?
* Are they expected?

---

# Services

Services run in the background and provide functionality.

On many Linux systems:

```bash
systemctl status <service>
```

can show service status.

Every unnecessary service can increase the attack surface.

---

# Packages

Debian-based distributions commonly use:

```bash
apt
```

Arch-based distributions commonly use:

```bash
pacman
```

Be careful about what repositories and packages you trust.

Don't install random scripts from the internet with administrator privileges.

---

# Logs

Linux logs are often stored under:

```text
/var/log
```

Logs can contain:

* Authentication events
* Service failures
* Application activity
* Network events
* System errors

Learning to read logs is useful for both administration and security investigations.

---

# Bash

Bash is a shell commonly used on Linux.

Learn:

* Commands
* Variables
* Pipes
* Redirection
* Conditions
* Loops
* Functions
* Exit codes
* Environment variables

Example:

```bash
cat access.log | grep "404"
```

This searches a log for HTTP 404 responses.

---

## Bash Safety

Be particularly careful with:

```text
eval
sudo
rm
curl | bash
Unquoted variables
Commands constructed from user input
```

Never blindly execute commands you found online.

Read them first.

---

# Networking

Networking is one of the most important foundations in cybersecurity.

If networking doesn't make sense, security tools can look like random wizardry.

They're not.

They're interacting with networks.

---

# IP Addresses

IPv4 addresses look like:

```text
192.168.1.20
```

IPv6 uses hexadecimal notation and provides a much larger address space.

An IP address identifies a network endpoint.

It does not automatically identify a human being.

---

# MAC Addresses

A MAC address identifies a network interface at the link layer.

Example:

```text
00:11:22:33:44:55
```

---

# Ports

Ports identify services on a host.

Common examples:

| Port | Typical Service |
| ---: | --------------- |
|   22 | SSH             |
|   53 | DNS             |
|   80 | HTTP            |
|  443 | HTTPS           |
|   25 | SMTP            |
|  445 | SMB             |

An open port isn't automatically a vulnerability.

It means something is listening.

You still need to understand what that service is and how it is configured.

---

# TCP and UDP

TCP is connection-oriented and provides reliable delivery.

UDP is connectionless and has less protocol overhead.

Different applications choose different protocols depending on what they need.

---

# DNS

DNS translates names into network information.

Conceptually:

```text
example.test
     |
     v
DNS
     |
     v
IP address
```

Useful commands:

```bash
dig example.test
nslookup example.test
host example.test
```

---

# DHCP

DHCP allows devices to obtain network configuration automatically.

A typical device may receive:

* IP address
* Subnet mask
* Default gateway
* DNS server

---

# NAT

Network Address Translation allows networks to translate between address spaces.

A common home setup looks like:

```text
Laptop: 192.168.1.20
Phone:  192.168.1.21
              |
              v
           Router
              |
              v
           Internet
```

The router handles traffic between the private network and the internet.

---

# Firewalls

A firewall controls network traffic according to rules.

Rules might consider:

* Source
* Destination
* Port
* Protocol
* Interface
* Application

A firewall is only as good as its configuration.

---

# HTTP and HTTPS

HTTP is the protocol used by web applications.

HTTPS is HTTP protected with TLS.

A basic flow:

```text
Browser
   |
   | HTTP request
   v
Web Server
   |
   | HTTP response
   v
Browser
```

Understanding this flow is essential for web security.

---

# Wireshark

Wireshark allows you to inspect captured network traffic.

Use it on your own lab traffic.

Learn to identify:

* TCP handshakes
* DNS queries
* HTTP requests
* TLS traffic
* Source and destination addresses
* Ports
* Protocols

Don't just stare at packets.

Ask what the packet means in the context of the application.

---

# Programming

You don't need to become a software engineer.

But understanding code makes cybersecurity significantly easier.

Learn:

* Python
* Bash
* JavaScript basics
* HTML basics
* SQL
* C basics

---

# Python

Python is useful for:

* Automation
* Log parsing
* HTTP
* File analysis
* Data processing
* Security utilities
* CTF challenges

---

## Python Basics

Learn:

```text
Variables
Strings
Lists
Dictionaries
Loops
Functions
Exceptions
Files
Modules
JSON
Regular expressions
```

Example:

```python
with open("access.log", "r", encoding="utf-8") as file:
    for line in file:
        if "404" in line:
            print(line.strip())
```

Simple scripts like this can remove repetitive manual work.

---

# JavaScript

JavaScript is especially important for web security.

Learn:

* Variables
* Functions
* Objects
* Arrays
* DOM
* Events
* Fetch
* JSON
* Browser storage

Understanding JavaScript makes XSS and DOM-based vulnerabilities much easier to understand.

---

# SQL

SQL is used to interact with relational databases.

Basic concepts:

```sql
SELECT
FROM
WHERE
INSERT
UPDATE
DELETE
JOIN
ORDER BY
GROUP BY
```

A simple query:

```sql
SELECT username FROM users;
```

The security lesson is particularly important:

> SQL should treat user input as data, not executable query structure.

This is why parameterised queries are so important.

---

# Git and GitHub

Git is used to track code changes.

Learn:

```text
repositories
commits
branches
merges
pull requests
```

Security topics include:

* SSH keys
* Personal access tokens
* Secret scanning
* Dependency security
* Repository permissions
* Branch protection

Never commit:

```text
Passwords
API keys
Private keys
Cloud credentials
Session tokens
Database credentials
.env files containing secrets
```

A `.gitignore` file helps prevent accidental commits, but it doesn't erase secrets that have already entered Git history.

---

# Lab Setup

A lab gives you somewhere safe to experiment.

A simple setup:

```text
                    Your Computer
                         |
                  Virtualisation
                         |
              +----------+----------+
              |                     |
              v                     v
        Security VM             Target VM
       Parrot / Kali       Vulnerable application
```

Useful virtualisation platforms:

* VirtualBox
* VMware
* Hyper-V
* UTM
* Proxmox

---

## Useful Lab Targets

Consider:

* OWASP Juice Shop
* DVWA
* WebGoat
* Metasploitable
* CTF machines
* Purpose-built vulnerable VMs

---

## Lab Rules

1. Keep vulnerable systems isolated.
2. Take snapshots.
3. Use fake accounts and test data.
4. Never expose deliberately vulnerable systems publicly.
5. Keep notes.
6. Reset systems when necessary.

---

# Reconnaissance

Recon means information gathering.

The basic idea:

> Understand the target before testing it.

There are two broad categories.

## Passive Recon

Information is gathered without directly probing the target.

Examples:

* Public documentation
* Public DNS information
* Certificate transparency
* Public code repositories
* Public metadata

## Active Recon

You directly interact with the target.

Examples:

* Port scanning
* Service discovery
* HTTP requests
* Network enumeration

Active reconnaissance should only be performed with permission.

---

# Scanning and Enumeration

Scanning tells you what exists.

Enumeration tries to understand what you found.

Example:

```text
Host
 |
 +-- 22/tcp
 |
 +-- 80/tcp
 |
 +-- 443/tcp
```

You then investigate what those services are.

---

# Nmap

Nmap is commonly used for network and service discovery.

It can help identify:

* Hosts
* Open ports
* Services
* Service versions
* Operating-system information

The important part isn't memorising commands.

It's understanding the output.

If you find an open service, ask:

```text
What is it?
Why is it exposed?
Who owns it?
What version is it?
Is it expected?
What security controls protect it?
```

Only scan authorised systems.

---

# Web Security

Web security is one of the largest areas in cybersecurity.

Learn the web before learning web vulnerabilities.

Recommended order:

```text
HTTP
 |
Cookies
 |
Sessions
 |
Authentication
 |
Authorisation
 |
Input handling
 |
XSS / SQL Injection
 |
Other vulnerabilities
 |
Secure development
```

---

# Web HTTP

An HTTP request contains things such as:

```text
Method
URL / path
Headers
Cookies
Parameters
Body
```

Common methods:

```text
GET
POST
PUT
PATCH
DELETE
```

A response contains:

```text
Status code
Headers
Body
```

Common status codes:

|    Code | Meaning                 |
| ------: | ----------------------- |
|     200 | Success                 |
| 301/302 | Redirect                |
|     400 | Bad request             |
|     401 | Authentication required |
|     403 | Forbidden               |
|     404 | Not found               |
|     500 | Server error            |

---

# Cookies and Sessions

Web applications often need to remember users.

A simplified flow:

```text
Login
  |
  v
Server creates session
  |
  v
Browser receives cookie
  |
  v
Browser sends cookie
  |
  v
Server identifies session
```

Security depends on how sessions are generated, stored and validated.

---

# Authentication

Authentication answers:

> Who are you?

Examples:

* Password
* MFA
* Passkey
* Certificate
* Security token

Good authentication also involves secure session management.

---

# Authorisation

Authorisation answers:

> What are you allowed to do?

For example:

```text
Normal user
    |
    +-- View own profile

Administrator
    |
    +-- Manage users
```

An application can have strong authentication and still have broken authorisation.

---

# XSS

XSS stands for Cross-Site Scripting.

It occurs when untrusted input reaches a browser in a way that causes it to be interpreted as active content.

The basic idea:

```text
Untrusted input
      |
      v
Application
      |
      v
Unsafe output
      |
      v
Browser
```

---

## Reflected XSS

The input is reflected into the immediate response.

---

## Stored XSS

The input is stored by the application and later displayed to users.

---

## DOM-Based XSS

The vulnerability exists in client-side JavaScript and how it processes attacker-controlled data.

---

## Why XSS Matters

Depending on the application, XSS can affect:

* User actions
* Application data
* Session handling
* Account security
* Trust between users

The exact impact depends on the application's design and security controls.

---

## XSS Prevention

Useful defences include:

* Context-aware output encoding
* Safe DOM APIs
* Input validation where appropriate
* Content Security Policy
* Secure framework defaults
* Correct handling of HTML and JavaScript contexts

Practise XSS in training applications, not random websites.

---

# SQL Injection

SQL injection happens when untrusted input changes the meaning of a database query.

A vulnerable pattern might conceptually look like:

```text
SELECT * FROM users
WHERE username = 'INPUT';
```

If input is inserted directly into the query, the database may interpret part of the input as SQL.

---

## Why It Happens

The underlying mistake is treating:

```text
Untrusted data
```

as:

```text
Trusted SQL structure
```

---

## Potential Impact

Depending on the application and database permissions, SQL injection can affect:

* Authentication
* Data confidentiality
* Data integrity
* Database contents
* Application behaviour

---

## Prevention

Use:

* Parameterised queries
* Prepared statements
* Safe ORM APIs
* Least-privilege database accounts
* Appropriate input validation
* Safe error handling

The most important fix is separating query structure from user-controlled data.

---

# CSRF

Cross-Site Request Forgery involves tricking a user's browser into making an unwanted request to an application where the user is already authenticated.

A simplified idea:

```text
Victim logged into application
          |
          v
Malicious page
          |
          v
Browser sends unwanted request
          |
          v
Application
```

Defences include:

* CSRF tokens
* SameSite cookies
* Origin checking
* Appropriate authentication design

---

# SSRF

Server-Side Request Forgery happens when an application can be manipulated into making network requests chosen by an attacker.

The important distinction is:

```text
Attacker
   |
   v
Application
   |
   v
Internal resource
```

The server makes the request rather than the attacker's browser.

Potentially affected resources can include internal services or cloud metadata endpoints.

Defences include:

* Strict destination allowlists
* Network segmentation
* URL validation
* Blocking access to sensitive internal ranges where appropriate
* Egress controls

---

# Path Traversal

Path traversal happens when user-controlled input is used to access files without being safely constrained.

The security problem is essentially:

```text
User input
    |
    v
File path
    |
    v
Unexpected file
```

Defences include:

* Avoiding direct filesystem paths from users
* Canonicalising paths
* Allowlisting files
* Restricting application permissions
* Running services with least privilege

---

# File Upload Security

File uploads create an interesting attack surface.

Applications need to consider:

* File type
* File size
* File contents
* File names
* Storage location
* Execution permissions
* Malware scanning

Never assume that checking a filename extension alone is enough.

A safer architecture usually stores uploaded content separately from executable application code.

---

# Security Headers

HTTP security headers can provide additional browser-side protections.

Learn about:

```text
Content-Security-Policy
Strict-Transport-Security
X-Content-Type-Options
Referrer-Policy
Permissions-Policy
```

Headers are not magic.

They should support a secure application design rather than compensate for vulnerable code.

---

# API Security

APIs are a major part of modern applications.

Learn:

* REST
* JSON
* GraphQL
* API keys
* OAuth
* OpenID Connect
* JWT
* Rate limiting
* Authentication
* Authorisation
* Input validation

Common API security problems include:

* Missing authorisation checks
* Excessive data exposure
* Weak authentication
* Poor rate limiting
* Predictable object identifiers
* Unsafe input handling
* Misconfigured CORS
* Leaked secrets

---

# JWT

JWT stands for JSON Web Token.

A JWT commonly looks like:

```text
Header.Payload.Signature
```

The parts have different purposes.

### Header

Describes information about the token.

### Payload

Contains claims.

### Signature

Allows the recipient to verify that the token was signed correctly.

JWTs are not automatically secure.

Security depends on:

* Algorithm handling
* Key management
* Expiration
* Verification
* Storage
* Authorisation logic

Never assume that simply decoding a JWT gives you permission to change it.

---

# Burp Suite

Burp Suite is a platform for web security testing.

Important features include:

## Proxy

Allows you to inspect HTTP traffic from your browser.

## Repeater

Allows you to resend and modify requests.

## HTTP History

Shows requests that have passed through the proxy.

## Decoder

Helps inspect encoded data.

## Intruder

Provides automation for authorised testing.

Automation can generate significant traffic, so use it carefully.

---

# Wireless Security

Wireless security is about understanding how WiFi devices communicate and authenticate.

Learn:

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

Only test wireless networks you control.

---

# WiFi Fundamentals

A basic WiFi environment contains:

```text
Access Point
     |
     +-- Laptop
     |
     +-- Phone
     |
     +-- Test Device
```

The access point coordinates wireless communication.

Security mechanisms protect authentication and traffic.

---

# WPA2 and WPA3

WPA2 and WPA3 are security standards used by WiFi networks.

The exact authentication and encryption mechanisms depend on the network configuration.

The important learning topics are:

* Authentication
* Key establishment
* Encryption
* Protected management frames
* Password security

---

# Monitor Mode

Monitor mode allows compatible wireless hardware to observe wireless frames beyond normal client operation.

Not every wireless adapter supports all required capabilities.

Hardware and driver compatibility matters.

---

# Aircrack-ng

Aircrack-ng is a suite of tools for wireless security assessment.

Common tools include:

```text
airmon-ng
airodump-ng
aireplay-ng
aircrack-ng
```

## airmon-ng

Used to help manage wireless interfaces and monitor-mode configuration.

## airodump-ng

Used for wireless observation and packet capture.

## aireplay-ng

Supports wireless frame injection and replay testing.

## aircrack-ng

Can be used to audit captured wireless authentication material and assess password security.

It does not magically crack every network.

Results depend on:

* Wireless protocol
* Captured data
* Password strength
* Available resources

---

# Airgeddon

Airgeddon is a wireless auditing framework that combines different tools and workflows.

It can make certain lab workflows easier to navigate.

However, using a menu does not replace understanding the underlying technique.

If Airgeddon performs an action, learn what that action actually does.

---

# Fern WiFi Cracker

Fern WiFi Cracker provides a graphical interface for certain wireless auditing tasks.

It can be useful for beginners who are still becoming comfortable with the command line.

Again, understand the concepts underneath the GUI.

---

# Wireless Lab

A safe wireless lab might look like:

```text
Lab Router
    |
    +-- Test Laptop
    |
    +-- Test Phone
    |
    +-- Security VM
```

Use equipment you own.

Avoid experimenting on nearby networks.

---

# Cryptography

Cryptography is more than encryption.

Separate these concepts:

```text
Encoding
Hashing
Encryption
Digital Signatures
```

---

# Encoding

Encoding changes representation.

Base64 is an example.

```text
Text
 |
 v
Base64
 |
 v
Encoded text
```

No secret key is required.

Therefore Base64 is not encryption.

---

# Hashing

Hashing produces a fixed-size output from input.

Example:

```text
Input
  |
  v
Hash function
  |
  v
Hash
```

Common general-purpose hash functions include SHA-256 and SHA-512.

Password storage should use a password-specific hashing function such as Argon2id, bcrypt or scrypt rather than simply hashing a password with SHA-256.

---

# Encryption

Encryption protects confidentiality.

## Symmetric Encryption

Uses a shared secret key.

```text
Plaintext
   |
   v
Encryption + Key
   |
   v
Ciphertext
```

The recipient needs the appropriate key to decrypt it.

## Asymmetric Encryption

Uses a public/private key pair.

This is heavily used in modern secure communications.

---

# Digital Signatures

Digital signatures help verify:

* Authenticity
* Integrity

They are used in areas such as software signing and secure communications.

---

# TLS

TLS protects network communications.

HTTPS is HTTP over TLS.

Learn:

* Certificates
* Certificate authorities
* Public/private keys
* Handshakes
* Authentication
* Encryption

---

# Password Security

Passwords should not normally be stored as plaintext.

Learn:

* Password length
* Password uniqueness
* Password managers
* MFA
* Passkeys
* Password hashing
* Salting
* Rate limiting
* Credential stuffing
* Password spraying

---

## Password Hashing

Applications should use an appropriate password-hashing algorithm.

Common choices include:

* Argon2id
* bcrypt
* scrypt

A salt helps ensure that identical passwords don't simply result in identical stored values.

---

## Defensive Controls

Useful controls include:

* MFA
* Strong passwords
* Password managers
* Rate limiting
* Breached-password screening
* Secure password hashing
* Login monitoring

---

# Windows

Windows is extremely important in enterprise cybersecurity.

Learn:

* Users
* Groups
* Permissions
* Processes
* Services
* Registry
* PowerShell
* Event logs
* Task Scheduler
* Windows Defender
* Windows networking

---

# Active Directory

Active Directory manages identities, computers, policies and resources in many Windows environments.

A simplified layout:

```text
Domain Controller
       |
       +-- Users
       |
       +-- Groups
       |
       +-- Computers
       |
       +-- Policies
```

---

# LDAP

LDAP is used to access directory information.

It can be used to query things such as:

* Users
* Groups
* Computers
* Directory attributes

---

# Kerberos

Kerberos is an authentication protocol used heavily by Active Directory.

At a high level, it uses tickets to allow users and services to authenticate without repeatedly sending passwords across the network.

Learn:

* Tickets
* KDC
* Authentication
* Service principals
* Trust relationships

---

# SMB

SMB is commonly used for file and resource sharing on Windows networks.

Learn:

* Shares
* Permissions
* Authentication
* Network access
* Signing

---

# PowerShell

PowerShell is useful for Windows administration and security analysis.

Learn:

* Objects
* Pipelines
* Variables
* Functions
* Modules
* Event logs
* Processes
* Services

PowerShell is not simply "Windows Bash".

It works heavily with structured objects.

---

# OSINT

OSINT stands for Open-Source Intelligence.

It means gathering and analysing information from publicly available sources.

Possible sources include:

* Public websites
* DNS
* Certificate transparency
* Public documents
* Code repositories
* Public metadata
* Search engines

---

## OSINT Process

```text
Question
   |
   v
Collect
   |
   v
Verify
   |
   v
Correlate
   |
   v
Document
```

The most important step is verification.

Finding something online doesn't automatically mean it is accurate.

---

# Vulnerability Management

Not every vulnerability needs to be exploited.

A mature security process involves:

```text
Asset inventory
      |
      v
Identify vulnerabilities
      |
      v
Validate findings
      |
      v
Assess risk
      |
      v
Remediate
      |
      v
Verify the fix
```

---

# CVE

A CVE identifies a publicly documented vulnerability.

Example concept:

```text
CVE
 |
 +-- Vulnerability identifier
 +-- Description
 +-- References
```

---

# CWE

CWE describes categories of software weaknesses.

For example, injection weaknesses can be grouped into broader categories.

---

# CVSS

CVSS is used to communicate vulnerability severity using a defined scoring system.

A CVSS score is not the same thing as your organisation's overall business risk.

Context matters.

---

# Threat Modelling

Threat modelling asks:

> What could go wrong, and what can we do about it?

---

## Assets

Identify what needs protection.

Examples:

```text
Customer data
User accounts
Payment information
Source code
API keys
Servers
```

---

## Trust Boundaries

Consider:

```text
Internet
   |
   v
Web Server
   |
   v
Application
   |
   v
Database
```

Each boundary is worth examining.

---

# STRIDE

STRIDE is a threat-modelling framework.

It covers:

```text
S = Spoofing
T = Tampering
R = Repudiation
I = Information Disclosure
D = Denial of Service
E = Elevation of Privilege
```

Use frameworks to structure your thinking rather than blindly following a checklist.

---

# MITRE ATT&CK

MITRE ATT&CK is a knowledge base describing adversary behaviour.

It organises behaviour into tactics and techniques.

A simplified sequence might look like:

```text
Initial Access
      |
Execution
      |
Persistence
      |
Privilege Escalation
      |
Credential Access
      |
Discovery
      |
Lateral Movement
      |
Collection
      |
Command and Control
```

Real incidents don't necessarily follow this exact order.

ATT&CK can help defenders:

* Describe behaviour
* Map detections
* Identify security gaps
* Organise threat intelligence
* Explain incidents

---

# Digital Forensics

Digital forensics is the process of collecting and analysing digital evidence.

A simplified workflow:

```text
Preserve
   |
   v
Acquire
   |
   v
Analyse
   |
   v
Document
   |
   v
Report
```

---

# Disk Forensics

Study:

* Files
* Filesystems
* Metadata
* Deleted files
* Timestamps
* Browser artefacts
* Application data

---

# Memory Forensics

RAM can contain information that never gets written to disk.

Investigators may examine:

* Processes
* Network connections
* Loaded modules
* Memory artefacts

---

# Timeline Analysis

Timeline analysis combines timestamps from multiple sources.

For example:

```text
10:00  User logged in
10:03  File created
10:05  Process started
10:06  Network connection
10:08  File modified
```

The timeline helps investigators understand what happened.

---

# Forensics Tools

Common tools include:

* Autopsy
* The Sleuth Kit
* Volatility
* FTK Imager
* Plaso

---

# Malware Analysis

Malware analysis attempts to understand what malicious software does.

Never execute unknown malware on your normal computer.

Use an isolated analysis environment.

---

# Static Analysis

Static analysis examines a file without executing it.

Look at:

* File type
* Hash
* Strings
* Imports
* Metadata
* Sections
* Embedded resources

---

# Dynamic Analysis

Dynamic analysis observes behaviour during execution in an isolated environment.

Look at:

* Processes
* Files
* Registry activity
* Network connections
* Persistence
* Child processes

---

# Indicators of Compromise

Examples include:

```text
File hashes
IP addresses
Domains
File paths
Registry keys
Process names
```

An IOC isn't automatically proof of malicious activity.

Context matters.

---

# YARA

YARA is used to identify files based on patterns.

A YARA rule can look for combinations of:

* Strings
* Byte patterns
* File properties
* Conditions

Conceptually:

```text
File
 |
 v
YARA rule
 |
 +-- Match
 |
 +-- No match
```

YARA is useful in malware analysis and detection engineering.

---

# Sigma

Sigma is used to describe detection logic for logs in a vendor-neutral format.

A simple idea:

```text
Event
  |
  v
Log
  |
  v
Sigma Rule
  |
  v
Alert
```

Good detection rules should balance useful coverage with manageable false positives.

---

# Defensive Security

Security isn't only about breaking things.

A defender needs to understand:

* Prevention
* Detection
* Investigation
* Containment
* Recovery
* Hardening

---

# SIEM

A SIEM collects and analyses security events.

A basic architecture:

```text
Endpoints
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

Examples include:

* Wazuh
* Splunk
* Elastic Security

---

# Detection Engineering

A useful detection should answer:

```text
What happened?
Why is it suspicious?
What evidence supports it?
What should an analyst investigate next?
```

Avoid writing detections that alert on absolutely everything.

Noise can be almost as problematic as missing useful events.

---

# Incident Response

A common lifecycle is:

```text
Preparation
    |
Detection
    |
Analysis
    |
Containment
    |
Eradication
    |
Recovery
    |
Lessons Learned
```

The exact process varies between organisations.

The important part is having a plan before something happens.

---

# Reverse Engineering

Reverse engineering is about understanding software without relying entirely on its source code.

Learn:

* C
* Assembly
* CPU registers
* Memory
* Stack
* Heap
* Functions
* ELF
* PE
* Debugging

---

# Static Analysis

Inspect a program without running it.

Useful tools:

* Ghidra
* strings
* objdump

Questions to ask:

```text
What functions exist?
What libraries are used?
What strings are present?
Where is the entry point?
What inputs does the program process?
```

---

# Dynamic Analysis

Observe a program while it runs.

Useful tools include:

* GDB
* Debuggers
* Process monitors
* Network monitors

---

# Assembly

Assembly is a human-readable representation of machine instructions.

You may encounter instructions such as:

```text
mov
push
pop
call
cmp
jmp
ret
```

You don't need to memorise every instruction immediately.

Learn how registers, memory and control flow work.

---

# Binary Exploitation

This is an advanced subject.

Learn the foundations first.

Prerequisites include:

* C
* Linux
* Assembly
* Memory
* Debugging
* Processes
* System calls

---

## Memory

Understand:

```text
Code
Global data
Heap
Stack
Libraries
```

---

## Security Protections

Learn what these are designed to prevent:

* ASLR
* DEP/NX
* Stack canaries
* PIE
* RELRO
* Control-flow protections

Practise using purpose-built CTF binaries and local vulnerable programs.

---

# Cloud Security

Cloud environments introduce new security boundaries.

Learn:

* Identity
* Permissions
* Storage
* Networking
* Logging
* Secrets
* Configuration

---

# Shared Responsibility

Cloud providers secure certain parts of the underlying infrastructure.

Customers are still responsible for many things, including:

* Identity
* Permissions
* Data
* Applications
* Configuration
* Secrets

The exact split depends on the service.

---

# AWS

Learn:

* IAM
* EC2
* S3
* VPC
* Security Groups
* CloudTrail
* KMS
* Secrets management

---

# Azure

Learn:

* Microsoft Entra ID
* Virtual Networks
* Network Security Groups
* Storage
* Key Vault
* Defender for Cloud

---

# Common Cloud Security Problems

* Excessive permissions
* Public storage
* Exposed credentials
* Weak identity controls
* Missing logging
* Poor network segmentation

---

# Container Security

Containers package applications and their dependencies.

A container is not simply a small virtual machine.

Learn:

* Images
* Containers
* Dockerfiles
* Registries
* Volumes
* Networks
* Secrets
* Privileges

---

# Docker Security

Watch for:

* Running containers unnecessarily as root
* Outdated images
* Secrets inside images
* Untrusted images
* Exposed Docker interfaces
* Excessive filesystem access

---

# Kubernetes

Once Docker makes sense, learn:

* Pods
* Services
* Deployments
* Namespaces
* RBAC
* Service accounts
* Network policies
* Secrets
* Admission controls

Use local clusters for learning.

---

# Mobile Security

Mobile security covers applications, permissions, storage, communication and platform security.

---

# Android

Learn:

* APKs
* Activities
* Services
* Intents
* Permissions
* ADB
* Application storage

Useful tools:

* JADX
* MobSF
* Android emulators

---

# iOS

Learn:

* App bundles
* Sandboxing
* Entitlements
* Code signing
* Secure storage
* Network security

Practise with your own applications, test applications and emulators.

---

# IoT Security

IoT combines:

* Hardware
* Embedded software
* Networking
* Firmware
* Physical interfaces

Learn:

* Embedded Linux
* Firmware
* UART
* SPI
* I2C
* JTAG
* Bootloaders
* Device authentication
* Firmware updates
* Default credentials

---

# Firmware Analysis

A basic workflow:

```text
Firmware
   |
   v
Identify format
   |
   v
Extract contents
   |
   v
Inspect filesystem
   |
   v
Analyse binaries
   |
   v
Inspect configuration
   |
   v
Document findings
```

Use hardware you own.

---

# CTFs and Practice

CTFs are a great way to practise without attacking real systems.

---

## OverTheWire

Good for:

* Linux
* Command line
* Basic security concepts

---

## TryHackMe

Useful for guided cybersecurity learning and structured rooms.

---

## Hack The Box

Useful for more realistic machines and challenges.

---

## PortSwigger Web Security Academy

Particularly useful for:

* XSS
* SQL injection
* Authentication
* Access control
* SSRF
* Other web vulnerabilities

---

## picoCTF

Useful for beginner-friendly challenges across:

* Web
* Crypto
* Forensics
* Reverse engineering
* General security

---

# Projects

Projects turn knowledge into actual experience.

---

## Beginner Projects

### Linux Home Lab

Create a Linux VM and document:

* Users
* Groups
* Permissions
* Services
* Networking
* Logs

### Python Log Parser

Create a program that reads a local log and summarises interesting events.

### Packet Analysis

Capture traffic from your own lab and explain what each connection represents.

---

## Intermediate Projects

### Vulnerable Web Application

Build a deliberately vulnerable application.

Document:

```text
Vulnerability
    |
Cause
    |
Impact
    |
Detection
    |
Fix
    |
Verification
```

Include vulnerabilities such as XSS or SQL injection only in your controlled application.

### Windows Lab

Build a small Windows/Active Directory environment.

Document:

* Users
* Groups
* Policies
* Authentication
* Logging
* Security controls

### Detection Lab

Generate benign test events and create detections for them.

---

## Advanced Projects

### Malware Analysis Lab

Use safe training samples in an isolated environment.

Document:

* Static observations
* Dynamic observations
* Network behaviour
* Indicators
* Detection ideas

### Reverse Engineering

Write a small C program.

Compile it.

Then reverse engineer your own binary.

### Build a CTF

Create challenges covering:

* Linux
* Web
* Crypto
* Forensics
* Reverse engineering

---

# Tool Reference

| Tool            | Purpose                                  | Level        |
| --------------- | ---------------------------------------- | ------------ |
| Nmap            | Network/service discovery                | Beginner     |
| Wireshark       | Packet analysis                          | Beginner     |
| tcpdump         | Packet capture                           | Beginner     |
| Burp Suite      | Web testing                              | Beginner     |
| OWASP ZAP       | Web testing                              | Beginner     |
| Aircrack-ng     | Wireless security assessment             | Intermediate |
| Airgeddon       | Wireless auditing framework              | Intermediate |
| Fern            | Wireless auditing GUI                    | Beginner     |
| Metasploit      | Security testing framework               | Intermediate |
| Ghidra          | Reverse engineering                      | Advanced     |
| GDB             | Debugging                                | Advanced     |
| Hashcat         | Password auditing                        | Intermediate |
| John the Ripper | Password auditing                        | Intermediate |
| Gobuster        | Content discovery                        | Intermediate |
| Amass           | Asset discovery                          | Intermediate |
| Nikto           | Web server assessment                    | Beginner     |
| SQLMap          | SQL injection testing in authorised labs | Intermediate |
| Autopsy         | Digital forensics                        | Intermediate |
| Volatility      | Memory forensics                         | Advanced     |
| YARA            | File pattern matching                    | Intermediate |
| Sigma           | Detection rules                          | Intermediate |

---

# Troubleshooting

Cybersecurity tools won't always work.

That's normal.

When something fails, don't immediately reinstall everything.

Work backwards.

```text
What did I expect?
       |
       v
What actually happened?
       |
       v
What changed?
       |
       v
Is the hardware supported?
       |
       v
Is the driver working?
       |
       v
Is the interface configured?
       |
       v
Is the command correct?
       |
       v
Check logs
```

---

## Wireless Adapter Not Detected

Check:

```text
USB connection
Driver
Chipset
Interface name
Kernel support
Monitor-mode support
```

Don't assume every USB WiFi adapter supports every wireless testing feature.

---

## Port Doesn't Appear Open

Possible explanations include:

* Service isn't running
* Firewall blocks it
* Wrong interface
* Wrong IP
* Service listens only locally
* Network isolation
* Scan configuration

Don't immediately assume the target is broken.

---

## Web Request Doesn't Work

Check:

```text
URL
HTTP method
Headers
Cookies
Parameters
Body
Authentication
Redirects
TLS
Server response
```

Burp Suite can help you understand the request.

---

# Common Beginner Mistakes

<details>
<summary>Installing Kali and thinking you're finished</summary>

Kali is an operating system.

It doesn't teach you networking, Linux or security automatically.

</details>

<details>
<summary>Copying commands without understanding them</summary>

If you cannot explain what a command does, learn it before moving on.

</details>

<details>
<summary>Trying to learn everything at once</summary>

Cybersecurity is enormous.

Pick one topic and become comfortable with the fundamentals before adding another.

</details>

<details>
<summary>Ignoring networking</summary>

Networking knowledge makes almost every other security subject easier.

</details>

<details>
<summary>Only learning offensive security</summary>

Learn defence too.

Understanding logs, detection and hardening makes security knowledge much more complete.

</details>

<details>
<summary>Collecting tools instead of knowledge</summary>

Having 300 tools installed isn't particularly useful if you don't understand what any of them are doing.

</details>

---

# Learning Roadmap

## Stage 1: Computer Fundamentals

Learn:

```text
CPU
RAM
Storage
Processes
Operating systems
Filesystems
```

## Stage 2: Linux

Learn:

```text
Files
Permissions
Users
Processes
Services
Packages
Logs
Bash
SSH
```

## Stage 3: Networking

Learn:

```text
IP
MAC
TCP
UDP
DNS
DHCP
Ports
Subnets
Routing
NAT
Firewalls
HTTP
HTTPS
```

## Stage 4: Programming

Learn:

```text
Python
Bash
JavaScript basics
HTML basics
SQL
C basics
Git
```

## Stage 5: Security Fundamentals

Learn:

```text
Authentication
Authorisation
Cryptography
Least privilege
Threat modelling
Vulnerabilities
Risk
Logging
```

## Stage 6: Recon and Enumeration

Learn:

```text
Recon
Nmap
DNS
Service enumeration
HTTP enumeration
```

## Stage 7: Web Security

Learn:

```text
HTTP
Cookies
Sessions
Authentication
Authorisation
XSS
SQL injection
CSRF
SSRF
Path traversal
File uploads
API security
```

## Stage 8: Wireless

Learn:

```text
802.11
WiFi authentication
WPA2
WPA3
Monitor mode
Packet capture
Aircrack-ng
Airgeddon
Fern
```

## Stage 9: Windows

Learn:

```text
Windows
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

## Stage 10: Defensive Security

Learn:

```text
SIEM
Logging
Detection
YARA
Sigma
Incident response
Vulnerability management
Threat modelling
MITRE ATT&CK
```

## Stage 11: Advanced Security

Learn:

```text
Reverse engineering
Assembly
Binary exploitation
Malware analysis
Memory forensics
Cloud security
Container security
Mobile security
IoT security
```

---

# Suggested Weekly Schedule

You don't need to spend twelve hours every day learning this.

A realistic schedule could be:

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
Revision

Saturday
CTF / Lab

Sunday
Notes and review
```

Consistency matters more than trying to cram everything into one weekend.

---

# Glossary

| Term  | Meaning                                               |
| ----- | ----------------------------------------------------- |
| ACL   | Access Control List                                   |
| API   | Interface allowing software to communicate            |
| ARP   | Protocol used for IP-to-link-layer address resolution |
| CVE   | Identifier for a publicly documented vulnerability    |
| CWE   | Category of software weakness                         |
| CVSS  | Vulnerability severity scoring system                 |
| DNS   | Domain Name System                                    |
| EDR   | Endpoint Detection and Response                       |
| IAM   | Identity and Access Management                        |
| IOC   | Indicator of Compromise                               |
| JWT   | JSON Web Token                                        |
| LDAP  | Directory access protocol                             |
| MFA   | Multi-Factor Authentication                           |
| NAT   | Network Address Translation                           |
| OSINT | Open-Source Intelligence                              |
| RBAC  | Role-Based Access Control                             |
| SIEM  | Security Information and Event Management             |
| SMB   | Server Message Block                                  |
| SSO   | Single Sign-On                                        |
| TLS   | Transport Layer Security                              |
| TTP   | Tactics, Techniques and Procedures                    |
| VM    | Virtual Machine                                       |
| VPN   | Virtual Private Network                               |
| XSS   | Cross-Site Scripting                                  |
| CTF   | Capture The Flag                                      |
| SSRF  | Server-Side Request Forgery                           |
| CSRF  | Cross-Site Request Forgery                            |
| SQLi  | SQL Injection                                         |
| API   | Application Programming Interface                     |
| KDC   | Key Distribution Center                               |
| PE    | Portable Executable                                   |
| ELF   | Executable and Linkable Format                        |

---

# Security Principles Worth Remembering

## Least Privilege

Give users and programs only the access they need.

## Defence in Depth

Don't depend on one security control.

Use multiple layers.

```text
Authentication
      +
Authorisation
      +
Network controls
      +
Endpoint security
      +
Logging
      +
Monitoring
```

## Secure by Default

Systems should start in a reasonably secure configuration rather than requiring users to discover every security setting themselves.

## Fail Safely

When something goes wrong, the system should avoid exposing sensitive information or granting unintended access.

## Assume Breach

Security teams should consider what happens if one layer is compromised.

That means thinking about:

* Segmentation
* Monitoring
* Least privilege
* Backups
* Detection
* Recovery

---

# What To Do When You Get Stuck

Getting stuck is normal.

Before searching for the exact answer, try:

1. Read the error.
2. Identify the unfamiliar term.
3. Check documentation.
4. Reproduce the problem.
5. Simplify the setup.
6. Check logs.
7. Search for the underlying concept.
8. Try again.

Don't only search:

```text
"how do I get tool X to work"
```

Try understanding:

```text
"why does this error happen"
```

That difference matters.

---

# How To Take Good Notes

For each subject, keep notes in this format:

```text
Topic:

What is it?

Why does it exist?

How does it work?

What can go wrong?

How can it be detected?

How can it be prevented?

What did I practise?

What did I learn?
```

This makes your notes much more useful later.

---

# How To Write Security Reports

A basic report should explain:

```text
Finding
   |
Description
   |
Evidence
   |
Impact
   |
Affected component
   |
Recommendation
   |
Verification
```

Avoid writing reports that simply say:

> "This is vulnerable."

Explain:

* What happened
* Why it happened
* What could happen because of it
* How to fix it
* How you confirmed the fix

---

# Final Advice

Don't worry about looking like a hacker.

You don't need a ridiculous terminal setup or twelve monitors.

You need curiosity.

Learn how something works.

Break it in your lab.

Figure out why it broke.

Fix it.

Then try again.

The tools will change.

Linux distributions will change.

Vulnerabilities will change.

The fundamentals will stick around.

If you understand operating systems, networking, programming, authentication, web applications and how computers communicate, you'll always have something to build on.

Most importantly, practise legally.

Build your own lab.

Use CTFs.

Use training applications.

Test systems only when you have permission.

Learn the fundamentals first.

The fancy tools can wait.
