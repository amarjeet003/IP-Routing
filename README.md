# Default Routing Configuration on Cisco Routers

## Description
This project demonstrates how to configure **default routing** between two networks in Cisco Packet Tracer. Each network is connected through a router, with default routes set to enable communication between devices in different subnets. The setup also involves subnetting for efficient IP address utilization.

## Topology Overview
- **Router 0** connected to Network 1 (Yellow)
- **Router 1** connected to Network 2 (Blue)
- Default route configured on each router pointing to the other router's interface
- Switches connecting PCs within each network

## IP Addressing
### Router 0
- **Gig0/0**: 10.0.0.1 /29
- **Gig0/1**: 10.0.0.9 /29
- Default Route: `ip route 0.0.0.0 0.0.0.0 10.0.0.10`

### Router 1
- **Gig0/0**: 10.0.0.17 /29
- **Gig0/1**: 10.0.0.10 /29
- Default Route: `ip route 0.0.0.0 0.0.0.0 10.0.0.9`

## Commands Used
enable
configure terminal
interface gig0/0
no shutdown
ip address <IP> <Subnet Mask>
exit
interface gig0/1
no shutdown
ip address <IP> <Subnet Mask>
exit
ip route 0.0.0.0 0.0.0.0 <Next Hop IP>

## Outcome
After configuration, all PCs in both networks can communicate through the routers using the default routes.
