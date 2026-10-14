<img width="868" height="452" alt="image" src="https://github.com/user-attachments/assets/6b5e63ff-b0c5-4225-82ee-998ed62c7534" />


# Routing in Computer Networks

## 1. What is Routing?

**Definition:** Routing is the process of selecting the best path for forwarding data packets from a source to a destination across a network.

**বাংলা ব্যাখ্যা:** Routing হলো Source থেকে Destination-এ Data Packet পাঠানোর জন্য উপযুক্ত পথ নির্বাচন করার প্রক্রিয়া।

**Remember:** Routing = Selecting the path for data packets.

### Example

When a computer sends data to another network, routers determine the appropriate path to reach the destination.

`Source → Router → Router → Destination`

---

## 2. How Does Routing Work?

Routing works through the following steps:

1. The source sends a data packet.
2. The router checks the destination IP address.
3. The router looks up its routing table.
4. It selects the appropriate route based on the routing information.
5. The packet is forwarded to the next hop.
6. The process continues until the packet reaches its destination.

---

## 3. Types of Routing

Routing is mainly divided into two types.

### A. Static Routing

**Definition:** Static routing is a routing method in which routes are manually configured by a network administrator.

**Advantages:**
- Simple for small networks.
- No routing protocol updates are required.
- Low routing overhead.

**Disadvantages:**
- Routes must be updated manually.
- Difficult to manage in large networks.
- Does not automatically adapt to network failures.

**Example:** A manually configured route on a router.

### B. Dynamic Routing

**Definition:** Dynamic routing is a routing method in which routers learn and update routes automatically using routing protocols.

**Advantages:**
- Automatically learns routes.
- Can adapt to network topology changes.
- Suitable for large networks.

**Disadvantages:**
- Requires additional CPU and memory.
- Uses bandwidth to exchange routing information.
- More complex to configure and troubleshoot.

**Examples:** RIP, OSPF, EIGRP, and BGP.

---

## 4. Important Routing Protocols

# Routing Protocol in Computer Networks

## 1. What is a Routing Protocol?

**Definition:** A routing protocol is a set of rules that routers use to exchange routing information and determine the best path for forwarding data packets.

**বাংলা ব্যাখ্যা:** Routing Protocol হলো কিছু নিয়ম, যার মাধ্যমে Router-গুলো একে অপরের সঙ্গে Network-এর তথ্য আদান-প্রদান করে এবং ডেটা পাঠানোর জন্য উপযুক্ত পথ নির্ধারণ করে।

**Remember:**

`Routing Protocol = Route শেখা + Routing Information আদান-প্রদান`

**Examples:** RIP, OSPF, EIGRP, IS-IS, BGP.

---

## 2. How Does a Routing Protocol Work?

### *Basic Diagram*

```text
       Routing Information
   ┌────────────────────────┐
   │                        │
   ▼                        │
Router A  ◄──────────►  Router B
   │                        │
   ▼                        ▼
Routing Table          Routing Table
```

Router-গুলো Routing Information আদান-প্রদান করে এবং Routing Table তৈরি বা আপডেট করে।

### Working Steps

1. A router learns about its directly connected networks.
2. It exchanges routing information with other routers using a routing protocol.
3. It learns about different route networks.
4. It compares available routes using routing metrics and protocol rules.
5. It selects the preferred route and updates its routing information.
6. When a packet arrives, the router uses its routing table to forward the packet toward its destination.

**বাংলা ব্যাখ্যা:**

1. Router প্রথমে তার সরাসরি সংযুক্ত Network সম্পর্কে জানে।
2. Routing Protocol ব্যবহার করে অন্য Router-এর কাছ থেকে Route-এর তথ্য পায়।
3. বিভিন্ন Route সম্পর্কে জানতে পারে।
4. Metric ও Protocol-এর নিয়ম অনুযায়ী Route নির্বাচন করে।
5. Routing Table আপডেট করে।
6. Data Packet এলে Routing Table ব্যবহার করে Packet Forward করে।

---

## 3. Types of Routing Protocol

Routing Protocol-এর প্রধান তিনটি ধরন হলো:

### A. Distance Vector Routing

Definition: Distance Vector Routing is a method where routers learn routes from their neighboring routers and choose a path based on distance.

বাংলা: Distance Vector Routing হলো এমন একটি পদ্ধতি, যেখানে Router তার পাশের Router থেকে পথের তথ্য শিখে এবং দূরত্ব অনুযায়ী পথ নির্বাচন করে।

**Examples:**

- RIP (Routing Information Protocol)
- IGRP (Interior Gateway Routing Protocol — legacy protocol)

**Key Points:**

- Shares routing information with neighboring routers.
- RIP uses hop count as its metric.সহজ বাংলা ব্যাখ্যা: RIP গন্তব্যে পৌঁছাতে কতটি Router পার হতে হবে, তা গণনা করে পথ নির্বাচন করে। এই গণনাকে Hop Count বলে।
-  distance-vector routing uses the Bellman-Ford method.
- May experience slow convergence and routing loops.

### B. Link State Routing

**Definition:** In Link State Routing, routers build a map of the network topology and calculate the shortest paths using link-state information.

**বাংলা ব্যাখ্যা:** Router-গুলো Network-এর Link ও Cost সম্পর্কে তথ্য সংগ্রহ করে Network Topology তৈরি করে এবং Shortest Path নির্ধারণ করে।

**Examples:**

- OSPF (Open Shortest Path First)
- IS-IS (Intermediate System to Intermediate System)

**Key Points:**

- Builds a network topology database.
- Uses link-state information.
- OSPF uses Dijkstra's Shortest Path First (SPF) algorithm.
- Generally provides fast convergence.

### C. Path Vector Routing

**Definition:** Path Vector Routing uses path information to select routes between Autonomous Systems (ASes).

**বাংলা ব্যাখ্যা:** বিভিন্ন Autonomous System-এর মধ্যে গন্তব্যে পৌঁছানোর জন্য কোন কোন AS-এর মধ্য দিয়ে যেতে হবে, সেই Path-এর তথ্য ব্যবহার করে Route নির্বাচন করা হয়।

**Example:**

- BGP (Border Gateway Protocol)

**Key Points:**

- Used for inter-domain routing.
- Advertises network reachability and AS-path information.
- Uses path attributes and routing policies to select routes.
- Helps prevent AS-level routing loops through AS-PATH checks.

---

## 4. Important Routing Protocols for Job Exams

| Protocol | Full Form                                  | Type                     | Algorithm / Method           |
| -------- | ------------------------------------------ | ------------------------ | ---------------------------- |
| RIP      | Routing Information Protocol               | Distance Vector          | Bellman-Ford method          |
| OSPF     | Open Shortest Path First                   | Link State               | Dijkstra's SPF               |
| EIGRP    | Enhanced Interior Gateway Routing Protocol | Advanced Distance Vector | DUAL                         |
| IS-IS    | Intermediate System to Intermediate System | Link State               | SPF                          |
| BGP      | Border Gateway Protocol                    | Path Vector              | Path attributes and policies |

### Important Facts

- **RIP:** Uses hop count as its routing metric. Maximum usable hop count is 15; 16 means unreachable.
- **OSPF:** Uses Cost as its routing metric and calculates shortest paths using Dijkstra's algorithm.
- **EIGRP:** Uses DUAL (Diffusing Update Algorithm) to determine loop-free routes.
- **IS-IS:** Uses link-state information and SPF calculations.
- **BGP:** Exchanges routing information between Autonomous Systems and uses path attributes and policies to select routes.

---

## 5. IGP vs EGP

### What is IGP?

**IGP (Interior Gateway Protocol)** is used for routing within a single Autonomous System.

**Examples:** RIP, OSPF, EIGRP, IS-IS.

### What is EGP?

**EGP (Exterior Gateway Protocol)** refers to routing between Autonomous Systems. BGP is the protocol used for Internet-scale inter-domain routing.

| Feature   | IGP                       | EGP                       |
| --------- | ------------------------- | ------------------------- |
| Full Form | Interior Gateway Protocol | Exterior Gateway Protocol |
| Scope     | Within an AS              | Between ASes              |
| Purpose   | Internal routing          | Inter-domain routing      |
| Examples  | RIP, OSPF, EIGRP, IS-IS   | BGP                       |

**Note:** EGP is also the name of a historical routing protocol. Modern Internet inter-domain routing uses BGP.

---

## 6. Routing Protocol vs Routed Protocol

| Feature  | Routing Protocol                      | Routed Protocol                                       |
| -------- | ------------------------------------- | ----------------------------------------------------- |
| Purpose  | Exchanges routing information         | Carries data packets across networks                  |
| Function | Helps routers learn and select routes | Provides network-layer addressing and packet delivery |
| Examples | RIP, OSPF, EIGRP, BGP                 | IPv4, IPv6                                            |

**বাংলা ব্যাখ্যা:**

- **Routing Protocol:** Router-কে Route শিখতে ও নির্বাচন করতে সাহায্য করে।
- **Routed Protocol:** যে Network-Layer Protocol-এর Packet Router Forward করতে পারে।

---

## 7. Quick Revision for Job Exams

| Question                                      | Answer                                                       |
| --------------------------------------------- | ------------------------------------------------------------ |
| What is a routing protocol?                   | Rules for exchanging routing information and learning routes |
| Which protocol uses Distance Vector routing?  | RIP                                                          |
| Which protocol uses Link State routing?       | OSPF                                                         |
| Which protocol uses Dijkstra's algorithm?     | OSPF                                                         |
| Which protocol uses DUAL?                     | EIGRP                                                        |
| Which protocol uses Path Vector routing?      | BGP                                                          |
| What is RIP's maximum usable hop count?       | 15                                                           |
| What does RIP hop count 16 mean?              | Unreachable                                                  |
| Which protocol is commonly used between ASes? | BGP                                                          |
| Which protocols are examples of IGP?          | RIP, OSPF, EIGRP, IS-IS                                      |
| What does OSPF use as a metric?               | Cost                                                         |
| What is the full form of SPF?                 | Shortest Path First                                          |
| What is the full form of DUAL?                | Diffusing Update Algorithm                                   |

---

## 8. Easy Memory Tricks

Remember the following:

- **RIP → Distance Vector → Hop Count**
- **OSPF → Link State → Dijkstra → Cost**
- **EIGRP → Advanced Distance Vector → DUAL**
- **IS-IS → Link State → SPF**
- **BGP → Path Vector → Inter-AS Routing**
- **IGP → Within an Autonomous System**
- **BGP → Between Autonomous Systems**

### One-Line Summary

A routing protocol enables routers to exchange routing information, learn available routes, and select preferred paths for forwarding data packets.

**বাংলায়:** Routing Protocol হলো Router-গুলোর মধ্যে Route-এর তথ্য আদান-প্রদান করে গন্তব্যে ডেটা পাঠানোর উপযুক্ত পথ নির্ধারণ করার নিয়ম।


| Protocol | Full Form | Type | Algorithm / Method |
|---|---|---|---|
| RIP | Routing Information Protocol | Distance Vector | Bellman-Ford |
| OSPF | Open Shortest Path First | Link State | Dijkstra's SPF |
| EIGRP | Enhanced Interior Gateway Routing Protocol | Advanced Distance Vector | DUAL |
| IS-IS | Intermediate System to Intermediate System | Link State | SPF |
| BGP | Border Gateway Protocol | Path Vector | Path attributes and policies |

### Important Facts

- **RIP:** Uses hop count as its routing metric. Maximum usable hop count is 15; 16 means unreachable.
- **OSPF:** Uses cost as its routing metric and calculates shortest paths using Dijkstra's algorithm.
- **EIGRP:** Uses the DUAL algorithm to determine loop-free routes.
- **BGP:** Exchanges routing information between Autonomous Systems (ASes).

---

## 5. Routing vs Forwarding

| Routing | Forwarding |
|---|---|
| Selects a suitable path to the destination. | Sends a packet to the next hop along the selected path. |
| Uses routing information to build or update routing tables. | Uses the forwarding table to forward packets. |
| Determines where packets should go. | Moves packets toward their destination. |

**Remember:**
- Routing = Path selection.
- Forwarding = Packet movement.

---

## 6. Important Routing Terms

### Router
A networking device that forwards packets between different networks.

### Routing Table
A table containing information about destination networks and the routes used to reach them.

### Routing Protocol
A set of rules used by routers to exchange routing information.

### Next Hop
The next router or gateway to which a packet should be forwarded.

### Metric
A value used to compare routes and help select a preferred path.

**Examples of metrics:** Hop count, cost, and delay.

### Default Route
A route used when no more specific matching route is available.

IPv4 default route: `0.0.0.0/0`

IPv6 default route: `::/0`

---

## 7. IGP vs EGP

| IGP | EGP |
|---|---|
| Interior Gateway Protocol | Exterior Gateway Protocol |
| Used within an Autonomous System. | Used between Autonomous Systems. |
| Examples: RIP, OSPF, EIGRP, IS-IS | Example: BGP |

**Autonomous System (AS):** A group of IP networks and routers managed under a common routing administration and policy.

---

## 8. Routing vs Routed Protocol

| Routing Protocol | Routed Protocol |
|---|---|
| Helps routers exchange routing information and determine routes. | Carries data packets that can be routed across networks. |
| Examples: RIP, OSPF, BGP | Examples: IPv4, IPv6 |

---

## 9. Advantages of Routing

- Enables communication between different networks.
- Helps select suitable paths for data packets.
- Dynamic routing can adapt to topology changes.
- Supports large and complex networks.
- Provides alternative paths when available and properly configured.

## 10. Disadvantages of Routing

- Dynamic routing requires processing power and memory.
- Routing protocols may consume network bandwidth.
- Configuration errors can cause routing problems.
- Large networks can be difficult to troubleshoot.

---

## 11. Job Exam Quick Revision

| Question | Answer |
|---|---|
| What is routing? | Selecting a path for data packets. |
| What is static routing? | Manually configured routing. |
| What is dynamic routing? | Routing that learns routes using protocols. |
| Which protocol uses Bellman-Ford? | RIP (classic distance-vector method). |
| Which protocol uses Dijkstra's algorithm? | OSPF. |
| Which protocol uses DUAL? | EIGRP. |
| Which protocol is used between ASes? | BGP. |
| What is a routing table? | A table containing routing information. |
| What is a next hop? | The next router or gateway on the path. |
| What is a routing metric? | A value used to compare routes. |
| What is the IPv4 default route? | `0.0.0.0/0` |
| What is the IPv6 default route? | `::/0` |

---

## 12. Final Summary

- **Routing:** Selecting the path.
- **Forwarding:** Sending the packet to the next hop.
- **Static Routing:** Routes are configured manually.
- **Dynamic Routing:** Routes are learned using routing protocols.
- **RIP:** Distance Vector.
- **OSPF:** Link State.
- **EIGRP:** Advanced Distance Vector.
- **BGP:** Path Vector.
- **Routing Table:** Stores route information.

**One-line definition for exams:**

Routing is the process of selecting an appropriate path for forwarding data packets from a source to a destination across a network.

<img width="768" height="413" alt="image" src="https://github.com/user-attachments/assets/08406414-449b-4a91-803c-7eb549db7069" />

