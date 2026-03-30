# Nmap Scanning Lab (Cybersecurity Project)

## Objective
To perform network scanning using Nmap to identify live hosts, open ports, running services, and analyze the security posture of systems.

---

## Tools Used
- Kali Linux
- Nmap

---

## Network Range
192.168.64.0/24

---

## Step 1: Host Discovery

```bash
nmap -sn 192.168.64.0/24
```

**Result:**
- 192.168.64.1
- 192.168.64.2
- 192.168.64.254
- 192.168.64.128

---

## Step 2: Port Scanning

```bash
nmap 192.168.64.1
```

**Open Ports:**
- 902/tcp
- 912/tcp
- 5357/tcp

---

## Step 3: Service Detection

```bash
nmap -sV 192.168.64.1
```

**Findings:**
- VMware Authentication Daemon
- Microsoft HTTPAPI

---

## Step 4: OS Detection

```bash
nmap -A 192.168.64.1
```

**Result:**
- Windows 10/11 (approx)

---

## Step 5: Second Target Analysis

```bash
nmap -sV 192.168.64.2
```

**Result:**
- Port 53 (DNS) filtered

---

## Step 6: Full Port Scan

```bash
nmap -p- 192.168.64.2
```

**Result:**
- No additional ports found

---

## Step 7: Self Scan

```bash
nmap 192.168.64.128
```

**Result:**
- Port 22 (SSH) open

---

## Step 8: Localhost Scan

```bash
nmap localhost
```

**Observation:**
- Ports appear closed instead of filtered

---

## Step 9: Stealth Scan

```bash
nmap -sS 192.168.64.1
```

**Purpose:**
- Perform stealth scanning using SYN scan

---

## Security Analysis

- System 192.168.64.1 has multiple open ports, increasing attack surface
- VMware services may be targeted if vulnerabilities exist
- System 192.168.64.2 is more secure with minimal exposure
- SSH service on local machine could be targeted by brute-force attacks

---

## Real-world Use Case

This type of scanning is used by SOC analysts and penetration testers to identify exposed services, detect misconfigurations, and assess network security posture.

---

## Key Learnings

- Identified live hosts in a network
- Performed port scanning and service detection
- Understood difference between open, closed, and filtered ports
- Learned OS detection using Nmap
- Compared security posture of systems
- Understood stealth scanning techniques

---

## Conclusion

This project demonstrates how network reconnaissance is performed to identify exposed services and evaluate system security.
