# Final Addressing Table

## Subnet Assignment

| Subnet | Purpose |
|--------|----------|
| 0 | R1 G0/0 LAN |
| 1 | R1 G0/1 LAN |
| 2 | R2 G0/0 LAN |
| 3 | R2 G0/1 LAN |
| 4 | WAN Link |

---

## Router R1

| Interface | IP Address | Mask |
|------------|------------|------|
| G0/0 | 192.168.100.1 | /27 |
| G0/1 | 192.168.100.33 | /27 |
| S0/0/0 | 192.168.100.129 | /27 |

---

## Router R2

| Interface | IP Address | Mask |
|------------|------------|------|
| G0/0 | 192.168.100.65 | /27 |
| G0/1 | 192.168.100.97 | /27 |
| S0/0/0 | 192.168.100.158 | /27 |

---

## Switch Management (VLAN 1)

| Device | IP Address | Default Gateway |
|--------|------------|-----------------|
| S1 | 192.168.100.2 | 192.168.100.1 |
| S2 | 192.168.100.34 | 192.168.100.33 |
| S3 | 192.168.100.66 | 192.168.100.65 |
| S4 | 192.168.100.98 | 192.168.100.97 |

---

## Hosts

| Host | IP Address | Default Gateway |
|------|------------|-----------------|
| PC1 | 192.168.100.30 | 192.168.100.1 |
| PC2 | 192.168.100.62 | 192.168.100.33 |
| PC3 | 192.168.100.94 | 192.168.100.65 |
| PC4 | 192.168.100.126 | 192.168.100.97 |

---

## WAN Link Details

Network: 192.168.100.128/27  
Broadcast: 192.168.100.159  

R1: 192.168.100.129  
R2: 192.168.100.158  

---

## Implementation Notes

- First usable IP → Router interfaces
- Second usable IP → Switch management
- Last usable IP → End devices
- EIGRP configured for dynamic routing
- Full connectivity verified
