
# Access Control Lists (ACL) Configuration — Cisco Packet Tracer Lab

This project demonstrates the implementation of **Access Control Lists (ACL)** in **Cisco Packet Tracer** to manage and secure network traffic across multiple routers.  
The configuration applies both **Standard** and **Extended ACLs** to control which hosts or networks can access specific destinations or services.

---

## 📘 Overview

Access Control Lists (ACLs) are a fundamental part of network security and traffic management.  
In this lab, ACLs are used to:
- Filter and control network traffic based on IP addresses, protocols, and ports  
- Restrict access between different subnets  
- Simulate real-world network policies using router configurations  

This setup helps visualize how ACLs affect data flow within a LAN or multi-router environment.

---

## 🧩 Network Topology

The topology consists of three routers and multiple end devices connected through switches.  
Each router is configured with routing and ACL rules to enforce access policies.  
A visual representation of the topology is included in the `/assets/` directory.

---

## 📂 Assets

All related files and screenshots are stored in the `/assets/` directory:
/assets/
├── ROUTER0CLI # Router 0 configuration
├── ROUTER1CLI # Router 1 configuration
├── ROUTER2CLI # Router 2 configuration
└── topology # Network topology diagram


---

## ⚙️ Tools Used
- **Cisco Packet Tracer**
- **Router & Switch CLI Configuration**

---

## 🧠 Key Features
- Implementation of **Standard** and **Extended** ACLs  
- Traffic control between internal networks  
- Verification using `ping`, `traceroute`, and web access  
- Simulation of real-world access restrictions  

---

## 🧾 Results

After applying ACL configurations, network access is properly restricted according to defined policies.  
Verification tests confirm that only permitted traffic passes through while unauthorized requests are blocked.

---

Router(config)# access-list 110 permit tcp 192.168.10.2 0.0.0.0 host 192.168.1.1 eq 80
Router(config)# access-list 110 deny ip any host 192.168.1.1
Router(config)# interface fa0/1
Router(config-if)# ip access-group 110 out

---


## 📅 Date
**November 13, 2025**


