# Day 08: Default Gateway and How It Works

## 1. What is a Default Gateway?

A Default Gateway is a device, usually a router, that forwards network traffic from a local network to other networks.

It acts as the exit point from a local network.

**Example:**
- Laptop IP Address: `192.168.0.101`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `192.168.0.1`

Here, `192.168.0.1` is the router's IP address and acts as the Default Gateway.

## 2. Why Do We Need a Default Gateway?

A Default Gateway is needed when a device wants to communicate with another network.

For example:
- Accessing websites on the internet.
- Communicating with a server on another network.
- Sending data outside the local network.

Without a Default Gateway, a device can still communicate with devices on its local subnet, but generally cannot reach other networks.

## 3. Router vs Default Gateway

| Router | Default Gateway |
|---|---|
| A networking device. | The next-hop address used to reach other networks. |
| Connects different networks. | Usually the router's local interface IP. |
| Forwards packets using a routing table. | Provides the route out of the local network. |

## 4. Same Network Communication

Devices on the same subnet can communicate directly without using the Default Gateway.

**Example:**

- Laptop: `192.168.0.101/24`
- PC: `192.168.0.150/24`

Both devices belong to the same network:

`192.168.0.0/24`

They communicate through the local network.

## 5. Different Network Communication

When a laptop wants to communicate with a device on another network, it sends the traffic to its Default Gateway.

**Example:**

- Laptop IP: `192.168.0.101`
- Default Gateway: `192.168.0.1`
- Destination Server: `192.168.2.50`

### Communication Process

1. The laptop checks whether the destination belongs to its local network.
2. It identifies that the destination is on another network.
3. The laptop sends the packet towards its Default Gateway.
4. The router checks its routing table.
5. The router forwards the packet towards the destination network.
6. The packet eventually reaches the destination server.

## 6. Practical Lab – Windows CMD

### Command 1: Check IP Configuration

```cmd
ipconfig
```

Purpose: Displays IPv4 address, subnet mask and Default Gateway.

### Command 2: Display Default Gateway

```cmd
ipconfig | findstr /i "Gateway"
```

Purpose: Filters the output to show lines containing Gateway.

### Command 3: Ping Default Gateway

```cmd
ping 192.168.0.1
```

Purpose: Checks connectivity between the laptop and its Default Gateway.

### Practical Result

- Default Gateway: `192.168.0.1`
- Packets Sent: 4
- Packets Received: 4
- Packet Loss: 0%
- Average Response Time: 5 ms

**Result:** Successfully communicated with the Default Gateway.

## 7. Key Learnings

- A Default Gateway connects a local network to other networks.
- A router commonly acts as a Default Gateway.
- Devices on the same subnet can communicate directly.
- Devices communicating with another network generally use the Default Gateway.
- A router uses its routing table to forward packets.

## 8. Interview Questions

1. What is a Default Gateway?
2. Why do we need a Default Gateway?
3. What is the difference between a router and a Default Gateway?
4. Does communication between two devices on the same subnet require a Default Gateway?
5. What happens when a laptop wants to communicate with a device on another network?

---

**Day 08 Completed: Default Gateway and How It Works**
