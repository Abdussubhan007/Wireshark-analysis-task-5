# Wireshark-analysis-task-5
Packet capture and protocol analysis using wireshark

# Task 5: Capture and Analyze Network Traffic Using Wireshark

## 📌 Objective
Capture live network packets using Wireshark and identify basic protocols and traffic types.

---

## 🛠 Tools Used
- **Wireshark** (v4.4.7)
- Windows 10 (64-bit)

---

## 📶 Capture Summary
Captured live packets on Wi-Fi interface while browsing websites and pinging `google.com`.

### ✅ Protocols Identified:
1. **UDP** – Unreliable datagram traffic, port 5353 (used for MDNS), 5775 (custom).
2. **DNS** – Domain name lookups to `googleapis.com`, `accounts.google.com`, etc.
3. **ICMP/ICMPv6** – Ping requests and replies.
4. **ARP** – IP-to-MAC address resolution in local network.
5. **SSDP/HTTP** – Device discovery and basic web protocols (seen via NOTIFY * HTTP/1.1).

---

## 🔍 Sample Packet Details

### 📄 UDP Packet:
- **Source:** `192.168.29.246`
- **Destination:** `192.168.29.255`
- **Info:** Port 41028 → 5775, Len = 44

### 📄 DNS Query:
- Query for: `accounts.google.com`
- Response from: `142.250.77.227`

### 📄 ICMP:
- Ping echo request/reply with TTL and sequence number
- IPv6 addresses used

### 📄 ARP:
- Who has `192.168.29.1`? Tell `192.168.29.111`

---

## 📁 Files Included:
- `network-traffic-capture.pcapng` – Full packet capture file
- Screenshots:
  - UDP Filter
  - ICMP Filter
  - HTTP Filter
  - DNS Filter
  - ARP Filter
  - Full Traffic Overview

---

## 🚀 Learning Outcome
- Learned how to use Wireshark to capture and analyze traffic.
- Understood different network protocols and filtering techniques.
- Gained practical experience in live packet analysis.
