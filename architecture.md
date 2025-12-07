# 🧱 Network Architecture & Design

This homelab uses a segmented network approach to simulate production environments found in enterprise SOC operations. Each LAN is isolated to prevent lateral movement while still allowing centralized log collection.

---

## 🔐 Network Topology

WAN → pfSense → LAN1 (Ubuntu)
→ LAN2 (Windows Server + Win10)
→ LAN3 (Splunk SIEM)


---

## 🌐 Subnet Table

| Segment | Subnet | Gateway | Purpose |
|---------|--------|---------|---------|
| LAN1 | 192.168.2.0/24 | 192.168.2.1 | Linux system for testing |
| LAN2 | 192.168.3.0/24 | 192.168.3.1 | Windows Server + Windows 10 |
| LAN3 | 192.168.4.0/24 | 192.168.4.1 | Splunk SIEM |

---

## 🎯 Design Objectives

1. **Complete LAN isolation**  
   - No direct communication between LAN1, LAN2, or LAN3  
   - All routing goes through pfSense

2. **Centralized logging**  
   - All hosts can reach **Splunk: 192.168.4.10**

3. **Realistic enterprise model**
   - Multi-OS environment  
   - Windows Server for AD / domain tests  
   - Ubuntu for Linux-side experiments  

4. **Safe, confined environment**
   - No external risky traffic  
   - No exposure of LAN segments to WAN

---

[ISP Router]
|
WAN
|
[pfSense]
/ |
LAN1 LAN2 LAN3
(Ubuntu) (Win) (Splunk)

---

This structure forms the foundation for SOC-style monitoring, detection engineering, and adversary simulation.

## 📌 Logical Diagram

