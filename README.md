# 🔒 Task 8: VPN Setup and Privacy Analysis 
## 🎯 Objective
To gain **hands-on experience with Virtual Private Networks (VPNs)** and understand their **role in protecting privacy, encryption, anonymity**, and **secure communication**.

---

## 🛠 Tools Required
- Free VPN provider (choose one):
  - [ProtonVPN Free](https://protonvpn.com/free-vpn/)
  - [Windscribe Free](https://windscribe.com/)
- Browser: Chrome / Firefox / Brave
- Verification tools:
  - [https://whatismyipaddress.com](https://whatismyipaddress.com)
  - [DNS Leak Test](https://dnsleaktest.com/)
- Speed test: [https://fast.com](https://fast.com)

---

## ✅ Step-by-Step Implementation

### 🔹 Step 1: Register and Install VPN
- Go to the VPN provider’s website (e.g., ProtonVPN)
- Register for a **free account**
- Download and install the client (Windows/Linux/macOS)
- Login with your credentials

📸 Screenshot: `screenshots/vpn_installation_success.png`

---

### 🔹 Step 2: Connect to a VPN Server
- Launch the VPN app
- Choose **nearest available server** (for speed) or any foreign location (for IP masking)
- Click **Connect**

📸 Screenshot: `screenshots/vpn_connected.png`

---

### 🔹 Step 3: Verify VPN Tunnel
- Go to [whatismyipaddress.com](https://whatismyipaddress.com)
- Note new IP location → must reflect VPN location
- Go to [DNS Leak Test](https://dnsleaktest.com/) → ensure no DNS leakage

📸 Screenshot: `screenshots/vpn_dns_verified.png`

---

### 🔹 Step 4: Confirm Encrypted Communication
- Try accessing Google or YouTube
- Network traffic will be routed through encrypted tunnel
- Open Developer Tools → Network → See HTTPS traffic

---

### 🔹 Step 5: Disconnect VPN and Compare
- Disconnect VPN
- Revisit whatismyipaddress → you should see your **original IP**
- Repeat speed test on [fast.com](https://fast.com)

📸 Screenshot: `screenshots/vpn_disconnect_speedtest.png`

---

## 🧠 Deep Dive: VPN Architecture & Threat Analysis

### 📌 What is a VPN?
A **Virtual Private Network (VPN)** encrypts your internet traffic and tunnels it through a secure server, masking your IP address and securing your connection.

### 🔐 How does a VPN protect your privacy?
- **Encrypts traffic** using protocols like OpenVPN, IKEv2, WireGuard
- **Prevents ISP tracking** of your browsing habits
- **Hides your IP address** from websites
- **Defeats geo-restrictions** (e.g., for Netflix, censored sites)

### 🔄 VPN vs Proxy
| Feature | VPN | Proxy |
|--------|-----|--------|
| Encryption | ✅ Yes | ❌ No |
| Full device protection | ✅ Yes | ❌ No (usually browser only) |
| IP Masking | ✅ | ✅ |
| Speed | Slower | Faster |
| Use case | Security + privacy | Bypassing filters only |

---

### 🔐 VPN Encryption Explained
- VPNs use **AES-256** or **ChaCha20** encryption
- Establish **handshakes** using RSA or Elliptic Curve keys
- Creates a **secure tunnel** (IPSec, OpenVPN, WireGuard)
- Protects data from MITM (Man-in-the-Middle) attacks

### 🚫 VPN Limitations
- Slower speeds (due to encryption overhead)
- Some sites block VPN IP ranges
- Free VPNs may log data or inject ads
- Doesn’t protect against malware unless paired with antivirus

### ⚠️ VPN Can’t Guarantee 100% Anonymity
- VPN provider may log traffic
- Cookies and browser fingerprinting can still track users
- Use Tor + VPN for layered anonymity

### 🔍 VPN Protocols
| Protocol | Encryption | Speed | Security |
|---------|------------|-------|----------|
| OpenVPN | AES-256 | Medium | Very High |
| IKEv2 | AES-128/256 | Fast | High |
| WireGuard | ChaCha20 | Very Fast | High (newer) |
| PPTP | Weak | Fast | ❌ Outdated |

---

## 📚 Interview Questions & Answers

### 1. What is a VPN?
A VPN creates an encrypted tunnel between your device and the internet, hiding your IP address and protecting against eavesdropping.

### 2. How does a VPN protect privacy?
It masks your IP, encrypts your traffic, and prevents DNS leaks or ISP snooping.

### 3. VPN vs Proxy — which is better for security?
VPN. Proxies only hide IP addresses but do not encrypt data.

### 4. What is encryption in VPN?
The process of converting readable data into ciphertext using cryptographic algorithms (AES, ChaCha20).

### 5. Can VPN guarantee anonymity?
No. They reduce visibility, but true anonymity requires layered tools like Tor.

### 6. What VPN protocols are commonly used?
OpenVPN, WireGuard, IKEv2/IPSec — each with tradeoffs between speed and encryption.

### 7. What are limitations of VPNs?
Reduced speed, trust in provider, limited anonymity, possible IP bans.

### 8. How does VPN affect speed?
VPN adds latency due to encryption, server distance, and congestion. Paid plans usually perform better.

---

## 📂 GitHub Repository Structure
```
task8-vpn-privacy/
├── README.md
├── screenshots/
│   ├── vpn_installation_success.png
│   ├── vpn_connected.png
│   ├── vpn_dns_verified.png
│   └── vpn_disconnect_speedtest.png
└── vpn_analysis_report.md
```

---

## ✅ Task Completed By:
**Nitin sanap**  
Cybersecurity Intern — VPN & Encryption Analyst
