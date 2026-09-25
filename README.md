<div align="center">

# 🔑 Cryptographic Password Recovery & Hash Auditing Lab

**Offline Document Auditing with John the Ripper (Johnny GUI) & Networkwalks Tools**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cryptography-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Tool-John%20the%20Ripper-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/GUI-Johnny%20v2.2-E87500?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Module-W3--PM1%20%26%20W3--PM2-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Attack-Dictionary%20Attack-C00000?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Environment-Kali%20Linux%202026.2-0070C0?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-Week%2003-404040?style=flat-square&labelColor=0070C0" />
</p>

---

## 📌 Repository Overview

This repository documents the practical deliverables for **Week 3** of the Networkwalks Cybersecurity & Ethical Hacking Program:
* **W3-PM1:** Password Cracking with John the Ripper (JTR) and Johnny GUI.
* **W3-PM2:** Password Cracking with Networkwalks Web-based Cryptographic Tools.

The project covers extracting cryptographic hashes from locked PDF files[cite: 7, 8, 16, 21], executing dictionary attacks[cite: 8, 14, 15, 18], recovering plaintext passwords[cite: 7, 8, 10, 14, 18], and decrypting target files to validate capture-the-flag (CTF) challenges[cite: 7, 8, 9, 11, 12].

---

## 🎯 Lab Objectives

- Configure the **Johnny GUI** frontend with the core John the Ripper engine inside Kali Linux[cite: 7, 10, 19].
- Extract `$pdf$` formatted hash signatures from locked PDF documents[cite: 7, 8, 16, 21].
- Execute offline dictionary attacks against extracted hashes[cite: 7, 8, 14, 15, 18].
- Recover plaintext passwords and decrypt target PDFs to verify captured flags[cite: 7, 8, 9, 11, 12].
- Differentiate between two-way document encryption and one-way cryptographic hashing.

---

## 🛠️ Tools & Environments

| Component | Platform / Tool | Role in Engagement |
| :--- | :--- | :--- |
| **Operating System** | Kali Linux 2026.2 (VirtualBox)[cite: 9, 10, 17] | Primary attack and document analysis environment[cite: 7, 9, 10, 17]. |
| **Cracking Engine** | John the Ripper (JTR) Jumbo | Core command-line cryptographic audit engine. |
| **Cracking Frontend** | Johnny GUI v2.2[cite: 7] | Session manager and graphical execution engine for JTR[cite: 7, 10, 18, 19]. |
| **Web Utilities** | Networkwalks Hash Calculator & Password Cracker | Client-side hash extraction and dictionary recovery[cite: 8, 14, 15, 16]. |
| **Hash Extractor** | OnlineHashCrack (`pdf2john`)[cite: 7] | Web-based extraction of `$pdf$` strings from encrypted PDFs. |
| **Document Viewer** | Document Viewer (Evince / Acrobat)[cite: 7, 9, 11] | Decryption verification and captured flag inspection[cite: 7, 8, 9, 11]. |

---

## 📂 Repository File Structure

```text
├── README.md                           # Master documentation
├── hashes/
│   ├── hash1.txt                       # Extracted $pdf$ hash for PDF 1
│   ├── hash2.txt                       # Extracted $pdf$ hash for PDF 2
│   └── hash3.txt                       # Extracted $pdf$ hash for PDF 3
├── screenshots/
│   ├── Screenshot-533.jpg              # Uploading My-Locked-PDF1.pdf to OnlineHashCrack
│   ├── Screenshot-534.jpg              # Extracted $pdf$ hash for PDF 1
│   ├── Screenshot-535.jpg              # Saving hash1.txt to Kali desktop
│   ├── Screenshot-536.png              # Loading hash1.txt into Johnny GUI
│   ├── Screenshot-537.png              # Johnny successfully cracked PDF 1 ('password1')
│   ├── Screenshot-539.jpg              # Networkwalks Hash Calculator for PDF 2
│   ├── Screenshot-540.jpg              # Networkwalks Cracker input for PDF 2
│   ├── Screenshot-541.jpg              # Networkwalks Cracker cracked PDF 2 ('password1')
│   ├── Screenshot-542.jpg              # Unlocking My-Locked-PDF2.pdf
│   ├── Screenshot-543.jpg              # Flag 2 Captured
│   ├── Screenshot-544.jpg              # Flag 1 Captured
│   ├── Screenshot-545.png              # Johnny successfully cracked PDF 3 ('1qaz2wsx')
│   └── Screenshot-546.jpg              # Flag 3 Captured
└── targets/
    ├── My-Locked-PDF1.pdf              # Challenge PDF 1
    ├── My-Locked-PDF2.pdf              # Challenge PDF 2
    └── My-Locked-PDF3.pdf              # Challenge PDF 3
