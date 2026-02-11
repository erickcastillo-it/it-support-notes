Packet Tracer – IPv4 Subnetting Scenario
Overview

This lab focuses on subnetting an IPv4 network using a fixed-length subnet mask derived from the base network 192.168.100.0/24. The scenario simulates a small enterprise network composed of four LAN segments interconnected through a WAN link between two routers.

Objectives

Design an IPv4 subnetting scheme

Allocate subnets to four LANs and one WAN link

Configure routers, switches, and end devices

Verify end-to-end connectivity using ping

Apply structured IP allocation rules

Network Topology




The topology includes:

R1 with two LAN interfaces and one WAN interface

R2 with two LAN interfaces and one WAN interface

Four LAN segments (S1–S4 with PCs)

One WAN link between R1 and R2

Requirements

Base network: 192.168.100.0/24

Four LANs requiring a minimum of 25 usable host addresses each

One WAN subnet requiring two usable IP addresses

Consistent IP allocation strategy across all subnets

Address Space

Enterprise network: 192.168.100.0/24

All subnets derived from the /24 base network

Subnetting Decision

After analyzing subnet and host requirements, the /24 network was subdivided into equal-length subnets that:

Provide sufficient usable host addresses per LAN

Support a dedicated subnet for the WAN link

Maintain structured and predictable address allocation

The selected subnet mask satisfies the minimum host requirement per LAN while maintaining efficient address utilization.

Subnet Allocation

Subnet 0 → R1 G0/0 LAN

Subnet 1 → R1 G0/1 LAN

Subnet 2 → R2 G0/0 LAN

Subnet 3 → R2 G0/1 LAN

Subnet 4 → WAN link between R1 and R2

Addressing Rules
Routers

First usable IP addresses assigned to R1 interfaces

First usable IP addresses assigned to R2 LAN interfaces

Last usable IP address in the WAN subnet assigned to R2

Switches

Second usable IP address in each LAN assigned to VLAN 1

Hosts

Last usable IP address in each LAN assigned to the PC

Implementation

Routers configured with assigned IP addresses and interfaces enabled

Switch management interfaces configured with IP address and default gateway

End devices configured with correct IP address, subnet mask, and default gateway

Dynamic routing (EIGRP) preconfigured between routers

Testing and Verification

Host to default gateway: Successful

Inter-LAN communication: Successful

WAN connectivity between routers: Successful

End-to-end connectivity across the network: Successful

Files Included

subnetting-scenario-192.168.100.0.pka – Packet Tracer lab file

topology.png – Network topology diagram

addressing-table.md – IP addressing details

subnet-calculations.md – Subnetting calculations and logic

Lessons Learned

This lab reinforced IPv4 subnetting concepts, structured address planning, and the importance of consistent IP allocation rules when deploying and troubleshooting multi-LAN enterprise networks.
