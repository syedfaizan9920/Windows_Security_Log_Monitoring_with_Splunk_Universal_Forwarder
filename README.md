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

```

### 3. Configure outputs.conf
```ini
[tcpout]
defaultGroup = default-autolb-group

[tcpout:default-autolb-group]
server = <Your_Indexer_IP>:9997

```
### 4. Enable Receiving on Splunk Enterprise
```ini
Port: 9997

```

### 5. Restart Splunk UF
```ini
splunk restart

```
✅ Validation Example
Search Query in Splunk:
```ini
host="DESKTOP-IRBHD8G" sourcetype="WinEventLog:Security"

```

### Result:
Successfully indexed over 20,000+ Windows Security events, including:

EventCode 4624 – Logon Success

EventCode 4625 – Logon Failure

EventCode 4672 – Admin Privilege Use


---

✍️ Author

Faizanullah Syed

Cybersecurity & SOC Analyst Trainee

🌐 Connect with Me

📝 Blog: unmaskcyber.com 

## 🧠 #Tags

splunk universal forwarder, windows event logs, eventcode 4624, soc analyst project, log forwarding, inputs.conf, outputs.conf, tcp port 9997, splunk enterprise, siem project, real-time log collection, log monitoring, security log forwarder, windows splunk configuration, cybersecurity internship project, splunk data ingestion



