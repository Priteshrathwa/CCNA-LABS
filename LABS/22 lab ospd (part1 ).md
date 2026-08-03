# Network Lab: OSPF Area 0 & Default Route Redistribution

## Topology & Addressing Summary
* **ISPR1 (ISP):** WAN IP `203.0.113.2/30`
* **R1 (ASBR):** WAN `203.0.113.1`, Links to R2/R3. Loopback0: `1.1.1.1/32`
* **R2:** Links to R1/R4. Loopback0: `2.2.2.2/32`
* **R3:** Links to R1/R4. Loopback0: `3.3.3.3/32`
* **R4:** Links to R2/R3, LAN `192.168.4.254`. Loopback0: `4.4.4.4/32`



! ==================== ROUTER R1 ====================
enable
configure terminal
hostname R1

interface GigabitEthernet3/0
 ip address 203.0.113.1 255.255.255.252
 no shutdown
interface GigabitEthernet0/0
 ip address 10.0.12.1 255.255.255.252
 no shutdown
interface FastEthernet1/0
 ip address 10.0.13.1 255.255.255.252
 no shutdown
interface Loopback0
 ip address 1.1.1.1 255.255.255.255
 no shutdown

ip route 0.0.0.0 0.0.0.0 203.0.113.2

router ospf 1
 router-id 1.1.1.1
 network 10.0.12.0 0.0.0.3 area 0
 network 10.0.13.0 0.0.0.3 area 0
 network 1.1.1.1 0.0.0.0 area 0
 passive-interface Loopback0
 default-information originate
exit

! ==================== ROUTER R2 ====================
enable
configure terminal
hostname R2

interface GigabitEthernet0/0
 ip address 10.0.12.2 255.255.255.252
 no shutdown
interface FastEthernet1/0
 ip address 10.0.24.1 255.255.255.252
 no shutdown
interface Loopback0
 ip address 2.2.2.2 255.255.255.255
 no shutdown

router ospf 1
 router-id 2.2.2.2
 network 10.0.12.0 0.0.0.3 area 0
 network 10.0.24.0 0.0.0.3 area 0
 network 2.2.2.2 0.0.0.0 area 0
 passive-interface Loopback0
exit

! ==================== ROUTER R3 ====================
enable
configure terminal
hostname R3

interface FastEthernet1/0
 ip address 10.0.13.2 255.255.255.252
 no shutdown
interface FastEthernet2/0
 ip address 10.0.34.1 255.255.255.252
 no shutdown
interface Loopback0
 ip address 3.3.3.3 255.255.255.255
 no shutdown

router ospf 1
 router-id 3.3.3.3
 network 10.0.13.0 0.0.0.3 area 0
 network 10.0.34.0 0.0.0.3 area 0
 network 3.3.3.3 0.0.0.0 area 0
 passive-interface Loopback0
exit

! ==================== ROUTER R4 ====================
enable
configure terminal
hostname R4

interface FastEthernet1/0
 ip address 10.0.24.2 255.255.255.252
 no shutdown
interface FastEthernet2/0
 ip address 10.0.34.2 255.255.255.252
 no shutdown
interface GigabitEthernet0/0
 ip address 192.168.4.254 255.255.255.0
 no shutdown
interface Loopback0
 ip address 4.4.4.4 255.255.255.255
 no shutdown

router ospf 1
 router-id 4.4.4.4
 network 10.0.24.0 0.0.0.3 area 0
 network 10.0.34.0 0.0.0.3 area 0
 network 192.168.4.0 0.0.0.255 area 0
 network 4.4.4.4 0.0.0.0 area 0
 passive-interface GigabitEthernet0/0
 passive-interface Loopback0
exit
