# Packet Tracer – IPv4 Subnetting Practice

## Overview
This lab focuses on subnetting an IPv4 network using a fixed-length subnet mask
based on specific host requirements. The scenario simulates a customer network
connected to an ISP.

## Objectives
- Design an IPv4 subnetting scheme
- Configure routers, switches, and end devices
- Verify connectivity using ping
- Troubleshoot addressing issues

## Network Topology
![Network Topology](networking/subnetting/packet-tracer-ipv4-subnetting/ipv4-subnetting-topology.png)

## Requirements
- LAN-A: minimum 50 hosts
- LAN-B: minimum 40 hosts
- At least two unused subnets for future expansion
- Same subnet mask for all networks (no VLSM)

## Address Space
- Customer network: 192.168.0.0/24
- ISP network: Provided by ISP configuration

## Subnetting Decision
After analyzing host and subnet requirements, a /26 subnet mask was selected:

- Subnet mask: 255.255.255.192
- Hosts per subnet: 62
- Number of subnets: 4

This mask satisfies both current and future network needs.

## Implementation
- Routers configured with IP addresses and interfaces enabled
- Switch management interfaces configured
- End devices configured with correct IP, subnet mask, and gateway

## Testing and Verification
- PC-A to default gateway: Successful
- PC-B to default gateway: Successful
- PC-A to PC-B: Successful

## Files included
- `packet-tracer-file.pka`: Packet Tracer lab
- `addressing-table.md`: Addressing details
- `subnet-calculation.md`: Subnetting calculations

## Lessons Learned
This exercise helped reinforce subnetting concepts, address planning,
and the importance of structured network documentation.
