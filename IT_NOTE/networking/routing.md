# IP Addressing and OSPF Routing

## Question
Explain how IP addressing and routing are used to exchange and deliver packets across networks using OSPF at the Network Layer.

## Answer

IP addressing and routing work together at the **Network Layer (Layer 3)** to deliver packets from a source network to a destination network.

### Working Process

1. **IP Addressing:** Each device is assigned a unique logical IP address to identify the source and destination.

2. **Packet Creation:** The sender creates an IP packet containing the source and destination IP addresses.

3. **Default Gateway:** If the destination belongs to another network, the packet is sent to the default gateway (router).

4. **OSPF Routing:** OSPF (Open Shortest Path First), a Link State Routing Protocol, exchanges routing information between routers.

5. **Shortest Path Calculation:** OSPF uses Dijkstra's Shortest Path First (SPF) algorithm to calculate the best route based on link cost.

6. **Packet Forwarding:** Routers examine the destination IP address and forward packets to the next-hop router using their routing tables.

7. **Packet Delivery:** The packet reaches the destination network and is delivered to the destination device.

## Example

PC-A → Router R1 → Router R2 → Router R3 → PC-B

## Important Points for Job Exams

| Topic | Answer |
|---|---|
| Network Layer | Layer 3 |
| IP Address | Logical Address |
| OSPF Type | Link State Routing |
| OSPF Algorithm | Dijkstra's SPF |
| OSPF Protocol Number | 89 |
| OSPF Function | Selects the best route |
| Router Function | Forwards packets between networks |

## Conclusion

IP addressing identifies the source and destination, OSPF determines the best route, and routers forward packets to deliver data across different networks.
