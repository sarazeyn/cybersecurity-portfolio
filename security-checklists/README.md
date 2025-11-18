# Security Checklists (Windows, Linux, Cloud)

---

# 🔹 Windows Server Security Checklist
- Enable Windows Firewall
- Disable SMBv1
- Enforce password policy (12+ chars)
- Enable MFA for admin users
- Apply least privilege access
- Configure audit policies
- Disable anonymous SID enumeration
- Enable Secure Boot

---

# 🔹 Linux Security Checklist
- Disable root SSH login
- Enforce key-based authentication
- Enable UFW/firewalld
- Install Fail2Ban
- Configure log rotation
- Remove unused packages
- Disable guest account
- Correct file permissions on /etc

---

# 🔹 Cloud Security Checklist (Azure)
- Enable Conditional Access
- Block legacy authentication
- Enable Defender for Cloud
- Enforce MFA for all users
- Use NSGs for all subnets
- Use Private Endpoints for storage & databases
- Use Key Vault for secrets
- Restrict RDP/SSH using Bastion
