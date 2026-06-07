<div align="center">

<img src="https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-3.0.3-black?style=for-the-badge&logo=flask&logoColor=white"/>
<img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Modules-30-orange?style=for-the-badge"/>
<img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge"/>

<br/>
<br/>

<h1>🛡️ CyberScan Pro</h1>
<h3>All-in-One Cybersecurity Intelligence Platform</h3>

<p><strong>30 offensive & defensive security modules in a single, self-hosted web dashboard.</strong></p>

<a href="https://anshul2414.github.io/cyberscan-pro">🌐 Live Demo</a> •
<a href="#-quick-start">🚀 Quick Start</a> •
<a href="#-modules">📦 Modules</a> •
<a href="#-screenshots">📸 Screenshots</a> •
<a href="#-docker">🐳 Docker</a>

<br/>

![CyberScan Pro Banner](https://img.shields.io/badge/CyberScan_Pro-v2.0-orange?style=flat-square&logo=shield&logoColor=white)

</div>

---

## ✨ Overview

**CyberScan Pro** is a powerful, self-hosted cybersecurity intelligence platform built with Python & Flask. Designed for **penetration testers**, **security researchers**, and **ethical hackers**, it combines 30 active security scanning modules into one slick, authenticated web dashboard — no API keys, no cloud SaaS subscriptions, just pure recon and analysis on your own infrastructure.

> Built by [Anshul](https://anshul2414.github.io) — Penetration Tester & Certified Ethical Hacker (CEH)

---

## 📦 Modules

### 🔵 Core Reconnaissance (16 modules)

| # | Module | Description |
|---|--------|-------------|
| 1 | **URL Check** | Analyze URL safety, redirects & response metadata |
| 2 | **Port Scan** | TCP port scanning with service detection |
| 3 | **DNS Lookup** | Full DNS enumeration (A, MX, NS, TXT, AAAA) |
| 4 | **SSL Inspector** | Certificate chain, expiry, cipher suite analysis |
| 5 | **WHOIS Lookup** | Domain registration & ownership data |
| 6 | **Tech Detect** | Identify web technologies, frameworks & CMS |
| 7 | **Email Security** | SPF, DKIM, DMARC validation & analysis |
| 8 | **Security Headers** | HTTP security header audit (HSTS, CSP, X-Frame) |
| 9 | **CORS Analyzer** | Cross-Origin Resource Sharing misconfiguration check |
| 10 | **WAF Detect** | Web Application Firewall fingerprinting |
| 11 | **Subdomain Enum** | Passive subdomain discovery & enumeration |
| 12 | **IP Geolocation** | IP intelligence — ASN, ISP, geo, threat classification |
| 13 | **Hash Tools** | MD5, SHA-1, SHA-256/512 generation & comparison |
| 14 | **Password Analyzer** | Strength scoring, entropy calculation, breach pattern check |
| 15 | **Robots.txt Parser** | Hidden paths and disallowed resource discovery |
| 16 | **CVE Search** | Search CVE database for vulnerability intelligence |

### 🔴 Advanced Offensive Modules (14 modules)

| # | Module | Description |
|---|--------|-------------|
| 17 | **Traceroute** | Network path tracing & hop latency analysis |
| 18 | **Dir Fuzzer** | Directory & endpoint brute-force enumeration |
| 19 | **XSS / SQLi / LFI Scanner** | Automated injection vulnerability scanner |
| 20 | **Open Redirect** | Open redirect chain detection & verification |
| 21 | **Cookie Analyzer** | Cookie flags, HttpOnly, Secure, SameSite audit |
| 22 | **JWT Analyzer** | JWT decode, algorithm audit, key-confusion detection |
| 23 | **TLS Deep Scan** | TLS version, cipher strength & certificate pinning |
| 24 | **Firewall Detect** | Active firewall & IDS/IPS detection techniques |
| 25 | **Email Header Forensics** | Full email header trace & spoofing analysis |
| 26 | **CIDR Scanner** | Bulk IP range scanning & host discovery |
| 27 | **Banner Grabber** | Service banner collection for fingerprinting |
| 28 | **API Security Tester** | REST/GraphQL endpoint enumeration & auth testing |
| 29 | **Network Fingerprinter** | OS & service stack fingerprinting |
| 30 | **SSRF / Cloud Probe** | SSRF detection & cloud metadata exposure testing |

---

## 🚀 Quick Start

### Option 1 — Python (Local)

```bash
# 1. Clone the repository
git clone https://github.com/anshul2414/cyberscan-pro.git
cd cyberscan-pro

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run the app
python app.py
```

Open **http://localhost:5000** in your browser.

> Default credentials: `admin` / `admin123`  
> ⚠️ **Change these before any deployment!**

---

### Option 2 — Windows (One-click)

```bat
# Double-click run.bat or execute:
run.bat
```

---

## 🐳 Docker

```bash
# Build & run with Docker Compose
docker-compose up -d

# App runs on http://localhost:8080
```

**Customize credentials via environment variables in `docker-compose.yml`:**

```yaml
environment:
  - AUTH_USERNAME=your_username
  - AUTH_PASSWORD=your_secure_password
  - SECRET_KEY=your-random-secret-key-here
```

---

## 🔐 Authentication

CyberScan Pro ships with **session-based authentication**:

- Login required to access all modules
- Credentials are set via environment variables
- Secret key protects session cookies
- All scan history stored in local SQLite database

---

## 📸 Screenshots

> Dashboard · Login · Scan Results

```
┌─────────────────────────────────────────────────────────────┐
│  🛡️ CyberScan Pro                               [Logout]    │
├──────────────┬──────────────────────────────────────────────┤
│              │                                              │
│  📡 Recon    │   Port Scan Results — scanme.nmap.org        │
│  🔍 Web      │   ┌────────────┬────────┬──────────────────┐ │
│  🔐 Auth     │   │ Port       │ State  │ Service          │ │
│  🧪 Inject   │   ├────────────┼────────┼──────────────────┤ │
│  📊 Network  │   │ 22/tcp     │ OPEN   │ SSH              │ │
│  🔑 Crypto   │   │ 80/tcp     │ OPEN   │ HTTP             │ │
│  📜 History  │   │ 443/tcp    │ OPEN   │ HTTPS            │ │
│              │   └────────────┴────────┴──────────────────┘ │
└──────────────┴──────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Backend** | Python 3.12, Flask 3.0 |
| **Frontend** | Vanilla JS, Chart.js, Font Awesome, Geist UI |
| **Database** | SQLite (scan history) |
| **Server** | Gunicorn (production) |
| **Container** | Docker + Docker Compose |
| **DNS** | dnspython |
| **WHOIS** | python-whois |

---

## 📁 Project Structure

```
cyberscan-pro/
├── app.py                  # Main Flask application (30 modules)
├── requirements.txt        # Python dependencies
├── Dockerfile              # Container build config
├── docker-compose.yml      # Multi-container orchestration
├── run.bat                 # Windows quick-start script
└── templates/
    ├── index.html          # Main dashboard UI
    └── login.html          # Authentication page
```

---

## ⚠️ Legal Disclaimer

> **CyberScan Pro is designed for authorized security testing and educational purposes only.**
>
> Always obtain **explicit written permission** before scanning any system, network, or domain you do not own. Unauthorized scanning may violate the Computer Fraud and Abuse Act (CFAA), the UK Computer Misuse Act, or equivalent laws in your jurisdiction.
>
> The author assumes no liability for misuse of this tool.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/new-module`
3. Commit your changes: `git commit -m 'Add: new security module'`
4. Push to branch: `git push origin feature/new-module`
5. Open a Pull Request

---

## 📬 Contact

**Anshul** — Penetration Tester & Ethical Hacker

- 🌐 Portfolio: [anssec.netlify.app](https://anssec.netlify.app)
- 💼 LinkedIn: [linkedin.com/in/anshul-9800a3275](https://linkedin.com/in/anshul-9800a3275)
- 🐙 GitHub: [github.com/anshul2414](https://github.com/anshul2414)
- 🎯 TryHackMe: [tryhackme.com/p/anshul28054](https://tryhackme.com/p/anshul28054)

---

## 📄 License

This project is licensed under the **MIT License** — see [LICENSE](LICENSE) for details.

---

<div align="center">

⭐ **If you find this useful, drop a star — it helps a lot!** ⭐

Made with ❤️ by [Anshul](https://github.com/anshul2414)

</div>
