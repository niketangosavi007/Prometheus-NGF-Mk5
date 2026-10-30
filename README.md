# Prometheus-NGF-Mk5
# 🔥 Prometheus Firewall Mk5
### AI-Assisted Linux Firewall & Intelligent Network Threat Detection

Prometheus Firewall Mk5 is an experimental Python-based network security project designed to inspect network traffic, identify suspicious packets, perform deep packet inspection, and automate threat response.

The project combines AI-assisted packet analysis, network monitoring, blockchain-based audit logging, and JWT-secured API access into a unified firewall architecture.

## 🚀 Key Features

- **Real-Time Packet Inspection (RTPI):** Captures and analyzes network packets using Scapy.
- **AI Threat Detection:** Uses PyTorch and TorchScript for packet feature scoring.
- **Deep Packet Inspection (DPI):** Performs additional payload inspection on suspicious packets.
- **JA3-Style Fingerprinting:** Includes an experimental TLS fingerprinting function.
- **Blockchain Logging:** Designed for security event logging through Hyperledger Fabric.
- **Automated IP Blocking:** Integrates with Fail2Ban for suspicious source IP response.
- **JWT Authentication:** Protects firewall management API endpoints.
- **Multithreaded Processing:** Supports asynchronous packet processing through worker threads.

## 🛠️ Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Packet Analysis | Scapy |
| AI / ML | PyTorch, TorchScript |
| API Framework | Flask |
| Authentication | JWT |
| Blockchain | Hyperledger Fabric |
| Automated Blocking | Fail2Ban |
| Network Protocol Analysis | TCP/IP |

## 🏗️ Architecture

```text
             Network Traffic
                    |
                    v
             Scapy Packet Capture
                    |
                    v
          Real-Time Packet Inspection
                    |
                    v
            AI Threat Scoring
                    |
             Suspicious Packet?
                    |
                    v
          Deep Packet Inspection
                    |
             Threat Detected
                    |
          +---------+---------+
          |         |         |
          v         v         v
       Logging   Blockchain  Fail2Ban
          |
          v
      Security Audit

          Flask REST API
                 |
          JWT Authentication
                 |
          Firewall Status
```

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Prometheus-Mk5.git
cd Prometheus-Mk5
```

### 2. Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install scapy torch flask PyJWT
```

Hyperledger Fabric and Fail2Ban require separate environment-specific configuration. The Python imports in the prototype may need adaptation to their actual SDKs and interfaces.

## ▶️ Execution

Run the firewall prototype with the required privileges for packet capture:

```bash
sudo python3 firewall.py
```

The Flask API listens on:

```text
http://127.0.0.1:8080
```

### API Endpoint

**GET `/firewall/status`**

Requires a valid JWT token in the Authorization header.

Example:

```http
GET /firewall/status
Authorization: Bearer YOUR_JWT_TOKEN
```

## 🔐 Security Considerations

- Replace the demonstration JWT secret with a securely managed secret.
- Train and validate the AI model before relying on its threat scores.
- Implement proper TLS ClientHello parsing for actual JA3 fingerprinting.
- Validate blockchain and Fail2Ban integrations before enabling automated response.
- Add packet-processing limits and resource management.
- Test firewall behavior in an isolated lab environment.

## ⚠️ Development Status

**Version:** Mk5

**Status:** Experimental Prototype

This project is intended for cybersecurity research, network defense experimentation, and educational purposes. Some components are demonstration implementations or require additional integration and validation.

## 🎯 Project Objective

To explore an intelligent Linux firewall architecture combining packet inspection, AI-assisted threat detection, automated response, and tamper-evident security logging.

## 👨‍💻 Author

**Niketan Gosavi**

Cybersecurity Research & Development

GitHub: https://github.com/niketangosavi07

---

*Prometheus Firewall Mk5 – Intelligent Network Defense.*
