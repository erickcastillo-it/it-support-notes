# IPv4 Subnetting Calculation

## Network Requirements

- Base network: 192.168.0.0/24
- LAN-A: minimum 50 hosts
- LAN-B: minimum 40 hosts
- Future expansion: at least 2 additional subnets
- Same subnet mask for all networks (no VLSM)

## Subnet Mask Selection

The largest subnet requires at least 50 host addresses.

To support 50 hosts:
- Required host bits: 6
- 2^6 = 64 addresses per subnet
- Usable hosts per subnet: 62

Selected subnet mask:
- CIDR: /26
- Subnet mask: 255.255.255.192

This mask provides:
- 4 subnets
- 62 usable hosts per subnet

## Subnet Breakdown

| Subnet | Network Address | First Host | Last Host | Broadcast |
|------|-----------------|------------|-----------|-----------|
| LAN-A | 192.168.0.0/26 | 192.168.0.1 | 192.168.0.62 | 192.168.0.63 |
| LAN-B | 192.168.0.64/26 | 192.168.0.65 | 192.168.0.126 | 192.168.0.127 |
| Future-1 | 192.168.0.128/26 | 192.168.0.129 | 192.168.0.190 | 192.168.0.191 |
| Future-2 | 192.168.0.192/26 | 192.168.0.193 | 192.168.0.254 | 192.168.0.255 |

## Address Assignment Logic

- Router interfaces use the first usable IP address
- Switch management interfaces use the second usable IP address
- End devices use the last usable IP address
- Default gateway is set to the router interface IP

## Validation

Connectivity was verified using ICMP (ping):
- PC-A to default gateway
- PC-B to default gateway
- PC-A to PC-B

All tests were successful.
