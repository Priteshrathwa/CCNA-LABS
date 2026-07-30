# Cisco CCNA Networking Portfolio and Lab Repository

Welcome to my hands-on networking portfolio. This public repository tracks my ongoing progress through the Cisco CCNA curriculum, hosting active network topologies engineered and simulated within Cisco Packet Tracer. Each lab focuses on mastering the Cisco IOS Command Line Interface (CLI), infrastructure protocols, and core troubleshooting workflows required for enterprise System and Network Administration.

---

## Core Technical Competencies Demonstrated

* **Layer 3 Routing:** Static Routing Configuration, Route Troubleshooting, Metric/Administrative Distance logic.
* **IP Architecture:** Variable Length Subnet Masking (VLSM), IPv4 Schema Design, Network Address Management.
* **Layer 2 Switching:** Virtual LANs (VLANs), 802.1Q Trunking Encapsulation, Broadcast Domain Isolation, STP Concepts.
* **Device Hardening:** Base Cisco IOS Security, Console/VTY Line Protection, Management IP Configuration.

---

## Lab Index and Project Structure

| Lab ID | Lab Name | Core Technologies and Protocols Tested |
| :--- | :--- | :--- |
| **01** | Packet Tracer Introduction | Workspace navigation, workspace simulation vs real-time modes. |
| **02** | Connecting Devices | Cable selection (Straight-through vs Crossover), interface verification. |
| **03** | OSI Model | Protocol Data Unit (PDU) encapsulation/decapsulation analysis. |
| **04** | Basic Device Security | Enable passwords, secret encryption, login banners, console lines. |
| **05** | Ethernet LAN Switching | MAC Address table populating logic, frame forwarding behaviors. |
| **06** | IPv4 Addresses | Layer 3 host addressing, default gateways, network vs host bits. |
| **07** | Interface Configuration | Speed/duplex negotiation, interface descriptions, bringing links UP. |
| **08** | Configuring Static Routes | Next-hop routing, exit interface assignments, recursive lookups. |
| **09** | Troubleshooting Static Routes | Resolving asymmetric routing paths, interface drops, and metrics. |
| **10** | Life of a Packet | End-to-end trace of ARP resolution and Layer 2/3 header alterations. |
| **11** | VLSM Subnetting | Efficient IP assignment, subnetting down to custom host constraints. |
| **12** | VLANs (Part 1) | Access port provisioning, data isolation, multi-switch environment tests. |
| **13** | VLANs (Part 2) | 802.1Q Native VLAN configs, Trunk port mapping across distribution links. |
| **14** | Multilayer Switching | Inter-VLAN routing via SVIs, routed ports, and `ip routing` enablement. |
| **16** | Analyzing STP | Root bridge election logic, STP port roles (Root, Designated, Blocked), and BPDU analysis. |
| **17** | Configuring Spanning Tree | STP bridge priority manipulation, PortFast, and BPDU Guard provisioning. |
| **18** | Rapid STP | 802.1w RSTP transition mechanisms, edge port configurations, and convergence optimization. |
| **19** | EtherChannel | Link aggregation using LACP (802.3ad), PAgP, and manual bundling on trunk links. |
| **20** | Floating Static Routes | Administrative Distance (AD) tuning, primary/backup path failover, and redundancy. |
---

## Featured Verification Commands Used

Every topology in this repository has been verified using production-level verification commands:
* `show ip route` — To validate Layer 3 routing tables.
* `show interfaces trunk` — To verify active 802.1Q encapsulation and allowed VLAN lists.
* `show vlan brief` — To check administrative database access mappings.
* `ping` / `traceroute` — To verify end-to-end data plane reachability.

---
*Note: This repository is actively updated as I progress through advanced routing, scaling protocols, and infrastructure security modules. All network files (`.pkt`) are built using Cisco Packet Tracer and are ready for deployment and validation testing.*
