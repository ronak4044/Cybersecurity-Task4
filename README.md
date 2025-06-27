# 🔐 Task 4 - Linux Firewall Configuration using UFW (Kali Linux)

## 📌 Objective
To configure and test basic firewall rules using *UFW (Uncomplicated Firewall)* in Kali Linux. The goal is to demonstrate control over network traffic by blocking and allowing specific ports, and to understand how a firewall filters incoming traffic.

---

## 🛠 Tools Used
- 🐧 Kali Linux (Debian-based)
- 🔥 UFW (Uncomplicated Firewall)
- 💬 Telnet (for testing blocked ports)
- 📸 Screenshot Tool (for documentation)

---

## 📋 Steps Performed

### ✅ 1. Installed UFW
```bash
sudo apt update
sudo apt install ufw -y

🔄 2. Enabled UFW

sudo ufw enable

🔍 3. Checked Firewall Status

sudo ufw status verbose

🚫 4. Blocked Port 23 (Telnet)

sudo ufw deny 23/tcp

🧪 5. Tested the Rule

telnet localhost 23

🧠 Result: Connection failed: Connection refused — ✅ Port is successfully blocked.

✅ 6. Allowed Port 22 (SSH)

sudo ufw allow 22/tcp

♻ 7. Removed Telnet Rule to Restore State

sudo ufw delete deny 23/tcp


---

📷 Screenshots

UFW status with rule list

Terminal output of Telnet showing blocked connection
