# Task 1: Local Network Port Scanning & Reconnaissance

## Objective
To discover open ports and active devices on a local subnet using Nmap to evaluate network exposure and service visibility.

## Environment Details
- **Attacking Host Operating System:** Windows 10/11 (Command Prompt)
- **Target Subnet Range:** 10.53.80.0/24
- **Scan Method:** TCP SYN Scan (Stealth)

## Command Executed
```cmd
nmap -sS -T4 10.53.80.0/24 -oN network_scan_report.txt
```

## Scan Findings Summary
The scan successfully discovered 4 active hosts on the network pool:

1. **Host: 10.53.80.61 (Gateway/Router)**
   - Port 53/tcp (Open) - Domain (DNS Service)
2. **Host: 10.53.80.100 (Epson Printer)**
   - Port 80/tcp (Open) - HTTP (Web Management Interface)
   - Port 515/tcp (Open) - Printer Line Printer Daemon
   - Port 9100/tcp (Open) - Jetdirect Network Printing
3. **Host: 10.53.80.107 (Local Host Windows PC)**
   - Port 135/tcp (Open) - MSRPC (Remote Procedure Call)
   - Port 139/tcp (Open) - NetBIOS-SSN
   - Port 445/tcp (Open) - Microsoft-DS (SMB File Sharing)

---

