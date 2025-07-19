# 🌐 Project 2 – DNS Request Analysis Using Wireshark

## 📌 Project Overview

This project focuses on analyzing **Domain Name System (DNS)** traffic using Wireshark. DNS is the process that translates domain names (like `google.com`) into IP addresses so browsers can connect to websites.

By capturing DNS queries and responses, we can observe how names are resolved, what DNS records look like, and why DNS is a critical — and vulnerable — part of internet communication.

---

## 🛠️ Tools Used

- 🐬 **Wireshark**
- 📶 **Phone hotspot** (Laptop connected to mobile data)
- 🌍 Websites visited: `example.net`, `neverssl.com`, `testphp.vulnweb.com`
- 💻 Google Chrome / Any browser

---

## 🔄 Steps Taken

### 1. Capture Started
- Opened Wireshark and selected the Wi-Fi interface.
- Began a live capture.

### 2. Browsed New Websites
- Visited several websites that had not recently been accessed.
- This forced the browser to send DNS queries to resolve domain names.

### 3. Filtered DNS Packets
- Applied this display filter:
  ```dns```

### 4. Analyzed DNS Packet Contents
- Examined:
  - Query types: `A` (IPv4), `AAAA` (IPv6)
  - Domain names requested
  - IP addresses returned in responses
  - UDP as the transport protocol for DNS
- Right-clicked and followed some UDP streams for full DNS communication view.

### 5. Saved the Capture
- Exported the session as: `project2_dns_request_analysis.pcapng`

---

## 📷 Screenshots

> Add your own screenshots from Wireshark:
- DNS query packet expanded
- UDP stream showing a full DNS request/response
- Interesting or unexpected DNS entries (e.g., multiple IPs)

---

## 📁 Project Files

| File | Description |
|------|-------------|
| `project2_dns_request_analysis.pcapng` | Packet capture file |
| `README.md` | This summary of the DNS traffic analysis |

---

## 🔍 Key Findings

- DNS uses **UDP port 53** by default.
- All domain name lookups are visible in plain text.
- Some websites triggered **multiple DNS requests** (e.g., subdomains or CDNs).
- DNS traffic reveals which domains are being accessed — **a big privacy risk** if not encrypted.
- **DNS poisoning** and **spoofing** attacks can target this layer.

---

## 🔐 Why This Matters

DNS is like the address book of the internet — and it's often overlooked. Attackers can:
- Intercept or manipulate DNS responses
- Use DNS tunneling to exfiltrate data
- Monitor DNS traffic to learn what sites users visit

This project highlights the need for **secure DNS solutions**, such as:
- DNS over HTTPS (DoH)
- DNS over TLS (DoT)
- Internal DNS logging for monitoring

---

## ✅ What’s Next

👉 [Project 3 – Detecting Malware Communication (PCAP Analysis)](#)  
We'll use a sample `.pcap` from a malware-infected machine and break down suspicious behavior like beaconing and command-and-control connections.

---

## 🙋 About Me

This is part of my cybersecurity learning journey using **Wireshark**. Each project in this repo demonstrates a real-world skill, hands-on analysis, and clear documentation — all geared toward building a strong portfolio.

Connect with me or check out my other Wireshark projects!
