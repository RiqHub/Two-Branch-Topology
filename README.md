# Two-Branch-Topology
Designed and implemented a simulated enterprise network in Cisco Packet Tracer connecting a headquarters (HQ) and a branch office. The lab incorporates VLAN segmentation, inter-VLAN routing, dynamic routing with OSPF, DHCP services, wireless networking, and a secure site-to-site VPN for encrypted communication.

<img width="1466" height="633" alt="image" src="https://github.com/user-attachments/assets/c4329393-4f3d-4f8d-add3-0f19b5d0c7de" />


# 🏗️ Network Architecture
--------
Two-site topology:

- Headquarters (HQ)
- Branch Office
  
Hybrid switching design:

- Core/Distribution switch (aggregation)
- Access switches (endpoints connected across multiple switches)
- WAN connectivity between routers (simulated internet link)
- Site-to-site VPN overlay for secure communication

-------------------
# ⚙️ Key Configurations

🔹 VLAN Segmentation
Configured multiple VLANs for logical separation:

- VLAN 10 – SALES
- VLAN 20 – HR
- VLAN 30 – FINANCE
- VLAN 40 – LOGISTICS
- VLAN 50 – IT
- VLAN 60 GUEST

🔹 🔐 Site-to-Site VPN (IPsec)

Configured a secure tunnel between HQ and Branch routers using IPsec

Implemented:

- ISAKMP policy (Phase 1)
- Pre-shared key authentication
- Transform set (Phase 2 encryption)
- Crypto ACL to define interesting traffic
- Crypto map applied to WAN interface
- Encrypted traffic between internal subnets across sites

🔹 Inter-VLAN Routing

- Implemented Router-on-a-Stick on both routers
- Configured subinterfaces with 802.1Q encapsulation
- Enabled communication between VLANs

🔹 Dynamic Routing

- Deployed OSPF (single-area, Area 0)
- Enabled automatic route advertisement between HQ and Branch
- Verified neighbor adjacency and routing tables

🔹 DHCP Services

- Configured DHCP pools per VLAN
- Automated IP address assignment for wired and wireless clients
- Reserved gateway address ranges using excluded addresses

🔹 Wireless Networking

Integrated access points into switch infrastructure

- HQ: Guest WiFi 
- Branch: Guest WiFi

🔹 Network Security (Switching)

- Implemented port security on access ports:
- Limited MAC addresses per port
- Enabled sticky MAC learning
- Configured violation mode (restrict)

----------
# 🧪 Validation & Testing
<b>
- Verified DHCP assignment (ipconfig)
- Tested inter-VLAN communication (ping between VLANs)
- Confirmed OSPF routes (show ip route)
- Verified VPN configuration and tunnel establishment
- Tested secure communication between HQ and Branch networks
<b/>

