# 🏁 TryHackMe: Networking Secure Protocols Challenge
**Path:** Cyber Security 101  
**Date:** 30 January 2026  
**Difficulty:** 🟢 Easy

---

## 🎯 Objective
The goal of this challenge was to apply my knowledge of network protocols (OSI Model, TCP/UDP, and Port numbers) to solve a hands-on scenario and retrieve a hidden flag.

## 🛠️ Tools & Concepts Used
* **Tools:** Wireshark
* **Concepts:** Traffic Decryption, PCAP Analysis, and TLS/SSL Handshakes.
---

## 🚀 The Challenge Process

### 1. Analysis of the Task


Challenge: One of the packets contains login credentials. What password did the user submit?

### 2. Steps Taken
1. **Initial Setup:** Launched the target machine and opened `randy-chromium.pcapng` in Wireshark.
2. **Protocol Configuration:** - Right-clicked a TLS packet and navigated to `Protocol Preferences` > `Transport Layer Security`.
   - Selected `Open Transport Layer Security preferences`.
3. **Decryption:** - Browsed to the `Documents` directory to locate the `ssl-key.log` file.
   - Applied the key log to Wireshark to decrypt the TLS traffic.
4. **Credential Extraction:** - Followed the hint to locate **Packet 366**, which revealed the decrypted login credentials.


### 3. Capturing the Flag
I successfully retrieved the flag: `[THM{B8WM6P}]`

---

## 💡 Key Learnings
* **What I learned:** I learned how to use a key log file to turn unreadable encrypted traffic into visible data—a critical skill for security analysis. Whereas the room was more about the network security protocols and port numbers for those protocols.

* **The Hardest Part:** Initially I was trying to find the packet that might have the credentials by myself by looking at the info of the packets which was not the case and also being hundreds of packets it was challenging. So, I had to take the hint from the challenge that said look at packet 366 and after opening the packet I was able to retrieve the information needed.

---

