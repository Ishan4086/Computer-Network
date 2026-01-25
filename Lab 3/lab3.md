# LAB 3: Design and Implementation of LAN Using Hub, Switch, Bridge, and Router in Cisco Packet Tracer

## Objective:
- To design a network topology using a Hub, a Switch, a Bridge and a Router
- To understand the working of hub, switch, bridge, and router
- To implement and test network connectivity using Cisco Packet Tracer

## Tools Used:
- Cisco Packet Tracer
- Personal Computer (Windows OS)
## Theory:

### Hub:
A hub is a basic networking device that operates at the Physical Layer (Layer 1) of the OSI model. It simply receives data from one port and broadcasts it to all other connected ports without any intelligence.

**Characteristics:**
- Broadcasts data to all connected devices
- Creates a single collision domain
- High chances of data collision
- Low performance and efficiency

### Switch:
A switch works at the Data Link Layer (Layer 2) and forwards data based on MAC addresses. Unlike a hub, it sends data only to the destination device.

**Characteristics:**
- Reduces collisions
- Improves network speed
- Efficient bandwidth utilization
- Maintains a MAC address table

### Bridge:
A bridge is used to connect two or more LAN segments. It also operates at the Data Link Layer and helps in controlling network traffic by filtering frames using MAC addresses.

**Characteristics:**
- Reduces unnecessary data flow
- Divides the collision domain
- Improves network performance

### Router:
A router operates at the Network Layer (Layer 3) of the OSI model. It is responsible for connecting different networks and routing data using IP addresses.

**Characteristics:**
- Routes data between different IP networks
- Breaks broadcast domains
- Provides path selection for packets


## Network Topology Used:
- Star Topology using Hub and Switch
- Extended LAN using a Bridge
- Internet network communication using a Router

## Output:

### I) HUB:

### II) SWITCH:

### III) BRIDGE:

### IV) ROUTER:

### V) REPEATER:

## Discussion:
In this experiment, we studied basic networking devices as hub, switch, bridge, repeater, and router using Cisco Packet Tracer. Hubs and repeaters, operating at the physical layer, simply forward or regenerate signals, while switches and bridges, at the data link layer, forward data based on MAC addresses, improving network efficiency.

Routers, at the network layer, were used to connect different IP networks. By assigning IP addresses to router interfaces and configuring default gateways on PCs, successful communication between networks was achieved. Practical observations included interface activation, gateway setup, and packet flow, reinforcing the differences in how these devices operate in real networks versus simulations.

## Conclusion:
The experiment provided hands-on understanding of networking devices. Hubs and repeaters extend the physical network, switches and bridges manage traffic within a network, and routers enable communication between networks. Overall, it highlighted each device's role, OSI layer operation, and importance in designing efficient networks.