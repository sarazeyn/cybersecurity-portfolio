# SOC Analyst Playbook

A complete Level 1 SOC Analyst reference with triage guides, investigation flows, and MITRE ATT&CK mapping.

---

## 🔹 1. Incident Response Workflow (L1 SOC)

1. **Alert received**
2. **Verify severity & source**
3. **Check metadata (timestamp, host, user, IP)**
4. **Run KQL queries or log searches**
5. **Validate if it's true positive or false positive**
6. **Collect supporting evidence**
7. **Escalate to L2 (if required)**
8. **Document investigation**
9. **Close incident with summary + recommendations**

---

## 🔹 2. Triage Checklist (L1 SOC)

- Who triggered the alert?
- What host or IP is involved?
- When did the activity happen?
- Repeated activity? (Failed logons, network scans)
- Any lateral movement?
- Any data exfiltration?
- Known malicious IP? (check VirusTotal)
- Was MFA enabled?
- Any unusual permissions?

---

## 🔹 3. MITRE ATT&CK Mapping (Common Techniques)

| Threat | Technique ID | Description |
|-------|--------------|-------------|
| Brute Force | T1110 | Multiple failed logon attempts |
| Process Injection | T1055 | Malware injecting into processes |
| Credential Dumping | T1003 | LSASS access |
| Phishing | T1566 | Malicious email |
| Lateral Movement | T1021 | Remote service connections |

---

## 🔹 4. Escalation Matrix

- **L1:** Initial triage, false/true positive validation  
- **L2:** Deep investigation, forensics, threat hunting  
- **L3:** Incident Response (IR), advanced containment, malware analysis  

---

## 🔹 5. Containment Actions

- Disable compromised account  
- Block IP via firewall  
- Isolate endpoint  
- Revoke access tokens  
- Reset password  
- Stop suspicious service/process  

---

## 🔹 6. Incident Documentation Template

**Incident ID:**  
**Type:** Brute force, malware, phishing  
**Source:** Sentinel alert  
**Summary:**  
**Impact:**  
**Actions taken:**  
**Evidence:**  
**Next steps:**  
**Status:** Closed / Escalated
