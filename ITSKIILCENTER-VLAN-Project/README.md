### Project Overview
This project involved designing and implementing a small enterprise network for a fictional organization called ITSKIILCENTER using Cisco Packet Tracer.
The objective was to create a segmented network environment using VLANs, configure IP addressing, implement inter-VLAN routing, and verify communication between departments.

## Network Topology

The network consists of:
- 1 Cisco 2901 Router
- 1 Cisco Switch
- 6 End Devices (PCs)

Departments were separated using VLAN technology.
## VLAN Structure

| VLAN ID | Department |
|----------|------------|
| 10       |  Administration 
| 20       |  Training 
| 30       |  IT Support 

## Technologies Used
- Cisco Packet Tracer
- VLANs
- Trunking
- Router-on-a-Stick
- Static IP Addressing
- Inter-VLAN Routing

## Configuration Tasks
- Switch Configuration
- Router Configuration
- End Device Configuration
  
## Troubleshooting
During implementation, devices in different VLANs were unable to communicate. 
After investigation, the issue was traced to the switch port connected to the router being configured as an access port instead of a trunk port.

The problem was resolved by:
- Configuring the switch port as a trunk
- Allowing VLAN traffic to traverse the link
- Verifying router subinterface configuration

This successfully restored inter-VLAN communication.

## Verification

Connectivity was tested using:
- Ping tests
- show vlan brief
- show ip interface brief

Successful communication was verified:
- Within VLANs
- Between VLANs
- Between devices and their gateways

## Skills Demonstrated
- Network Design
- VLAN Configuration
- Trunking
- Inter-VLAN Routing
- Router-on-a-Stick
- Troubleshooting
- Network Documentation

## Outcome
The project successfully demonstrated enterprise network segmentation and secure communication between departments using VLAN technology and inter-VLAN routing.
