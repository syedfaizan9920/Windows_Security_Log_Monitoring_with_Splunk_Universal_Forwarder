# 🔐 Windows Security Log Monitoring with Splunk Universal Forwarder

**Author:** Faizanullah Syed  
**Role:** SOC Analyst Trainee | Cybersecurity Enthusiast

---

## 📌 Project Overview

This project demonstrates how to forward **Windows Security Event Logs** using **Splunk Universal Forwarder (UF)** to a centralized **Splunk Enterprise Server** for real-time security monitoring.

Designed as part of a hands-on **SOC Analyst Assignment**, it focuses on setting up reliable log pipelines to detect and monitor events like logon attempts, failed login alerts, and privilege escalations (EventCodes 4624, 4625, 4672, etc.).

---

## 🚀 Key Features

- ✅ Forwarding logs via **Splunk UF on Windows**
- ✅ Monitors **Event Log: Security**
- ✅ Detects **successful/failed logins, admin access attempts**
- ✅ Uses **inputs.conf & outputs.conf**
- ✅ Fully validated with real-time Splunk search queries
- ✅ SEO-optimized keywords for learning and visibility

---

## 🧰 Tools & Technologies

- 🟦 Splunk Universal Forwarder (Windows)
- 🟧 Splunk Enterprise Server (Indexer)
- 🪟 Windows 10/11
- 🔐 WinEventLog:Security
- ⚙️ TCP Port 9997
- 📁 Config Files: `inputs.conf`, `outputs.conf`

---

### 📖 Step-by-Step Implementation

### 1. Install Splunk UF on Windows  
> Download from [Splunk Downloads](https://www.splunk.com/en_us/download/universal-forwarder.html)

### 2. Configure inputs.conf
```ini
[WinEventLog://Security]
disabled = 0
index = wineventlog


