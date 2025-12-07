# 🛡️ Proxmox + pfSense SOC Homelab  
A fully segmented Proxmox-based homelab designed for SOC analysis, network segmentation, and log collection with Splunk.

This project documents the setup of:

- pfSense firewall  
- 4 isolated network segments  
- Ubuntu VM  
- Windows Server  
- Windows 10 client  
- Splunk log collector  
- Full network isolation + controlled log flow  

---

## 🔧 Homelab Architecture

**Hypervisor:** Proxmox  
**Firewall:** pfSense  
**Log Collector:** Splunk (192.168.4.10)

Network Segments:

| Segment | Subnet | Purpose |
|--------|--------|---------|
| WAN | ISP DHCP | Internet uplink |
| LAN1 | 192.168.2.0/24 | Ubuntu VM |
| LAN2 | 192.168.3.0/24 | Windows Server + Win10 |
| LAN3 | 192.168.4.0/24 | Splunk server |

---

## 📅 7-Day Build Timeline  
This project was built using a structured 7-day plan:

### **Day 1 — Proxmox Network Setup**
- Created WAN + 3 LAN bridges  
- Verified persistent networking  

### **Day 2 — pfSense Installation**
- Configured WAN + LAN1/2/3 interfaces  
- Assigned gateways  
- Enabled DHCP  

### **Day 3 — Ubuntu VM Deployment**
- Assigned static IP  
- Tested routing & connectivity  

### **Day 4 — Windows Server + Win10**
- Deployed AD-capable host  
- Verified subnet segmentation  

### **Day 5 — Splunk Deployment**
- Installed Splunk on 192.168.4.10  
- Prepared to receive logs  

### **Day 6 — Firewall Segmentation**
- Blocked cross-LAN traffic  
- Allowed only logging to Splunk  

### **Day 7 — Documentation + Snapshots**
- Exported diagrams  
- Finalized write-up  

---

## 🔥 Purpose of This Lab

This lab demonstrates skills relevant to:

- Network segmentation  
- Firewall rule creation  
- SIEM log ingestion  
- Homelab design  
- Virtualization (Proxmox)  
- Multi-OS management  
- SOC analysis workflows  

---

## 📁 Documentation  
All detailed setup instructions can be found in `/docs`:

- `architecture.md`  
- `pfSense-setup.md`  
- `proxmox-networking.md`  
- `segmentation-rules.md`  
- `splunk-logging.md`  

---

## 📸 Screenshots  
See `/images` for diagrams and configurations.

---

⭐ *This homelab will continue evolving with detection labs, threat simulations, and logging exercises.*  
