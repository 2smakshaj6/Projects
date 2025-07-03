# WireGuard VPN on AWS – Secure Personal VPN Setup

This project is about setting up a **personal VPN** using **WireGuard** on an **Ubuntu EC2 instance**, giving me secure, encrypted internet access—especially on public or untrusted networks.

---

## Why I Built This

I wanted a lightweight, fast, and secure way to encrypt my internet traffic—something more efficient than OpenVPN or commercial VPN apps. Setting up **WireGuard** on **AWS EC2** gave me full control over the setup, cost, and security.

---

## Key Goals

- Encrypt all outbound traffic to maintain privacy on public Wi-Fi  
- Route traffic securely through a VPS under my control  
- Harden the VPN server to prevent abuse or unauthorized access  
- Explore real-world configuration of firewalls and system hardening  

---

## Tools & Technologies

- **WireGuard** – Fast, modern VPN protocol  
- **AWS EC2** – Ubuntu 22.04 VPS host  
- **iptables** – Packet filtering and NAT  
- **fail2ban** – SSH brute-force protection  
- **Cloudflare WARP (optional)** – Additional routing & encryption layer  

---

## How I Set It Up

### 1. Launched EC2 Instance
- Spun up a lightweight Ubuntu 22.04 instance on AWS (t2.micro)
- Configured the **security group** to allow **UDP traffic on port 51820**

### 2. Installed & Configured WireGuard
- Installed WireGuard via the official PPA
- Generated server/client keys
- Configured `wg0.conf` on both ends to enable tunneling

### 3. Enabled IP Forwarding & NAT
- Edited sysctl settings to enable IP forwarding
- Used `iptables` to NAT outbound traffic through the EC2's public IP

### 4. Hardened the Server
- Installed and configured **fail2ban** to monitor SSH  
- Locked down unused ports in UFW  
- Disabled root login and enforced key-based SSH authentication

### 5. (Optional) Layered Cloudflare WARP  
- Tested using **Cloudflare WARP** as an upstream DNS or tunnel to further obfuscate traffic  
- Verified DNS leak protection

---

## Lessons Learned

- WireGuard is refreshingly simple to configure compared to legacy VPNs  
- AWS’s security groups make it easy to restrict VPN access to your own IPs if needed  
- IP forwarding + NAT setup can be tricky without logging enabled—debugging taught me a lot  
- Fail2ban is a simple but effective way to reduce brute-force attempts on exposed instances  

---

## What’s Next

- Add automatic connection for mobile devices via QR config  
- Try deploying this setup on other cloud platforms (e.g., Oracle Cloud, DigitalOcean)  
- Integrate with Pi-hole or AdGuard for DNS filtering  
- Set up monitoring and alerting for the EC2 instance  

---

## Repo

[View on GitHub](https://github.com/your-repo/personal-vpn-setup)

---

## Final Note

This was a great weekend project to brush up on Linux networking, firewall management, and VPN configuration. If you're thinking about setting up your own VPN, I highly recommend trying WireGuard—simple, fast, and secure.
