# Network Connectivity Troubleshooting Methodology Based on the OSI Model

This guide establishes the Standard Operating Procedure (SOP) for diagnosing, isolating, and resolving network incidents in IT technical support. A **Bottom-Up** approach is applied (from Layer 1 to higher layers), ensuring physical infrastructure is systematically validated before escalating to logical configuration or application-layer issues.

---

## 1. Layer 1: Physical (Transmission Media & Hardware)
* **Objective:** Verify the hardware integrity, cabling status, and electrical/optical signal reception.
* **Checkpoints:**
  * Physical inspection of UTP/FTP cables (damaged RJ45 connectors, excessive bending).
  * Verification of optical power levels on FTTH links (Rx/Tx) or RF signal levels on coaxial/HFC connections.
  * Status of Modem/ONT/Switch LEDs: Power, PON/LOS, Link/ACT on Ethernet ports.

## 2. Layer 2: Data Link (Synchronization & L2 Switching)
* **Objective:** Ensure direct communication between adjacent interfaces and local link status.
* **Checkpoints:**
  * Modem/ONT synchronization with the ISP central office (OLT/DOCSIS authentication status).
  * Ethernet port negotiation (speed and duplex mode: 10/100/1000 Mbps).
  * Inspection of switch uplink interfaces, VLAN tagging/isolation, and MAC address tables.

## 3. Layer 3: Network (IP Addressing & Routing)
* **Objective:** Confirm proper logical IP assignment and packet transmission inside and outside the local network.
* **Checkpoints:**
  * IP address assignment (DHCP lease validation vs. APIPA address `169.254.x.x`).
  * Local connectivity test to the Default Gateway (`ping <Gateway_IP>`).
  * Verification of the local routing table and outbound traffic to an external public IP (`ping 8.8.8.8`).

## 4. Layer 4: Transport (Packet Loss, Latency & Ports)
* **Objective:** Analyze end-to-end communication quality and specific port reachability.
* **Checkpoints:**
  * Route tracing (`traceroute` / `tracert`) to identify hops with high latency or packet loss.
  * Assessment of ISP WAN links (identifying external latency spikes or link degradation).
  * Testing specific TCP/UDP service ports via terminal utilities (`telnet`, `nc`, `Test-NetConnection`).

## 5. Layers 5, 6 & 7: Session, Presentation & Application (End-User Services)
* **Objective:** Confirm the proper operation of protocols, services, and software consumed by the end-user.
* **Checkpoints:**
  * Domain name resolution using DNS (`nslookup`, `dig`) and clearing stale local DNS cache (`ipconfig /flushdns`).
  * Application protocol validation (HTTP/HTTPS requests in web browsers).
  * Troubleshooting specific services such as SIP/VoIP registrations, VPN clients (IKEv2/IPSec), or SaaS platforms.
