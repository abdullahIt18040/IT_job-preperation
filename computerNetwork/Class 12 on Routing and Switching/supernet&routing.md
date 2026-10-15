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

<img width="892" height="472" alt="image" src="https://github.com/user-attachments/assets/782dd57e-02db-4312-8a38-94f7f87bcfaf" />


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

**Definition:**Link State Routing is a method where routers create a map of the network and find the shortest path to the destination. using link-state information.

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

# Unicast and Multicast Routing

## 1. Unicast Routing

**Definition:** Unicast Routing sends data from one sender to one receiver.

**বাংলা ব্যাখ্যা:** একজন Sender থেকে একজন Receiver-এর কাছে ডেটা পাঠানোকে Unicast Routing বলে।

**Example:**

- Sending an email to one person.
- Sending data to a specific computer.

**Key Points:**
- One-to-One communication.
- Data is sent to a single receiver.
- Uses a Unicast IP address.

**Remember:** Unicast = One-to-One.

---

## 2. Multicast Routing

**Definition:** Multicast Routing sends data from one sender to a specific group of receivers.

**বাংলা ব্যাখ্যা:** একজন Sender থেকে নির্দিষ্ট একদল Receiver-এর কাছে ডেটা পাঠানোকে Multicast Routing বলে।

**Example:**
- Live video streaming to a specific group.
- Online classes for a group of students.

**Key Points:**
- One-to-Many communication (specific group).
- Data is delivered to group members.
- Uses a Multicast IP address.
- Helps reduce unnecessary duplicate data transmission.

**Remember:** Multicast = One-to-Specific Group.

---

## 3. Unicast vs. Multicast Routing

| Feature | Unicast | Multicast |
|---|---|---|
| Communication | One-to-One | One-to-Specific Group |
| Sender | One | One |
| Receiver | One | Multiple group members |
| IP Address | Unicast IP | Multicast IP |
| Example | Email to one person | Streaming to a group |

---

## 4. Bonus: Broadcast Routing

**Definition:** Broadcast Routing sends data to all devices in a network where broadcast is supported.

**বাংলা ব্যাখ্যা:** একটি নেটওয়ার্কের সব ডিভাইসের কাছে ডেটা পাঠানোকে Broadcast বলে।

**Remember:** Broadcast = One-to-All.

---

## 5. Job Exam Quick Revision

- **Unicast:** One-to-One
- **Multicast:** One-to-Specific Group
- **Broadcast:** One-to-All
- **Unicast IP:** Identifies a single interface for unicast delivery.
- **Multicast IPv4 Range:** `224.0.0.0` – `239.255.255.255`

when send data from source router to distination router we are used follow two routing protocal .

1. Distance routing (used bellman-ford algoritm) .
   <img width="831" height="374" alt="image" src="https://github.com/user-attachments/assets/f26f47ac-5f4d-469a-8d50-1e375c3dad0c" />
  <img width="1066" height="622" alt="image" src="https://github.com/user-attachments/assets/0a979d87-437c-4fe3-8f05-3e89e30c3121" />

   
3. link- state routing (used Dijkstra algorithm) .
   
## 4. Important  Distance routing and  link- state routing   differmnece  for Job Exams
# Count-to-Infinity Problem

## 1. Definition

**Definition:** When a network fails, routers keep increasing the distance to the destination because of incorrect routing information. This is called the Count-to-Infinity Problem.
**বাংলা ব্যাখ্যা:** কোনো নেটওয়ার্ক নষ্ট হয়ে গেলে Router-গুলো ভুল তথ্যের কারণে গন্তব্যের দূরত্ব বারবার বাড়াতে থাকে। একে Count-to-Infinity Problem বলে।

## 2. Example

Suppose Router A, B, and C are connected:

`A ---- B ---- C`

- Network X is connected to Router A.
- Network X becomes unreachable.
- Router B and C mistakenly believe that the other router can still reach X.
- So, they keep increasing the distance.

Example:

`2 → 3 → 4 → 5 → ... → Infinity`

## 3. How to Resolve Count-to-Infinity

### 1. Split Horizon
A router does not send a route back to the router from which it learned that route.

**বাংলা:** যে Router থেকে Route শিখেছে, তাকে সেই Route আবার জানায় না।

### 2. Route Poisoning
A router marks a failed route as unreachable by setting its metric to infinity.

**বাংলা:** কোনো Route নষ্ট হলে তার Metric Infinity করে দেয়।




### 5. Maximum Hop Count
RIP uses 16 as infinity. A destination with a hop count of 16 is considered unreachable.

**বাংলা:** RIP-এ Hop Count 16 হলে গন্তব্য Unreachable ধরা হয়।

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
# 7. Distance Vector vs. Link State Routing

## Definition

**1. Distance Vector Routing:**

Each router learns routes from its neighboring routers and selects a route based on distance.

**বাংলা ব্যাখ্যা:** প্রতিটি Router তার পাশের Router থেকে Route-এর তথ্য শেখে এবং দূরত্ব অনুযায়ী Route নির্বাচন করে।

**2. Link State Routing:**

Each router builds a map of the network and uses it to find the shortest path.

**বাংলা ব্যাখ্যা:** প্রতিটি Router নেটওয়ার্কের একটি Map তৈরি করে এবং গন্তব্যে যাওয়ার সবচেয়ে ছোট পথ খুঁজে বের করে।

---

## Comparative Analysis

| Feature | Distance Vector Routing | Link State Routing |
|---|---|---|
| **1. Working Principle** | Learns routes from neighboring routers. | Builds a map of the network. |
| **বাংলা ব্যাখ্যা** | পাশের Router থেকে Route শেখে। | নেটওয়ার্কের Map তৈরি করে। |
| **2. Information Exchanged** | Exchanges routing table information with neighbors. | Shares link-state information about network links. |
| **বাংলা ব্যাখ্যা** | Neighbor Router-দের সঙ্গে Routing Table-এর তথ্য আদান-প্রদান করে। | নেটওয়ার্কের Link-এর অবস্থা ও Cost-এর তথ্য ছড়িয়ে দেয়। |
| **3. Routing Algorithm** | Bellman-Ford algorithm. | Dijkstra's algorithm. |
| **বাংলা ব্যাখ্যা** | Bellman-Ford Algorithm ব্যবহার করে Route হিসাব করে। | Dijkstra Algorithm ব্যবহার করে Shortest Path বের করে। |
| **4. Convergence Speed** | Generally slow. | Generally fast. |
| **বাংলা ব্যাখ্যা** | নেটওয়ার্ক পরিবর্তনের পর সঠিক Route পেতে সাধারণত বেশি সময় লাগে। | সাধারণত দ্রুত নতুন Route নির্ধারণ করে। |
| **5. Information Maintained** | Maintains destination, distance, and next hop. | Maintains a network topology database and routing table. |
| **বাংলা ব্যাখ্যা** | গন্তব্য, দূরত্ব এবং পরবর্তী Router-এর তথ্য রাখে। | নেটওয়ার্কের Map-এর তথ্য ও Routing Table রাখে। |
| **6. Bandwidth Requirement** | Periodic updates may consume bandwidth. | Link-state updates also consume bandwidth. |
| **বাংলা ব্যাখ্যা** | নিয়মিত Update পাঠাতে Bandwidth লাগে। | Link-এর তথ্য ছড়িয়ে দিতেও Bandwidth লাগে। |
| **7. CPU and Memory** | Generally requires fewer resources. | Generally requires more CPU and memory. |
| **বাংলা ব্যাখ্যা** | সাধারণত কম CPU ও Memory লাগে। | সাধারণত বেশি CPU ও Memory লাগে। |
| **8. Routing Problem** | May suffer from the count-to-infinity problem. | Temporary routing loops may occur during network changes. |
| **বাংলা ব্যাখ্যা** | Count-to-Infinity সমস্যা হতে পারে, যেখানে ভুল তথ্যের কারণে Distance বাড়তে থাকে। | নেটওয়ার্ক পরিবর্তনের সময় সাময়িক Routing Loop হতে পারে। |
| **9. Advantages** | Simple to configure and suitable for small networks. | Fast convergence and better knowledge of network topology. |
| **বাংলা ব্যাখ্যা** | সহজে Configure করা যায় এবং ছোট নেটওয়ার্কের জন্য উপযোগী। | দ্রুত Route নির্ধারণ করে এবং নেটওয়ার্ক সম্পর্কে ভালো ধারণা রাখে। |
| **10. Disadvantages** | Slow convergence and possible routing loops. | More complex and requires more resources. |
| **বাংলা ব্যাখ্যা** | ধীরে Converge করতে পারে এবং Routing Loop হতে পারে। | Configure করা কঠিন এবং বেশি Resource লাগে। |
| **11. Examples** | RIP | OSPF, IS-IS |
| **বাংলা ব্যাখ্যা** | RIP হলো Distance Vector Protocol। | OSPF ও IS-IS হলো Link State Protocol। |

---

## Conclusion

**English:** Distance Vector Routing is simple and suitable for small networks, whereas Link State Routing provides faster convergence and is suitable for larger networks.

**বাংলা ব্যাখ্যা:** Distance Vector Routing সহজ এবং ছোট নেটওয়ার্কের জন্য উপযোগী। অন্যদিকে, Link State Routing সাধারণত দ্রুত Convergence করে এবং বড় নেটওয়ার্কের জন্য বেশি উপযোগী।

---

## Important Terms

**1. Convergence:** The time required for routers to update their routing information after a network change.

বাংলা: নেটওয়ার্কে পরিবর্তন হলে Router-গুলোর Routing Information সঠিক হতে যে সময় লাগে।

**2. Routing Loop:** Data keeps moving between routers without reaching its destination.

বাংলা: ডেটা গন্তব্যে না পৌঁছে বারবার Router-গুলোর মধ্যে ঘুরতে থাকে।

**3. Count-to-Infinity:** Routers keep increasing the distance to an unreachable destination because of incorrect routing information.

বাংলা: ভুল Routing Information-এর কারণে Router-গুলো অচল গন্তব্যের Distance বারবার বাড়াতে থাকে।

**4. Bandwidth:** The capacity of a network to transfer data over a period of time.

বাংলা: নেটওয়ার্কের মাধ্যমে নির্দিষ্ট সময়ে ডেটা স্থানান্তরের ক্ষমতা।

---

## Job Exam Quick Revision

- **Distance Vector** = Neighbor + Bellman-Ford + RIP
- **Link State** = Network Map + Dijkstra + OSPF
- **Distance Vector** = Generally slower convergence
- **Link State** = Generally faster convergence
- **Distance Vector** = Count-to-Infinity Problem

**মনে রাখার কৌশল:** Distance Vector প্রতিবেশীর কাছ থেকে Route শেখে, আর Link State নেটওয়ার্কের Map তৈরি করে Route বের করে।



<img width="768" height="413" alt="image" src="https://github.com/user-attachments/assets/08406414-449b-4a91-803c-7eb549db7069" />

