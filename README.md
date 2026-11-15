![Splunk](https://img.shields.io/badge/Splunk-000000?style=for-the-badge&logo=splunk&logoColor=white)
![SIEM](https://img.shields.io/badge/SIEM-Dashboard-blue?style=for-the-badge)
![SOC](https://img.shields.io/badge/SOC-Analyst-red?style=for-the-badge)
![SSH](https://img.shields.io/badge/SSH-Brute_Force-green?style=for-the-badge)
![DNS](https://img.shields.io/badge/DNS-Log_Analysis-4FC3F7?style=for-the-badge)
![FTP](https://img.shields.io/badge/FTP-Log_Analysis-66BB6A?style=for-the-badge)
![SMTP](https://img.shields.io/badge/SMTP-Phishing_Detection-FF7043?style=for-the-badge)
![DHCP](https://img.shields.io/badge/DHCP-Rogue_Device-AB47BC?style=for-the-badge)
![Tunnel](https://img.shields.io/badge/Tunnel-Covert_Channel-FFA726?style=for-the-badge)
![SPL](https://img.shields.io/badge/SPL-Queries-orange?style=for-the-badge)

**A comprehensive SIEM lab portfolio with 6 Splunk dashboards covering SSH, DNS, FTP, SMTP, DHCP, and Tunnel threat analysis — built with SPL queries, importable XML, and geo-location threat intelligence.**

</div>

## 🎯 What This Project Covers

This repository contains **6 complete Splunk SIEM dashboards** built from scratch — each with a step-by-step lab guide, SPL queries, importable XML, and real log data.

| # | Dashboard | Events | Key Skills | Guide |
|---|-----------|--------|-----------|-------|
| 1 | 🛡️ **SSH Log Analysis** | 1,201 SSH events | Brute-force detection, failed login analysis, geo-location mapping | [`SSH_LOG_ANALYSIS.md`](SSH_LOG_ANALYSIS.md) |
| 2 | 🌐 **DNS Log Analysis** | 1,500 DNS events | DGA detection, NXDOMAIN analysis, suspicious domain hunting | [`DNS_LOG_ANALYSIS.md`](DNS_LOG_ANALYSIS.md) |
| 3 | 📁 **FTP Log Analysis** | 1,200 FTP events | File transfer monitoring, anonymous access detection, command analysis | [`FTP_LOG_ANALYSIS.md`](FTP_LOG_ANALYSIS.md) |
| 4 | 📧 **SMTP Log Analysis** | 1,000 email events | Phishing detection, attachment analysis, TLS compliance | [`SMTP_LOG_ANALYSIS.md`](SMTP_LOG_ANALYSIS.md) |
| 5 | 🖧 **DHCP Log Analysis** | 800 DHCP events | Rogue device detection, IP lease monitoring, asset discovery | [`DHCP_LOG_ANALYSIS.md`](DHCP_LOG_ANALYSIS.md) |
| 6 | 🔒 **Tunnel Log Analysis** | 1,000 tunnel events | Covert channel detection, protocol analysis, persistent backdoor hunting | [`TUNNEL_LOG_ANALYSIS.md`](TUNNEL_LOG_ANALYSIS.md) |

## 📸 Dashboard Previews

### 🛡️ SSH Log Analysis Dashboard

![SSH Dashboard](screenshots/dashboard-complete.png)

> **Panels:** Total SSH Events · Successful Logins · Failed Logins · Invalid User Attempts · Failed Logins by Username · Brute Force IPs · Geo-Location Map

---

### 🌐 DNS Log Analysis Dashboard

![DNS Dashboard](screenshots/dns-dashboard.png)

> **Panels:** Total DNS Queries · Successful Resolutions · NXDOMAIN Responses · Suspicious Queries · Top Queried Domains · Query Type Distribution · Suspicious Domain Table

---

### 📁 FTP Log Analysis Dashboard

![FTP Dashboard](screenshots/ftp-dashboard.png)

> **Panels:** Total FTP Events · Successful Transfers · Failed Operations · Suspicious Activity · Top Users · Command Distribution · Geo-Location Map

---

### 📧 SMTP Log Analysis Dashboard

![SMTP Dashboard](screenshots/smtp-dashboard.png)

> **Panels:** Total Emails · With Attachments · Unencrypted (No TLS) · Suspicious Emails · Top Senders · Attachment Types · Geo-Location Map

---

### 🖧 DHCP Log Analysis Dashboard

![DHCP Dashboard](screenshots/dhcp-dashboard.png)

> **Panels:** Total DHCP Events · Unique Devices · IP Assignments · Suspicious Devices · Message Type Distribution · Top Devices · Rogue Device Table

---

### 🔒 Tunnel Log Analysis Dashboard

![Tunnel Dashboard](screenshots/tunnel-dashboard.png)

> **Panels:** Total Tunnel Events · Tunnels Established · Tunnels Terminated · Suspicious Tunnels · Protocol Distribution · Top Sources · Geo-Location Map

---

## <img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="25"> Skills Demonstrated

| Category | Skills |
|----------|--------|
| **SIEM Operations** | Dashboard creation, panel configuration, shared time tokens, XML source editing |
| **SPL Queries** | `stats count`, `dc()`, `top`, `where`, `table`, `iplocation`, `geom`, `sort`, field filtering |
| **Threat Detection** | Brute-force identification, DGA/C2 detection, phishing triage, rogue device hunting, covert channel analysis |
| **Cloud Security** | AWS GuardDuty, S3→SQS→Splunk pipeline, IAM credential compromise response, MITRE ATT&CK Cloud mapping |
| **Log Analysis** | SSH, DNS, FTP, SMTP, DHCP, Tunnel — 6 source types |
| **Geo-Intelligence** | IP-to-country resolution, choropleth mapping, geo-blocking recommendations |
| **SOC Workflow** | Alert triage mindset, threat hunting queries, incident response playbooks, analyst tips embedded throughout |


### Option 1 — Follow the Step-by-Step Guide

1. Pick a dashboard from the table above
2. Upload the corresponding log data from the `data/` folder into Splunk
3. Follow the task-by-task instructions to build each panel manually
4. Learn SPL by doing ✅

### Option 2 — One-Click XML Import

1. Open Splunk → **Dashboards** → **Create New Dashboard**
2. Click **Edit** → **Source** (top-left)
3. Paste the XML from any of the 8 dashboard files in `xml/`:
   - [`xml/ssh_dashboard.xml`](xml/ssh_dashboard.xml) — SSH Dashboard
   - [`xml/dns_dashboard.xml`](xml/dns_dashboard.xml) — DNS Dashboard
   - [`xml/ftp_dashboard.xml`](xml/ftp_dashboard.xml) — FTP Dashboard
   - [`xml/smtp_dashboard.xml`](xml/smtp_dashboard.xml) — SMTP Dashboard
   - [`xml/dhcp_dashboard.xml`](xml/dhcp_dashboard.xml) — DHCP Dashboard
   - [`xml/tunnel_dashboard.xml`](xml/tunnel_dashboard.xml) — Tunnel Dashboard
4. Click **Save** → Done 🚀

## 📂 Project Structure

```
splunk-soc-project/
│
├── 📄 README.md                          ← You are here
├── 📄 SSH_LOG_ANALYSIS.md                ← SSH Dashboard guide
├── 📄 DNS_LOG_ANALYSIS.md                ← DNS Dashboard guide
├── 📄 FTP_LOG_ANALYSIS.md                ← FTP Dashboard guide
├── 📄 SMTP_LOG_ANALYSIS.md               ← SMTP Dashboard guide
├── 📄 DHCP_LOG_ANALYSIS.md               ← DHCP Dashboard guide
├── 📄 TUNNEL_LOG_ANALYSIS.md             ← Tunnel Dashboard guide
│
├── 📁 screenshots/
│   ├── 🖼️ dashboard-complete.png         ← SSH dashboard screenshot
│   ├── 🖼️ dns-dashboard.png              ← DNS screenshot
│   ├── 🖼️ ftp-dashboard.png              ← FTP screenshot
│   ├── 🖼️ smtp-dashboard.png             ← SMTP screenshot
│   ├── 🖼️ dhcp-dashboard.png             ← DHCP screenshot
│   ├── 🖼️ tunnel-dashboard.png           ← Tunnel screenshot
│
├── 📁 data/
│   ├── 📊 ssh_logs_new.json              ← 1,201 SSH authentication events
│   ├── 📊 dns_logs.json                  ← 1,500 DNS query events
│   ├── 📊 ftp_logs.json                  ← 1,200 FTP transfer events
│   ├── 📊 smtp_logs.json                 ← 1,000 SMTP email events
│   ├── 📊 dhcp_logs.json                 ← 800 DHCP lease events
│   ├── 📊 tunnel_logs.json               ← 1,000 tunnel traffic events

│
└── 📁 xml/
    ├── 📝 ssh_dashboard.xml              ← Importable Splunk XML (SSH)
    ├── 📝 dns_dashboard.xml              ← Importable Splunk XML (DNS)
    ├── 📝 ftp_dashboard.xml              ← Importable Splunk XML (FTP)
    ├── 📝 smtp_dashboard.xml             ← Importable Splunk XML (SMTP)
    ├── 📝 dhcp_dashboard.xml             ← Importable Splunk XML (DHCP)
    ├── 📝 tunnel_dashboard.xml           ← Importable Splunk XML (Tunnel)
```

## 🔧 Prerequisites

| Requirement | Details |
|-------------|---------|
| **Splunk** | Enterprise (local) or Cloud — [free trial](https://www.splunk.com/en_us/download.html) works |
| **GeoIP** | Built-in `iplocation` command + `geo_countries` lookup (ships with Splunk) |
| **Knowledge** | Basic SPL, network protocols (SSH, HTTP, DNS, FTP, SMTP, DHCP), tunneling concepts, AWS basics |


## 📊 Data Sources Overview

### SSH Logs (`ssh_logs_new.json`) — 1,201 events

| Field | Example | Purpose |
|-------|---------|---------|
| `id.orig_h` | `31.184.137.182` | Source IP (attacker) |
| `event_type` | `Failed SSH Login` | Event classification |
| `username` | `root`, `admin` | Targeted account |
| `auth_attempts` | `8` | Number of auth attempts per session |


### DNS Logs (`dns_logs.json`) — 1,500 events

| Field | Example | Purpose |
|-------|---------|---------|
| `query` | `malware-c2.evil.com` | Queried domain name |
| `qtype_name` | `A`, `TXT`, `MX` | DNS query type |
| `rcode_name` | `NOERROR`, `NXDOMAIN` | DNS response code |
| `classification` | `Suspicious` | Threat classification |

### FTP Logs (`ftp_logs.json`) — 1,200 events

| Field | Example | Purpose |
|-------|---------|---------|
| `user` | `anonymous`, `admin` | FTP username |
| `command` | `RETR`, `STOR`, `DELE` | FTP command |
| `arg` | `/tmp/malware.exe` | Target file path |
| `reply_code` | `226`, `550` | FTP reply code |

### SMTP Logs (`smtp_logs.json`) — 1,000 events

| Field | Example | Purpose |
|-------|---------|---------|
| `mailfrom` | `noreply@phishing-site.tk` | Sender email address |
| `rcptto` | `ceo@company.com` | Recipient email |
| `subject` | `URGENT: Password Reset` | Email subject line |
| `attachment_type` | `.exe`, `.pdf` | Attachment file type |

### DHCP Logs (`dhcp_logs.json`) — 800 events

| Field | Example | Purpose |
|-------|---------|---------|
| `msg_type` | `DISCOVER`, `ACK` | DHCP message type |
| `mac_address` | `DE:AD:BE:EF:00:01` | Device MAC address |
| `hostname` | `ROGUE-DEVICE` | Device hostname |
| `leased_ip` | `192.168.1.105` | Assigned IP address |

### Tunnel Logs (`tunnel_logs.json`) — 1,000 events

| Field | Example | Purpose |
|-------|---------|---------|
| `tunnel_type` | `GRE`, `Teredo`, `6to4` | Tunnel protocol |
| `action` | `tunnel_established` | Tunnel event type |
| `orig_bytes` | `245000` | Data transferred (bytes) |
| `classification` | `Suspicious` | Threat classification |


