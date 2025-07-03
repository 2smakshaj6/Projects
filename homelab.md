# Secure Networking & Security Monitoring – My DIY Homelab Setup

*A hands-on, self-hosted security project where I turned spare devices into a VPN-secured, firewall-protected, threat-monitored network.*

---

## What This Is  
This is my homegrown secure network build, mixing practicality with curiosity. Using tools like Tailscale, Suricata, Wazuh, and AdGuard Home, I set up a system with VPN access, firewall hardening, traffic inspection, centralized logging, and DNS-level filtering.

One highlight: I repurposed an old Windows laptop into a fully functioning SIEM dashboard.

---

## Why I Built It  
I wanted to go beyond theory and actually deploy the tools I’ve been learning about in cybersecurity. This project helped me practice VPN setup, access control, monitoring, and incident response—all in a safe, self-contained environment.

---

## Tech Stack & Tools

| Category              | Tools Used                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| VPN                   | Tailscale (remote access + exit node)                                       |
| Firewall              | UFW + iptables (access control, brute force protection with fail2ban)       |
| Intrusion Detection   | Suricata (real-time traffic inspection + threat rulesets)                   |
| Security Monitoring   | Wazuh + ELK + Grafana (log aggregation & dashboards)                         |
| DNS Filtering         | AdGuard Home (network-wide filtering for ads and malware)                   |
| Hardware              | Raspberry Pi 4, Ubuntu Server, Windows 10 laptop                            |

---

## How I Did It

### Tailscale VPN with Exit Node  
Installed Tailscale on a Raspberry Pi 4 to enable remote access. Enabled the exit node feature and locked it down with firewall rules.

### Firewall Hardening (UFW + iptables)  
Used UFW for general rule sets and iptables for detailed packet filtering. Added fail2ban to block brute-force SSH attempts.

### Suricata IDS/IPS  
Set up Suricata on the Ubuntu server to inspect LAN and WAN traffic using the Emerging Threats rule set. Tuned it to reduce noise and surface actionable alerts.

### Wazuh SIEM + Dashboards  
Repurposed an old Windows 10 laptop to run Wazuh, which collects logs from my network devices. Combined it with the ELK stack and Grafana to create visual dashboards.

### DNS Filtering with AdGuard Home  
Installed AdGuard on the Raspberry Pi to block unwanted domains and filter malware at the DNS level. All my devices now route DNS queries through it.

---

## What I Learned

- VPN setup and exit node configuration with Tailscale  
- Real-world application of iptables and UFW for layered access control  
- Deploying and tuning Suricata for meaningful intrusion detection  
- Building a centralized SIEM pipeline with Wazuh, Elasticsearch, and Grafana  
- Setting up DNS-based filtering to improve privacy and reduce noise  
- Giving old hardware a purpose in security operations  

---

## Hardware Used

| Device             | Role                                 |
|--------------------|--------------------------------------|
| Raspberry Pi 4     | VPN + DNS filtering                  |
| Ubuntu Server      | Main system for Suricata and Wazuh agent |
| Windows Laptop     | Wazuh server and dashboard host      |

---

## What's Next

- Replace the Wazuh server with a more stable Linux-based host  
- Experiment with pfSense or OPNsense for advanced firewalling  
- Add external threat intelligence feeds to Suricata  
- Automate security patching and alert triage  
- Integrate with self-hosted platforms like Proxmox or Nextcloud  

---

## See More

[View the GitHub repository](#) for setup files, config examples, and dashboards.

---

## Final Thoughts  
This homelab helped me solidify concepts I’d only encountered in theory. It gave me space to break things safely, troubleshoot, and think like a defender. And reviving old hardware made it even more satisfying.
