# 🔹 Secure Networking & Security Monitoring - Homelab 

*A self-hosted, security-hardened networking project leveraging VPN, firewalls, and security monitoring tools for encrypted remote access and network protection.*

---

## 📌 Project Overview
This project serves as a **homelab**, focusing on **secure networking, traffic monitoring, and access control** using open-source security tools. The setup includes a **Tailscale-powered VPN exit node**, firewall hardening with **iptables & UFW**, **Suricata for IDS/IPS**, **Wazuh for centralized security monitoring**, and **AdGuard Home for network-wide DNS filtering**.

Additionally, an **old Windows laptop** has been repurposed to act as a **dedicated Wazuh SIEM server and monitoring station**.

### 🚀 Objectives:
- ✅ Implement **a VPN-based secure network using Tailscale**.
- ✅ Deploy **firewall rules (iptables & UFW) for access control**.
- ✅ Monitor **network traffic & detect threats with Suricata IDS/IPS**.
- ✅ Set up **Wazuh SIEM for centralized security analysis**.
- ✅ Utilize an **old Windows laptop** as a **security monitoring dashboard**.
- ✅ **Future-Proofing**: Transition into a **dedicated homelab setup** in the future.

---

## 🛠️ Tools & Technologies

### 🔹 Networking & Security
- **VPN**: Tailscale (Encrypted Remote Access, Exit Node)
- **Firewall**: iptables + UFW (Traffic Filtering, Security Hardening)
- **Intrusion Detection**: Suricata (IDS/IPS, Packet Inspection)
- **SIEM & Monitoring**: Wazuh (Security Log Analysis, Threat Detection)
- **DNS Filtering**: AdGuard Home (Alternative to Pi-hole)

### 🔹 OS & Platforms
- **Ubuntu Server 22.04** (Firewall, VPN, IDS)
- **Windows 10** (Repurposed for Wazuh SIEM & Security Monitoring)
- **Raspberry Pi 4** (Tailscale Exit Node, AdGuard Home)

---

## ⚙️ Implementation Steps

### 1️⃣ Configuring a Secure VPN Exit Node with Tailscale
- Installed **Tailscale** on a **Raspberry Pi 4**.
- Enabled **Exit Node mode** to allow remote devices to route traffic securely.
- Configured **firewall rules** to restrict unauthorized access.

### 2️⃣ Firewall Hardening with iptables & UFW
- Enabled **UFW (Uncomplicated Firewall)** for simple rule management.
- Configured **iptables** for fine-tuned packet filtering & access control.
- Implemented **fail2ban** to protect against brute-force attacks.

### 3️⃣ Deploying Suricata for Intrusion Detection & Prevention
- Installed **Suricata IDS/IPS** on the Ubuntu server.
- Configured **WAN & LAN interfaces** for traffic monitoring.
- Applied **Emerging Threats rulesets** to detect malicious activity.

### 4️⃣ Setting Up Wazuh SIEM for Security Monitoring
- Installed **Wazuh Agent** on the Ubuntu server.
- Configured **log forwarding** to a **Wazuh SIEM instance**.
- Integrated **Suricata logs** with Wazuh for **correlated threat analysis**.

### 5️⃣ Integrating the Old Windows Laptop for SIEM Monitoring
- Installed **Wazuh Server** on the **Windows 10 laptop**.
- Configured it to **aggregate and visualize security logs** from the Ubuntu server.
- Installed **Grafana & ELK Stack** for **advanced security dashboards**.
- Enabled **remote access via Tailscale** for **secure log analysis**.

### 6️⃣ Network-Wide DNS Filtering with AdGuard Home
- Installed **AdGuard Home** on the Raspberry Pi.
- Configured **custom blocklists** for malware & ad filtering.
- Set **AdGuard as the DNS resolver** for all network devices.

---

## 🔹 Key Skills Developed
✔ **Firewall Security** – Configured **iptables & UFW** for traffic filtering.  
✔ **VPN Networking** – Set up **Tailscale exit node** for encrypted remote access.  
✔ **Intrusion Detection & Prevention** – Used **Suricata IDS/IPS** to monitor network traffic.  
✔ **Security Monitoring & SIEM** – Deployed **Wazuh for centralized security event analysis**.  
✔ **Network Hardening** – Enforced **SSH security, access control, and threat detection**.  
✔ **Traffic Filtering** – Used **AdGuard Home for DNS-based malware & ad blocking**.  
✔ **SIEM Dashboarding** – Repurposed **Windows laptop for security monitoring**.

---

## 📌 Hardware Used
- **Raspberry Pi 4 (4GB RAM)** – Running **Tailscale Exit Node & AdGuard Home**.
- **Ubuntu Server (x86 or ARM)** – Running **firewall, Suricata IDS, and Wazuh Agent**.
- **Old Windows Laptop** – Running **Wazuh SIEM server & security dashboards**.

---

## 🔮 Future Scope
This **homelab project** lays the foundation for a **dedicated homelab setup** with advanced features:

- ✔ **Transition to OPNsense/pfSense** for more granular firewall control.
- ✔ **Deploy Wazuh as a full SIEM server** with a custom dashboard.
- ✔ **Expand IDS/IPS capabilities** by integrating Suricata with external threat intelligence feeds.
- ✔ **Automate security updates & monitoring** for proactive defense.
- ✔ **Deploy a self-hosted VPN gateway** for improved remote access security.

---

## 🔗 GitHub Repository
##*[View full implementation details & configurations](#)*  

---

## 📌 Conclusion
This **homelab project** successfully implements **a self-hosted, security-enhanced network infrastructure** with **firewall protection, VPN tunneling, and threat monitoring**. It provides **strong network security** while maintaining **scalability for future homelab expansion**.

---

