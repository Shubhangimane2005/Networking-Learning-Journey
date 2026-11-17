# Day 7: Subnet Mask and CIDR Notation

## Overview

On Day 7 of my Computer Networking Learning Journey, I learned about Subnet Masks, Network Identification, and CIDR Notation.

I understood how a subnet mask helps devices identify whether another IP address belongs to the same local network or a different network.

## Topics Covered

### 1. What is a Subnet Mask?

A subnet mask is a 32-bit number used with an IPv4 address to identify the network portion and host portion of an IP address.

Example:

- IP Address: `192.168.0.101`
- Subnet Mask: `255.255.255.0`

In this example:
- Network portion: `192.168.0`
- Host portion: `101`

### 2. Why Do We Use a Subnet Mask?

A subnet mask helps a device:
- Identify its local network.
- Determine whether a destination device belongs to the same network.
- Determine whether data needs to be sent to another network through a router.

### 3. Network Identification Practical

I practised identifying network addresses using IP addresses and subnet masks.

| Device | IP Address | Subnet Mask | Network Address |
|---|---|---|---|
| PC 1 | 192.168.1.10 | 255.255.255.0 | 192.168.1.0 |
| PC 2 | 192.168.1.20 | 255.255.255.0 | 192.168.1.0 |
| PC 3 | 192.168.2.10 | 255.255.255.0 | 192.168.2.0 |

**Observations:**
- PC 1 and PC 2 belong to the same network.
- PC 3 belongs to a different network.
- All three PCs can use the same subnet mask while belonging to different networks.

### 4. What is CIDR?

CIDR stands for Classless Inter-Domain Routing.

CIDR notation represents the network prefix length using slash notation.

Example:

`192.168.1.10/24`

Here, `/24` means that 24 bits are used for the network portion.

### 5. Common Subnet Masks and CIDR

| Subnet Mask | CIDR |
|---|---|
| 255.0.0.0 | /8 |
| 255.255.0.0 | /16 |
| 255.255.255.0 | /24 |
| 255.255.255.128 | /25 |
| 255.255.255.192 | /26 |
| 255.255.255.224 | /27 |

## Practical Exercises

I used my Windows Command Prompt to check my network configuration.

**Command:**

```cmd
ipconfig
```

I identified:
- IPv4 Address: `192.168.0.101`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.0.1`

I also practised identifying network addresses using different IP addresses and subnet masks.

## Key Learnings

- Understood the purpose of a subnet mask.
- Learned the difference between network and host portions.
- Practised identifying network addresses.
- Understood why different networks can use the same subnet mask.
- Learned CIDR notation and common subnet mask formats.

## CMD Commands Practised

### 1. ipconfig
Displays the basic IP configuration of network adapters, including IPv4 address, subnet mask and default gateway.

### 2. ipconfig | findstr /i "IPv4 Subnet"
Filters the output to display only IPv4 address and subnet information.

## Conclusion

Day 7 helped me understand how subnet masks divide IP addresses into network and host portions. I also learned how CIDR notation represents subnet masks in a shorter format.

Next: Day 8 – Default Gateway and How It Works.
