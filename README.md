# Cisco CCNA Networking Portfolio and Lab Repository

Welcome to my hands-on networking portfolio. This public repository tracks my ongoing progress through the Cisco CCNA curriculum, hosting active network topologies engineered and simulated within Cisco Packet Tracer. Each lab focuses on mastering the Cisco IOS Command Line Interface (CLI), infrastructure protocols, and core troubleshooting workflows required for enterprise System and Network Administration.

---

## Core Technical Competencies Demonstrated

* **Dynamic & Static Routing:** OSPF (Single & Multi-area), EIGRP basics, Floating Static Routes, Administrative Distance tuning, and IPv6 routing.
* **Layer 2 Infrastructure:** VLANs, 802.1Q Trunks, Voice VLANs, EtherChannel (LACP/PAgP), Rapid STP (802.1w), and STP/HSRP alignment.
* **Network Services & Redundancy:** First Hop Redundancy (HSRP), DHCP Server/Relay, DNS, NTP, SNMP, Syslog, and NAT/PAT (Static & Dynamic).
* **Security & Device Hardening:** Standard & Extended ACLs, Port Security, DHCP Snooping, Dynamic ARP Inspection (DAI), and SSH.
* **Enterprise Connectivity & Wireless:** GRE Site-to-Site Tunnels, QoS traffic marking/queuing, and Wireless LAN Controller (WLC) deployments.

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
| **21** | EIGRP Configuration | Autonomous system numbers, network advertisements, wildcard masks, and passive interfaces. |
| **22** | OSPF (Part 1) | Single-area OSPFv2 setup, router ID selection, and adjacency formation. |
| **23** | OSPF (Part 2) | DR/BDR election tuning via priority, passive interfaces, and default-route injection. |
| **24** | OSPF (Part 3) | Multi-area OSPF, interface cost manipulation, and hello/dead timer tuning. |
| **25** | HSRP Configuration | First Hop Redundancy Protocol (FHRP), virtual IPs, priority, and preemption. |
| **26** | IPv6 Configuration (Part 1) | Global unicast addressing, link-local addresses, and SLAAC/EUI-64 generation. |
| **27** | IPv6 Configuration (Part 2) | IPv6 neighbor discovery (NDP), Solicited-Node multicast, and router advertisements. |
| **28** | IPv6 Static Routes | Next-hop IPv6 static routes, link-local interface routing, and default routes (`::/0`). |
| **29** | Standard ACLs | Numbered/named standard access control lists placed near destinations for traffic filtering. |
| **30** | Extended ACLs | Protocol, source/destination IP, and Layer 4 port filtering placed close to the traffic source. |
| **31** | CDP & LLDP | Layer 2 discovery protocols, device neighbor discovery, and TLV verification. |
| **32** | NTP | Network Time Protocol client/server synchronization, stratum levels, and timezone settings. |
| **33** | DNS | Domain Name System resolution configuration and Cisco IOS local host-to-IP mappings. |
| **34** | DHCP | Cisco IOS DHCP server pools, excluded addresses, and DHCP Relay Agent (`ip helper-address`). |
| **35** | SNMP | Simple Network Management Protocol agent configuration, community strings (RO/RW), and traps. |
| **36** | Syslog | Centralized log collection, logging severity levels, and buffer management. |
| **37** | SSH | Remote management hardening, RSA key-pair generation, VTY transport limits, and local auth. |
| **38** | FTP & TFTP | Remote file system backups, Cisco IOS image management, and configuration loading. |
| **39** | Static NAT | One-to-one inside local to inside global translation for external-facing servers. |
| **40** | Dynamic NAT & PAT | Many-to-many dynamic pools and Port Address Translation (NAT Overload) via ACLs. |
| **41** | Voice VLANs | Auxiliary voice VLAN encapsulation, CoS trust boundaries, and IP phone connectivity. |
| **42** | QoS | Quality of Service classification, DSCP markings, policing, shaping, and priority queuing. |
| **43** | Port Security | MAC address learning (Static, Dynamic, Sticky), maximum host limits, and violation modes. |
| **44** | DHCP Snooping | Layer 2 defense against rogue DHCP servers, trusted vs untrusted ports, and binding database. |
| **45** | Dynamic ARP Inspection | Mitigating ARP spoofing/poisoning by cross-referencing the DHCP snooping binding table. |
| **46** | STP & HSRP Synchronization | Aligning STP Root Bridge with HSRP Active Router roles to prevent suboptimal transit paths. |
| **47** | GRE Tunnels | Generic Routing Encapsulation point-to-point tunnels over simulated IP backbones. |
| **48** | Wireless LANs | Centralized WLC deployment, lightweight AP (LAP) associations, and WPA2-Enterprise SSIDs. |

---

## Featured Verification Commands Used

Every topology in this repository has been verified using production-level verification commands:
* `show ip route` / `show ipv6 route` — Validate Layer 3 dynamic and static routing tables.
* `show ip ospf neighbor` / `show ip eigrp neighbors` — Confirm dynamic routing adjacency states.
* `show standby brief` — Verify HSRP state, priority, and virtual IP failover.
* `show interfaces trunk` — Check active 802.1Q encapsulation and allowed VLAN lists.
* `show ip dhcp snooping binding` / `show ip arp inspection` — Audit Layer 2 security defenses.
* `show ip nat translations` — Inspect active inside/outside address mapping translations.
* `ping` / `traceroute` — Verify end-to-end data plane reachability across hops.

---
