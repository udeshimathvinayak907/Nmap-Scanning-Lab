# Nmap Scanning Lab (Cybersecurity Project)

## Objective
To perform network scanning using Nmap and identify live hosts, open ports, running services, and analyze the security posture of systems.

---

## Tools Used
- Kali Linux
- Nmap

---

## Step 1: Host Discovery

Command:
nmap -sn 192.168.64.0/24

Result:
- 192.168.64.1
- 192.168.64.2
- 192.168.64.254
- 192.168.64.128

---

## Step 2: Port Scanning

Command:
nmap 192.168.64.1

Open Ports:
- 902/tcp
- 912/tcp
- 5357/tcp

---

## Step 3: Service Detection

Command:
nmap -sV 192.168.64.1

Findings:
- VMware Authentication Daemon
- Microsoft HTTPAPI

---

## Step 4: OS Detection

Command:
nmap -A 192.168.64.1

Result:
- Windows 10/11 (approx)

---

## Step 5: Second Target Analysis

Command:
nmap -sV 192.168.64.2

Result:
- Port 53 (DNS) filtered

---

## Step 6: Full Port Scan

Command:
nmap -p- 192.168.64.2

Result:
- No additional ports found

---

## Step 7: Self Scan

Command:
nmap 192.168.64.128

Result:
- Port 22 (SSH) open

---

## Step 8: Localhost Scan

Command:
nmap localhost

Observation:
- Ports appear closed instead of filtered

---

## Step 9: Stealth Scan

Command:
nmap -sS 192.168.64.1

Purpose:
- Perform stealth scanning using SYN scan

---

## Key Learnings

- Identified live hosts in a network
- Performed port scanning and service detection
- Understood difference between open, closed, filtered ports
- Learned OS detection using Nmap
- Compared security posture of systems
- Understood stealth scanning techniques

---

## Conclusion

This project demonstrates how attackers and security analysts perform network reconnaissance to identify exposed services and evaluate system security.
