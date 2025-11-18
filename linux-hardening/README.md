# Linux Server Hardening

## Overview
This project focuses on securing a Linux server used for web or application hosting.

## Hardening Tasks
- Disabled root login over SSH
- Enforced key-based authentication
- Configured UFW/firewalld to allow only required ports
- Installed and configured Fail2Ban
- Enabled system logging and log rotation
- Managed users and groups with least-privilege access

## Example SSH Configuration
```bash
# /etc/ssh/sshd_config
PermitRootLogin no
PasswordAuthentication no
AllowUsers sara
sudo ufw allow 22/tcp
sudo ufw allow 443/tcp
sudo ufw enable

### 👉 Scroll down → Click **Commit new file**

✔ Folder #3 is done.

---

# 🔵 **STEP 2 — Create the `windows-server-lab` folder**

### 👉 Again click:  
**Code → Add file → Create new file**

### 👉 Name your file:

