# Subnet Calculation – 192.168.100.0/24

## Step 1 – Determine Required Subnets

- LAN R1 G0/0
- LAN R1 G0/1
- LAN R2 G0/0
- LAN R2 G0/1
- WAN Link

Total required subnets: **5**

---

## Step 2 – Borrow Bits

Formula:

2^n ≥ required subnets

2^2 = 4 (insufficient)  
2^3 = 8 (sufficient)

Borrowed bits: **3**

New prefix:

/24 + 3 = **/27**

---

## Step 3 – Host Capacity

Remaining host bits: 5

2^5 − 2 = **30 usable hosts**

Requirement: minimum 25 hosts  
Status: ✔ Requirement satisfied

---

## Step 4 – Subnet Mask

Binary:

11111111.11111111.11111111.11100000

Decimal:

255.255.255.224

---

## Step 5 – Subnet Increment

Block size calculation:

256 − 224 = **32**

Subnets increment by 32 in the last octet.

---

## Generated Subnets

| Subnet | Network Address | First Host | Last Host | Broadcast |
|--------|-----------------|------------|------------|------------|
| 0 | 192.168.100.0/27 | 192.168.100.1 | 192.168.100.30 | 192.168.100.31 |
| 1 | 192.168.100.32/27 | 192.168.100.33 | 192.168.100.62 | 192.168.100.63 |
| 2 | 192.168.100.64/27 | 192.168.100.65 | 192.168.100.94 | 192.168.100.95 |
| 3 | 192.168.100.96/27 | 192.168.100.97 | 192.168.100.126 | 192.168.100.127 |
| 4 | 192.168.100.128/27 | 192.168.100.129 | 192.168.100.158 | 192.168.100.159 |
| 5 | 192.168.100.160/27 | 192.168.100.161 | 192.168.100.190 | 192.168.100.191 |
| 6 | 192.168.100.192/27 | 192.168.100.193 | 192.168.100.222 | 192.168.100.223 |
| 7 | 192.168.100.224/27 | 192.168.100.225 | 192.168.100.254 | 192.168.100.255 |

---

## Design Validation

- 8 subnets created
- 5 subnets used
- 3 subnets reserved for future growth
- Fixed-Length Subnet Masking (FLSM) applied
- No address overlap
