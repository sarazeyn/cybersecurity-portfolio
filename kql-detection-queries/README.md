# KQL Detection Queries for Microsoft Sentinel

Collection of 20+ KQL detection and hunting queries.

---

## 🔹 1. Brute Force Detection
```kql
SecurityEvent
| where EventID == 4625
| summarize FailedLogons = count() by Account, IP = IpAddress, bin(TimeGenerated, 1h)
| where FailedLogons > 10
let failures = SecurityEvent | where EventID == 4625 | summarize count() by Account;
let success = SecurityEvent | where EventID == 4624;
success
| join kind=inner failures on Account
| where count_ > 5
SecurityEvent
| where EventID == 4720
| where TargetUserName contains "admin"
DeviceProcessEvents
| where FileName == "powershell.exe"
| where ProcessCommandLine contains "-EncodedCommand"
Heartbeat
| join kind=inner (DeviceNetworkEvents) on DeviceId
| summarize cnt = count() by RemoteIP
| where cnt < 3
SecurityEvent
| where EventID == 4625 and LogonType == 10
| summarize Attempts=count() by Account, IpAddress
DeviceRegistryEvents
| where RegistryKey contains "Run" or RegistryKey contains "RunOnce"
DeviceEvents
| where ActionType contains "MalwareDetected"
SecurityEvent
| where EventID == 7045
SecurityEvent 
| where EventID == 1102
