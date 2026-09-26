# CTC Cyber Security Workshop 2026

*Click on the session name below to jump to that session.*

## Table of Contents
- [Session 1: Cybersecurity Basics, Hackers, Attacks & Nmap Intro(21 Sep 2026)](#session-1-cybersecurity-basics-hackers-attacks--nmap-intro-21-sep-2026)

---

## Session 1: Cybersecurity Basics, Hackers, Attacks & Nmap Intro

### Topics Covered

#### 1. What is Cybersecurity?
Cybersecurity is the practice of protecting systems, networks, applications and data from digital attacks. The goal is usually summed up by the **CIA Triad**:

| Principle | Meaning |
|-----------|---------|
| **Confidentiality** | Only authorized people can access the data |
| **Integrity** | Data is accurate and not tampered with |
| **Availability** | Systems and data are accessible when needed |

#### 2. Different Types of Hackers

| Type | Also called | What they do |
|------|-------------|---------------|
| **White Hat** | Ethical hacker | Hacks legally, with permission, to find and fix vulnerabilities |
| **Black Hat** | Malicious hacker | Hacks illegally for personal gain, damage or theft |
| **Grey Hat** | — | Hacks without permission but without malicious intent (e.g. reports the flaw afterwards) |
| **Script Kiddie** | — | Uses existing tools/scripts without deep technical knowledge |
| **Hacktivist** | — | Hacks to promote a political or social cause |
| **State-Sponsored** | — | Works for a government to spy on or attack other nations |

#### 3. Blue Team vs Red Team

```
Red Team  ──attacks──▶  System/Network  ◀──defends──  Blue Team
```

- **Red Team**: the "attackers." They simulate real-world attacks to find weaknesses (offensive security, penetration testing).
- **Blue Team**: the "defenders." They monitor, detect and respond to attacks (security operations, incident response).
- **Purple Team**: red + blue working together, sharing findings to improve overall security.

#### 4. Different Types of Attacks

| Attack | What happens |
|--------|---------------|
| **Phishing** | Fake emails/messages trick users into giving up credentials or clicking malicious links |
| **Malware** | Malicious software (viruses, worms, trojans, ransomware) that damages or spies on a system |
| **DoS / DDoS** | Flooding a server with traffic so real users can't access it |
| **Man-in-the-Middle (MITM)** | Attacker secretly intercepts communication between two parties |
| **SQL Injection** | Malicious SQL code inserted into input fields to manipulate a database |
| **Brute Force** | Repeatedly guessing passwords until the correct one is found |
| **Social Engineering** | Manipulating people (not systems) into revealing confidential information |

#### 5. What is Nmap and How It Operates
**Nmap (Network Mapper)** is a free, open-source tool used to discover hosts and services on a network by sending crafted packets and analyzing the responses.

- It can find which devices are alive on a network (**host discovery**).
- It can find which **ports** are open, closed or filtered on a target.
- It can guess which **service/version** is running on a port (e.g. Apache 2.4).
- It can attempt to guess the target's **operating system**.

**How it works (simplified):** Nmap sends packets (TCP/UDP/ICMP) to specific ports on a target IP → the target responds (or doesn't) → Nmap interprets the response to decide if the port is open, closed, or filtered.

#### 6. Practical Demonstration of Nmap

| Command | What it does |
|---------|---------------|
| `nmap <target-ip>` | Basic scan — checks common ports on the target |
| `nmap -sV <target-ip>` | Detects service/version running on open ports |
| `nmap -O <target-ip>` | Attempts OS detection |
| `nmap -p 1-1000 <target-ip>` | Scans a specific port range |
| `nmap -sS <target-ip>` | Stealthy SYN scan (doesn't complete the TCP handshake) |
| `nmap -A <target-ip>` | Aggressive scan: OS, version, script scanning, traceroute |

> ⚠️ **Only scan systems you own or have explicit permission to test.** Scanning networks without authorization is illegal in most countries.

#### 7. What is an IP Address
An **IP (Internet Protocol) address** is a unique numerical label assigned to every device on a network, used to identify and locate it so data can be routed correctly.

- **IPv4**: format like `192.168.1.1` (four numbers, 0–255, separated by dots).
- **IPv6**: newer format like `2001:0db8:85a3::8a2e:0370:7334`, made to solve IPv4 running out of addresses.
- **Private IP**: used inside a local network (e.g. `192.168.x.x`, `10.x.x.x`) — not reachable directly from the internet.
- **Public IP**: assigned by your ISP, visible to the internet.

#### 8. Basic Kali Linux Commands

| Command | What it does | Example |
|---------|---------------|---------|
| `ifconfig` / `ip a` | Show network interfaces and IP addresses | `ip a` |
| `ping <ip>` | Check if a host is reachable | `ping 8.8.8.8` |
| `whoami` | Show current logged-in user | `whoami` |
| `sudo <command>` | Run a command with admin/root privileges | `sudo nmap -sS 192.168.1.1` |
| `netstat -tulnp` | Show open ports and active connections | `netstat -tulnp` |
| `apt update && apt upgrade` | Update package lists and installed tools | `sudo apt update` |
| `man <tool>` | Show the manual/help page for a tool | `man nmap` |

#### 9. How a Hacker Hacks Someone's System (Attack Lifecycle)
A typical attack (used by both real attackers and ethical pentesters) follows these stages:

1. **Reconnaissance** – gathering information about the target (IP, emails, employee names, technologies used).
2. **Scanning** – finding open ports, services and vulnerabilities (e.g. using Nmap).
3. **Gaining Access** – exploiting a found vulnerability to get into the system.
4. **Maintaining Access** – installing backdoors/malware to keep access for later.
5. **Covering Tracks** – deleting logs and hiding evidence of the intrusion.

Defenders (Blue Team) try to detect and stop attackers at every one of these stages.

---

### Resources

- **Cybersecurity Basics**
  - [What is Cybersecurity? (CISA)](https://www.cisa.gov/topics/cybersecurity-best-practices)
  - [CIA Triad Explained (NIST Glossary)](https://csrc.nist.gov/glossary/term/cia_triad)
- **Types of Hackers**
  - [Types of Hackers (OWASP)](https://owasp.org/)
- **Red Team / Blue Team**
  - [Red Team vs Blue Team (CISA)](https://www.cisa.gov/resources-tools/programs/red-team-blue-team)
- **Types of Attacks**
  - [OWASP Top 10](https://owasp.org/www-project-top-ten/)
  - [Common Attack Pattern Enumeration (MITRE CAPEC)](https://capec.mitre.org/)
- **Nmap**
  - [Nmap Official Reference Guide](https://nmap.org/book/man.html)
  - [Nmap Download & Docs](https://nmap.org/)
- **IP Addressing**
  - [What is an IP Address? (Cloudflare Learning)](https://www.cloudflare.com/learning/dns/glossary/what-is-my-ip-address/)
- **Kali Linux**
  - [Kali Linux Official Documentation](https://www.kali.org/docs/)
  - [Kali Linux Downloads](https://www.kali.org/get-kali/)
- **For the homework**
  - [VirtualBox Official Downloads](https://www.virtualbox.org/wiki/Downloads)
  - [Kali Linux VirtualBox Image (Official)](https://www.kali.org/get-kali/#kali-virtual-machines)

---

### Practice Questions
1. In your own words, explain the CIA Triad and give a real-world example of each principle being broken.
2. List three differences between a White Hat and a Black Hat hacker.
3. Explain the difference between Red Team and Blue Team in one or two sentences.
4. Run `nmap -sV` on a device you own on your home network and note down which ports and services it finds.
5. Find your own machine's private IP address using `ip a` (Linux) or `ipconfig` (Windows).

### Homework
1. **Install a Kali Linux virtual machine in VirtualBox.**
   - Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
   - Download the official [Kali Linux VirtualBox image](https://www.kali.org/get-kali/#kali-virtual-machines).
   - Import the image into VirtualBox and boot it up.
   - Log in and run `whoami` and `ip a` to confirm it's working, and take a screenshot.