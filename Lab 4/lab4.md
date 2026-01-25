# LAB 4: Subnetting and Supernetting using Cisco Packet Tracer

## Objective:
- To design and simulate a subnetting and supernetting using Cisco Packet Tracer
- To verify communication between computers using ping

## Software Required:
- Cisco Packet Tracer
- Windows PC/Laptop
## Theory:

### 1. Subnetting:
Subnetting is a method used in computer networks to break down a large network into smaller, more manageable sections called subnets. This helps make better use of IP addresses, reduces traffic congestion, and makes network management and security easier. By taking some bits from the host portion of an IP address, you can create multiple logical networks from a single network. Companies often use subnetting to separate different departments or areas while staying within the same main network.

### 2. Supernetting:
Supernetting is basically the reverse of subnetting where it merges several smaller networks into a bigger one. This helps cut down the number of entries in routing tables and makes routing simpler. It works by taking bits from the network part of an IP address so that a group of consecutive networks can be treated as a single route. Large networks and the Internet often use supernetting to make routing more efficient and scalable.

## Network Design:

### Subnetting

**Calculation:**
- Base network: 192.168.1.0/24
- Required number of subnets: 4
- Number of IP address per subnet: 64 (Block size)
- /26 (Borrowed 2 bits: 2^2 = 4 subnets)
- Subnet Mask: 255.255.255.192

**Subnet Table:**

| Subnet | Network Address | Broadcast Address | 1st Usable | Last Usable |
|--------|---|---|---|---|
| 1 | 192.168.1.0/26 | 192.168.1.63/26 | 192.168.1.1/26 | 192.168.1.62/26 |
| 2 | 192.168.1.64/26 | 192.168.1.127/26 | 192.168.1.65/26 | 192.168.1.126/26 |
| 3 | 192.168.1.128/26 | 192.168.1.191/26 | 192.168.1.129/26 | 192.168.1.190/26 |
| 4 | 192.168.1.192/26 | 192.168.1.255/26 | 192.168.1.193/26 | 192.168.1.254/26 |
## Network Topology:

### Subnetting:
A topology was created using Router 0 to connect two subnets: 192.168.1.0/26 and 192.168.1.64/26. Switch 0 connects PC 0, PC 1, and PC 2 in the first subnet, while Switch 1 connects PC 3, PC 4, and PC 5 in the second subnet. Both switches are connected to the router interfaces.

### Supernetting:
The topology consists of one router, one switch, and four PCs (PC 6 – PC 9). All PCs connect to the switch, which is connected to the router.

### Subnetting Configuration Table

| Device | IPv4 | Subnet Mask | Default Gateway |
|--------|---|---|---|
| Router 0 (FastEthernet 0/0) | 192.168.1.1 | 255.255.255.192 | N/A |
| Router 0 (FastEthernet 0/1) | 192.168.1.65 | 255.255.255.192 | N/A |
| PC 0 (Subnet 1) | 192.168.1.2 | 255.255.255.192 | 192.168.1.1 |
| PC 1 (Subnet 1) | 192.168.1.3 | 255.255.255.192 | 192.168.1.1 |
| PC 2 (Subnet 1) | 192.168.1.4 | 255.255.255.192 | 192.168.1.1 |
| PC 3 (Subnet 2) | 192.168.1.66 | 255.255.255.192 | 192.168.1.65 |
| PC 4 (Subnet 2) | 192.168.1.67 | 255.255.255.192 | 192.168.1.65 |
| PC 5 (Subnet 2) | 192.168.1.68 | 255.255.255.192 | 192.168.1.65 |

**Test Cases:**
- PC 0 to PC 4
- PC 3 to PC 1

### Supernetting Configuration Table

| Device | IPv4 | Subnet Mask | Default Gateway |
|--------|---|---|---|
| Router 0 (FastEthernet 0/0) | 192.168.0.1 | 255.255.252.0 | N/A |
| PC 6 | 192.168.0.10 | 255.255.252.0 | 192.168.0.1 |
| PC 7 | 192.168.1.10 | 255.255.252.0 | 192.168.0.1 |
| PC 8 | 192.168.2.10 | 255.255.252.0 | 192.168.0.1 |
| PC 9 | 192.168.3.10 | 255.255.252.0 | 192.168.0.1 |

**Test Cases:**
- PC 6 to Router
- PC 6 to PC 7, 8, 9
## Discussion:
In this lab, we carried out subnetting and supernetting using Cisco Packet Tracer to get hands-on experience with IP address allocation and routing. Subnetting allowed us to split a large network into smaller segments, which made better use of IP addresses and reduced network congestion. On the other hand, supernetting combined several networks into a single larger network, helping to simplify routing and decrease the number of entries in routing tables. All configurations were tested within the simulator, and successful packet delivery confirmed that the concepts were applied correctly.

## Conclusion:
This lab provided practical insight into managing IP addresses and improving routing efficiency. It reinforced the theoretical ideas of subnetting and supernetting, showing how thoughtful network design can enhance performance and scalability. Overall, the experiment offered a solid foundation for designing and managing efficient computer networks.