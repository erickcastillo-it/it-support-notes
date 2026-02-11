Packet Tracer – IPv4 Subnetting Design and Implementation (192.168.100.0/24)

Project Summary This lab documents the design and implementation of a fixed-length IPv4 subnetting scheme using the network 192.168.100.0/24. The objective was to divide the address space to support four LAN segments and one WAN link between two routers, ensuring each LAN provides capacity for at least 25 hosts.

The exercise simulates a small enterprise environment where structured address planning, consistent allocation rules, and verification procedures are required.

Network Topology The topology includes:

2 Routers (R1 and R2)

4 LAN segments

1 WAN link between R1 and R2

4 Access Switches (S1–S4)

4 End Devices (PC1–PC4)

Each LAN requires sufficient addressing for:

Router interface

Switch management interface (VLAN 1)

End devices

The WAN link requires two usable IP addresses, one per router interface.

Design Requirements Base Network: 192.168.100.0/24

Constraints:

Each LAN must support a minimum of 25 usable host addresses.

All subnets must be derived from the /24 network.

Subnetting must satisfy both LAN and WAN requirements.

Address allocation must follow a consistent and documented rule set.

Addressing Strategy The subnetting process followed these steps:

Determine the total number of required subnets based on the topology.

Borrow the appropriate number of bits from the host portion.

Validate that the resulting subnet size supports at least 25 usable hosts per LAN.

Calculate:

Total subnets created

Usable hosts per subnet

Binary representation of subnet increments

Build a complete subnet table including:

Subnet address

First usable host

Last usable host

Broadcast address

Subnet Allocation to Topology Subnets were assigned as follows:

Subnet 0 → R1 G0/0 LAN

Subnet 1 → R1 G0/1 LAN

Subnet 2 → R2 G0/0 LAN

Subnet 3 → R2 G0/1 LAN

Subnet 4 → WAN link between R1 and R2

IP Address Allocation Rules To maintain consistency and clarity, the following allocation policy was applied:

Routers

First usable IP addresses assigned to R1 interfaces.

First usable IP addresses assigned to R2 LAN interfaces.

Last usable IP address in the WAN subnet assigned to R2.

Switches

Second usable IP address in each LAN assigned to VLAN 1.

Hosts

Last usable IP address in each LAN assigned to the PC.

This structured allocation approach simplifies troubleshooting and improves documentation clarity.

Implementation The following configurations were completed in Packet Tracer:

Routers

LAN interfaces configured with assigned IP addresses.

WAN interfaces configured and enabled.

Interfaces verified as operational.

Switches

VLAN 1 management interface configured.

Default gateway configured to router LAN interface.

End Devices

IP address configured.

Subnet mask configured.

Default gateway configured.

Routing Dynamic routing (EIGRP) was preconfigured between R1 and R2. Only IP addressing configuration was required.

Verification and Testing Connectivity was validated using the following tests:

Host to default gateway

Inter-LAN communication

End-to-end connectivity across WAN link

Router-to-router reachability

All devices successfully responded to ICMP echo requests according to the addressing plan.

Project Files

subnetting-scenario-192.168.100.0.pka – Packet Tracer configuration file

topology.png – Network topology diagram

addressing-table.md – Completed IP addressing table

subnet-calculations.md – Subnetting calculations and binary breakdown

Technical Skills Demonstrated

Fixed-length subnetting (FLSM)

Binary subnet analysis

Structured IP allocation planning

Router and switch interface configuration

Default gateway configuration

Connectivity verification and troubleshooting methodology

Conclusion This lab reinforces disciplined IPv4 address planning in a multi-LAN and WAN environment. The structured subnet allocation model ensures scalability, clarity in documentation, and simplified troubleshooting, aligning with CCNA-level network design practices.
