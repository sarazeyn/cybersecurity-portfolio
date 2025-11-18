# Microsoft Sentinel SIEM Lab

## Overview
This project demonstrates how I deployed Microsoft Sentinel, connected security logs, and built KQL queries to detect suspicious activity.

## What I did
- Created an Azure Log Analytics workspace
- Enabled Microsoft Sentinel
- Connected security event logs
- Built custom KQL queries
- Investigated alerts and created analytics rules

## Example KQL Query
```kql
SecurityEvent
| where EventID == 4625
| summarize FailedLogons = count() by Account, IPAddress = IpAddress, bin(TimeGenerated, 1h)
| where FailedLogons > 10

4. Scroll down → **Commit changes**

Your first folder is created! 🎉  

---

## 🔵 **STEP B — Add the other folders the same way**

Repeat the same process for:

### Folder 2  
`azure-network-security/README.md`

### Folder 3  
`linux-hardening/README.md`

### Folder 4  
`windows-server-lab/README.md`

Paste the content I gave for each folder.

---

# ⭐ When all folders are added — your GitHub will look like this:


4. Scroll down → **Commit changes**

Your first folder is created! 🎉  

---

## 🔵 **STEP B — Add the other folders the same way**

Repeat the same process for:

### Folder 2  
`azure-network-security/README.md`

### Folder 3  
`linux-hardening/README.md`

### Folder 4  
`windows-server-lab/README.md`

Paste the content I gave for each folder.

---

# ⭐ When all folders are added — your GitHub will look like this:

