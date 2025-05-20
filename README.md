# CISCO-Packet-Tracer-Project
This project demonstrates a simulated enterprise-level network infrastructure using Cisco Packet Tracer. It models a secure and segmented environment featuring internal departments, a DMZ (De-Militarized Zone), and external access through routers and switches


---

## 🌐 Network Overview

The network is divided into distinct functional areas with interconnecting routers and switches to simulate real-world enterprise setups:

### 🔸 Internal Network Segments

| Department      | Subnet             | Devices                          |
|----------------|--------------------|----------------------------------|
| Intelligence    | 192.168.1.0/26     | PC, Laptop, Smartphone, Printer  |
| Reception       | 192.168.1.64/26    | PC, Smartphone                   |
| Operator_Home   | 192.168.1.128/26   | PC, Smartphone, DNS Server       |
| Office          | 192.168.1.192/26   | PC, Smartphone, Webcam           |

- **VLAN 20** is configured for mobile devices (smartphones).

### 🔸 DMZ (Demilitarized Zone)

| Server         | IP Address     | Description               |
|----------------|----------------|---------------------------|
| Web Server     | 192.168.2.2     | Hosts public-facing site  |
| Syslog Server  | 192.168.2.50    | Logs events and alerts    |
| Sniffer        | 192.168.2.1     | Monitors internal traffic |

### 🔸 External Network

| Device         | IP Address     | Description                    |
|----------------|----------------|--------------------------------|
| My Office      | 192.168.3.2     | External company server        |
| External Laptop| 192.168.3.3     | Used for external access       |

---

## 🔧 Configuration Overview

### Internal Routing

- `Internal_Router (192.168.1.x)` routes traffic between internal VLANs.
- Static or dynamic routing (e.g., RIP, OSPF) can be configured to handle intra-network communication.

### External Routing & DMZ

- `External_Router (192.168.2.3)` links DMZ to external network (`192.168.3.0/24`).
- DMZ allows controlled access to public-facing services while protecting internal networks.

### Wireless Access Points

- Each department has a dedicated **Access Point** connected to a switch.
- Wireless devices are logically segregated using VLAN 20.

---

## 🧪 Simulation Features

- IP addressing, subnetting, and inter-VLAN routing
- Public server access simulation via DMZ
- Wireless device integration
- Centralized logging (Syslog server)
- Network monitoring via Sniffer

---

## 🚀 How to Run

1. Open the `.pkt` file using **Cisco Packet Tracer** (v8.0+ recommended).
2. Power on devices and observe traffic between:
   - Internal departments
   - Internal to DMZ (e.g., accessing the web server)
   - External to DMZ or internal (test access control)
3. Use simulation mode to trace packets and monitor traffic with Sniffer or Syslog server.

---

## 🛠️ Future Enhancements

- Configure firewall rules between internal/DMZ/external zones
- Implement DHCP and NAT
- Integrate VPN for secure remote access
- Add redundancy via HSRP or dual routers

---

## 🧑‍💻 Author

Created by [Your Name]  
[Your Contact or GitHub Profile Link]

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

