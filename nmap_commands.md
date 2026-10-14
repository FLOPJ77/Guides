# NMAP Commands

Install:
```bash
sudo apt update && sudo apt install nmap -y
```

Basic scans:
```bash
nmap 192.168.1.1
# or
nmap scanme.nmap.org

```

Scan online devices (no port scanning):
```bash
nmap -sn 192.168.1.0/24

```


Specific ports:
```bash
nmap -p 22,80,443 192.168.1.1

```

Ports range:
```bash
nmap -p 1-1000 192.168.1.1

```

Scan all 65,535 ports:
```bash
nmap -p- 192.168.1.1

```

Fast scan top 100 most common ports:
```bash
nmap -F 192.168.1.1

```

Detect service versions (Apache, OpenSSH...):
```bash
nmap -sV 192.168.1.1

```

Detect OS:
```bash
sudo nmap -O 192.168.1.1

```

Aggressive scan (OS, version, script, traceroute):
```bash
sudo nmap -A 192.168.1.1

```

Stealth scan (SYN scan):
```bash
sudo nmap -sS 192.168.1.1

```

Saving output in a text file:
```bash
nmap -oN results.txt 192.168.1.1

```

All in one common command:
```bash
sudo nmap -sV -p- -oN my_scan.txt 192.168.1.1

```


