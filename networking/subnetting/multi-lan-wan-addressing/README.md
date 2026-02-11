Packet Tracer – IPv4 Subnetting Scenario (192.168.100.0/24)

Overview This lab focuses on designing and implementing an IPv4 subnetting scheme based on a given /24 network. The objective is to divide the network into multiple subnets to support four LAN segments and one WAN link between two routers.

The exercise simulates a real-world scenario where a company must allocate address space efficiently while meeting minimum host requirements per LAN.

Objectives Part 1: Design an IPv4 Addressing Scheme

Determine the required number of subnets

Calculate borrowed bits

Identify total subnets created

Calculate usable host addresses per subnet

Build a complete subnet table

Document the addressing plan

Part 2: Implement and Verify Connectivity

Assign IP addresses to routers, switches, and PCs

Configure LAN interfaces

Configure switch management interfaces

Configure end devices

Verify connectivity using ping

Network Scenario Base Network: 192.168.100.0/24

Topology Includes:

Router R1 (2 LAN interfaces + 1 WAN interface)

Router R2 (2 LAN interfaces + 1 WAN interface)

Four LAN segments

One WAN link between R1 and R2

Four switches (S1–S4)

Four PCs (PC1–PC4)

Each LAN must support at least 25 host addresses, including:

End devices

Switch management interface

Router interface

The WAN link requires two usable IP addresses (one per router interface).

Part 1 – Addressing Design

Step 1: Subnet the Network Subnet 192.168.100.0/24 to meet the following requirements:

Determine how many subnets are required based on the topology.

Calculate how many bits must be borrowed from the host portion.

Identify how many subnets are created.

Determine how many usable host addresses are available per subnet.

Ensure each LAN supports at least 25 usable hosts.

Avoid borrowing too many bits.

Step 2: Binary Subnet Representation Document the binary values of the first five subnets. Include:

Subnet number

Network address

Bit values for the fourth octet

Step 3: Subnet Mask Calculation Document:

Binary representation of the new subnet mask

Decimal representation of the subnet mask

Prefix length notation

Step 4: Subnet Table Complete a structured subnet table including:

Subnet number

Subnet address

First usable host

Last usable host

Broadcast address

Include only the subnets that are created based on your calculations.

Step 5: Subnet Assignment to Topology Assign subnets as follows:

Subnet 0 → R1 G0/0 LAN

Subnet 1 → R1 G0/1 LAN

Subnet 2 → R2 G0/0 LAN

Subnet 3 → R2 G0/1 LAN

Subnet 4 → WAN link between R1 and R2

Step 6: Addressing Plan Rules Follow these allocation guidelines:

Routers

Assign the first usable IP addresses to R1 (LAN interfaces and WAN interface).

Assign the first usable IP addresses to R2 LAN interfaces.

Assign the last usable IP address of the WAN subnet to R2.

Switches

Assign the second usable IP address in each LAN subnet to the switch VLAN 1 interface.

Hosts

Assign the last usable IP address in each LAN subnet to the PCs.

Document the complete addressing table clearly.

Part 2 – Implementation

Step 1: Configure R1 LAN Interfaces

Assign IP addresses according to the addressing table.

Enable interfaces.

Ensure hosts can reach the default gateway.

Step 2: Configure Switch S3

Assign IP address to VLAN 1.

Configure the default gateway.

Step 3: Configure PC4

Assign IP address.

Configure subnet mask.

Configure default gateway.

Step 4: Verify Connectivity You should be able to:

Ping the default gateway from hosts.

Verify inter-LAN connectivity.

Confirm WAN connectivity between routers.

EIGRP is preconfigured between R1 and R2. Only addressing must be completed.

Deliverables for GitHub Include the following files in this folder:

subnetting-scenario-192.168.100.0.pka – Packet Tracer file

topology.png – Network topology image

addressing-table.md – Completed IP addressing table

subnet-calculations.md – Subnetting calculations and binary analysis

Lessons Reinforced

Fixed-length subnetting design

Binary-to-decimal subnet calculations

Structured IP allocation strategy

LAN vs WAN addressing considerations

Verification and troubleshooting methodology

This lab demonstrates structured network planning and disciplined IP address documentation aligned with CCNA-level subnetting practices.
