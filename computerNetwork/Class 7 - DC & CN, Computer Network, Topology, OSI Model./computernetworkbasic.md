<img width="872" height="571" alt="image" src="https://github.com/user-attachments/assets/c9fbfc15-0331-4669-b17c-49775cc264bb" />

# Computer Network

## What is a Computer Network?

A **Computer Network** is a group of two or more computers or devices connected together to **communicate and share data, resources, and services**.

### Simple Definition

> A computer network allows devices to communicate and exchange data with each other.

### Examples

* Internet
* Wi-Fi Network
* Office Network
* Mobile Network
* Home Network

---

## How Does a Computer Network Work?

When one device wants to send data to another device, the data travels through a network using different networking devices and protocols.

### Basic Process

```text
Sender
   ↓
Data
   ↓
Network
   ↓
Router / Switch
   ↓
Receiver
```

### Example

Suppose **Computer A** wants to send a message to **Computer B**.

```text
Computer A
    ↓
Data is divided into packets
    ↓
Packets are sent through the network
    ↓
Router/Switch forwards the packets
    ↓
Computer B receives the packets
    ↓
Packets are reassembled
    ↓
Original Data
```

---

## Main Components of a Computer Network

### 1. Sender

The device that sends data.

Examples:

```text
Computer
Mobile
Server
```

### 2. Receiver

The device that receives data.

Examples:

```text
Computer
Mobile
Server
```

### 3. Transmission Medium

The path through which data travels.

Examples:

```text
Ethernet Cable
Fiber Optic Cable
Wi-Fi
Radio Waves
```

### 4. Networking Devices

Devices that help data travel through the network.

Examples:

* **Switch** – Connects devices within a local network.
* **Router** – Connects different networks and forwards packets.
* **Access Point** – Provides wireless network connectivity.
* **Modem** – Connects a network to an Internet service.

---

## How Data Travels?

Data is usually divided into small units called **Packets** before transmission.

```text
Original Data
      ↓
   Packets
      ↓
Network
      ↓
Destination
      ↓
Packets combined
      ↓
Original Data
```

Each packet can contain information such as:

* Source address
* Destination address
* Data
* Control information

---

## Protocols

A **Protocol** is a set of rules that devices follow to communicate with each other.

Common network protocols:

| Protocol | Purpose                               |
| -------- | ------------------------------------- |
| HTTP     | Web communication                     |
| HTTPS    | Secure web communication              |
| TCP      | Reliable data delivery                |
| IP       | Addressing and routing                |
| DNS      | Converts domain names to IP addresses |
| DHCP     | Automatically assigns IP addresses    |
| FTP      | File transfer                         |

---

## Simple Example: Opening a Website

Suppose we enter:

```text
https://example.com
```

The basic process is:

```text
User
 ↓
Browser
 ↓
DNS
 ↓
Find Server IP Address
 ↓
TCP/IP Communication
 ↓
Router
 ↓
Internet
 ↓
Web Server
 ↓
Response
 ↓
Browser
 ↓
Web Page
```

### In Simple Words

1. User enters a website address.
2. **DNS** finds the server's IP address.
3. Data is divided into packets.
4. Packets travel through routers and other network devices.
5. The destination server receives the packets.
6. The server processes the request.
7. The server sends a response back.
8. The browser displays the webpage.

---

## Why Do We Need Computer Networks?

Computer networks are used for:

* Data sharing
* File sharing
* Resource sharing
* Internet access
* Communication
* Remote access
* Server-client communication
* Cloud services

---

## Key Points

```text
Computer Network
       ↓
Connects multiple devices
       ↓
Allows communication
       ↓
Data is divided into packets
       ↓
Packets travel through network
       ↓
Receiver receives and processes data
```

### One-Line Definition

> **A computer network is a collection of connected devices that communicate and share data and resources using networking protocols.**

<img width="1173" height="524" alt="image" src="https://github.com/user-attachments/assets/ad907f01-7aa4-4370-8d54-3748161ba4c2" />
<img width="1030" height="539" alt="image" src="https://github.com/user-attachments/assets/b1c4fd5c-293c-4d10-a545-ef7af75e3ab0" />
# Types of Computer Network

A **computer network** can be classified based on the **geographical area it covers**.

## 1. PAN — Personal Area Network

* Covers a **very small area**.
* Usually used around one person.
  <img width="1007" height="498" alt="image" src="https://github.com/user-attachments/assets/84e69ce6-b777-4f1e-98d8-0830bbbbb808" />

* **Example:** Bluetooth connection between a phone and earbuds.

## 2. LAN — Local Area Network

* Covers a **small area** such as a room, building, office, or school.
* **Example:** Office Wi-Fi network.
<img width="1048" height="519" alt="image" src="https://github.com/user-attachments/assets/1248df78-a164-4840-a1a9-fc65f1b06eca" />

## 3. MAN — Metropolitan Area Network

* Covers a **city or large town**.
* **Example:** Network connecting offices across a city.
<img width="1053" height="603" alt="image" src="https://github.com/user-attachments/assets/cc51b158-2680-48a9-9ee5-98a40eeb81c6" />

## 4. WAN — Wide Area Network
  area: it cover whole world.
* Covers a **large geographical area**, such as countries or continents.
  device used: all device ( router, switch,hub etc),firewall .

* **Example:** Internet.
<img width="1141" height="589" alt="image" src="https://github.com/user-attachments/assets/77c1ea7c-869c-4cf4-be2a-630642338b6c" />

## Easy Way to Remember

```text
PAN → Person
LAN → Building
MAN → City
WAN → Country / World
```

### Short Definition

> **Network types are categories of networks based on the geographical area they cover.**
# Types of Network Based on Privacy

Based on **privacy and accessibility**, networks can be divided into three types:

## 1. Intranet

* A **private network** used within an organization.
* Only **authorized employees/users** can access it.
* Used for sharing internal information and resources.
* **Example:** A company's internal website.

> **Intranet = Private network for internal users**

---

## 2. Extranet

* A **private network** that allows access to **authorized external users**.
* Used to communicate with customers, suppliers, partners, etc.
* **Example:** A company portal accessed by its suppliers.

> **Extranet = Private network with limited external access**

---

## 3. Internet

* A **global public network** that connects computers and networks worldwide.
* Anyone can access its services through an Internet connection.
* **Example:** Google, YouTube, websites, email.

> **Internet = Global public network**

### Easy Way to Remember

```text
Intranet → Internal Users
Extranet → Internal + Authorized External Users
Internet → Everyone / Public
```

### Quick Comparison

| Network      | Access                    | Scope                   |
| ------------ | ------------------------- | ----------------------- |
| **Intranet** | Internal users            | Organization            |
| **Extranet** | Authorized external users | Organization + Partners |
| **Internet** | Public                    | Worldwide               |

<img width="1131" height="483" alt="image" src="https://github.com/user-attachments/assets/5978b8d6-3cf8-4c0c-8da1-6c8062ce5070" />

<img width="1012" height="236" alt="image" src="https://github.com/user-attachments/assets/de60fa4d-9ba2-4b67-9823-c8b2a4a109dd" />

# Network Topology

**Network topology** is the **arrangement or layout of devices and connections in a network**.

## Types of Network Topology

### 1. Bus Topology

There is main one cable (backbon) . All devices are connected to **one main cable (backbone) by the wire **.

<img width="1084" height="563" alt="image" src="https://github.com/user-attachments/assets/107b78db-3929-4fc9-868c-b30d4e11ed70" />


**Features:**

* Uses one main backbone cable.
* All devices share the same communication medium.
* Requires terminators at both ends.

**Number of Cables:**

* **1 main cable** + short connecting cables for devices.

**Advantages:**

* Simple to install.
* Low cost.
* Uses less cable.

**Disadvantages:**

* If the main cable fails, the whole network can fail.
* Performance decreases when many devices are connected.

* Difficult to troubleshoot.

---

### 2. Star Topology

All devices are connected to a **central device**, such as a switch or hub.

```text
       PC
        |
PC ── Switch ── PC
        |
       PC
```
<img width="1055" height="560" alt="image" src="https://github.com/user-attachments/assets/4398739d-c46a-408a-b218-cc5cdd8a7408" />

**Features:**

* Has a central device.
* Each device has a separate connection to the central device.
* Commonly used in modern LANs.

**Number of Cables:**

* **n devices = n cables** to the central device.
* 
* * **n devices = n-1  cables** all over the Topology .

**Advantages:**

* Easy to install and manage.
* Easy to find faults.
* Failure of one cable affects only one device.
* Easy to add or remove devices.

**Disadvantages:**

* Requires more cable than Bus topology.
* If the central device fails, the entire network stops.
* Higher installation cost.

---

### 3. Ring Topology

In Ring Topology, each device is directly connected to two neighboring devices through point-to-point links, forming a closed ring.
or In Ring Topology, each device has a point-to-point connection with two neighboring devices

```text
PC ── PC
|      |
PC ── PC

PC1 ↔ PC2 → Point-to-point
PC2 ↔ PC3 → Point-to-point
PC3 ↔ PC4 → Point-to-point
PC4 ↔ PC1 → Point-to-point
```

**Features:**

* Devices form a closed loop.
* Data travels around the ring.
* Can use token-based communication.

**Number of Cables:**

* For **n devices → n connections/cable links**.

**Advantages:**

* Provides orderly data transmission.
* Less chance of data collision.
* Performs consistently under heavy traffic.

**Disadvantages:**

* Failure of one connection can affect the network.
* Difficult to troubleshoot.
* Adding or removing a device can affect the network.
<img width="1036" height="602" alt="image" src="https://github.com/user-attachments/assets/c76c0b4c-1348-4ef7-b5a8-9348b3d061b8" />

---



<img width="986" height="505" alt="image" src="https://github.com/user-attachments/assets/79b99e83-7ba2-478f-ae06-12731c69f81f" />
<img width="1020" height="524" alt="image" src="https://github.com/user-attachments/assets/e47bc05c-9789-467d-afd3-fd4ad57822d2" />
<img width="969" height="456" alt="image" src="https://github.com/user-attachments/assets/1be805c7-72b4-421a-ad46-cef28c95e304" />
<img width="1001" height="522" alt="image" src="https://github.com/user-attachments/assets/c8cace40-ee58-4e56-b07b-56e07b22de89" />
<img width="1011" height="525" alt="image" src="https://github.com/user-attachments/assets/2ba1fd8e-85ff-4fa4-94de-d7e5a4b97905" />

<img width="995" height="467" alt="image" src="https://github.com/user-attachments/assets/2af1db60-e7bd-459d-962f-1cc945a7c4bb" />

<img width="1102" height="611" alt="image" src="https://github.com/user-attachments/assets/a951d5d2-f588-4746-87f1-6ceb9678b700" />
<img width="1091" height="456" alt="image" src="https://github.com/user-attachments/assets/04a0ff1e-1fef-4ada-9375-9b4b2859f513" />
<img width="1078" height="470" alt="image" src="https://github.com/user-attachments/assets/96a3cdb4-8e76-41a4-9cff-4a294382c64f" />
<img width="1088" height="592" alt="image" src="https://github.com/user-attachments/assets/6ffd7121-9009-4a1e-aca7-a578521d4820" />

# Network Topology Example — 100 PCs in 2 Floors

## Problem

Suppose a building has **100 PCs**:

* **1st Floor → 50 PCs**
* **2nd Floor → 50 PCs**

Which network topology is suitable?

## Answer

**Tree Topology** is a suitable choice.

### Network Structure

```text
                    Core Switch
                   /           \
                  /             \
        1st Floor Switch     2nd Floor Switch
             /   |   \           /   |   \
            PC   PC   PC  ...   PC   PC   PC
             \   |   /           \   |   /
              50 PCs              50 PCs
```

### Why Tree Topology?

1. **Easy Management**
   Each floor can be managed separately.

2. **Scalable**
   More PCs or floors can be added easily.

3. **Fault Isolation**
   A problem on one floor may not affect the other floor.

4. **Good Performance**
   Each floor has its own switch to handle local traffic.

5. **Suitable for Large Networks**
   Tree topology is suitable for networks with many devices and multiple levels/floors.

## Simple Structure

```text
Core Switch
    │
    ├── Switch 1 → 50 PCs (1st Floor)
    │
    └── Switch 2 → 50 PCs (2nd Floor)
```

## Exam Point

> **For 100 PCs distributed across two floors, Tree Topology is a suitable choice because it provides a hierarchical structure with separate switches for each floor.**

### Important Note

In real-world networks, this structure is often called an **Extended Star / Hierarchical Star topology**, because each floor uses a **Star topology** and the switches are connected hierarchically.
# Network Topology — Scenario Based Problems

## Problem 1 — Small Office

### Scenario

একটি ছোট অফিসে **10টি PC** আছে। সব PC একটি central device-এর সাথে connected হবে।

### Question

Which topology is suitable?

### Answer

**Star Topology**

### Why?

কারণ সব PC একটি **central switch**-এর সাথে connected থাকবে এবং network manage করা সহজ হবে।

```text
        PC
         |
PC ─── Switch ─── PC
         |
        PC
```

---

## Problem 2 — 100 PCs in Two Floors

### Scenario

একটি building-এ:

* 1st Floor → 50 PCs
* 2nd Floor → 50 PCs

### Question

Which topology is suitable?

### Answer

**Tree Topology**

### Why?

প্রতিটি floor-এর জন্য আলাদা switch ব্যবহার করে hierarchical network তৈরি করা যায়।

```text
             Core Switch
             /         \
        Switch 1      Switch 2
        50 PCs        50 PCs
```

---

## Problem 3 — Maximum Reliability

### Scenario

একটি network-এ **maximum reliability** দরকার। একটি connection নষ্ট হলেও communication বন্ধ হওয়া যাবে না।

### Question

Which topology is best?

### Answer

**Mesh Topology**

### Why?

Mesh topology-তে multiple paths থাকে। একটি link নষ্ট হলেও অন্য path দিয়ে data যেতে পারে।

> **Maximum reliability → Mesh**

---

## Problem 4 — Minimum Cable Cost

### Scenario

একটি network তৈরি করতে হবে যেখানে **cable cost যত কম সম্ভব** রাখতে হবে।

### Question

Which topology is suitable?

### Answer

**Bus Topology**

### Why?

Bus topology-তে একটি main backbone cable ব্যবহার করা হয়।

> **Low cable cost → Bus**

---

## Problem 5 — Easy Fault Detection

### Scenario

একটি office network-এ এমন topology দরকার যেখানে কোনো একটি PC-এর connection নষ্ট হলে সহজে সমস্যা খুঁজে বের করা যাবে।

### Question

Which topology is suitable?

### Answer

**Star Topology**

### Why?

প্রতিটি PC-এর আলাদা connection থাকে। তাই কোন cable বা PC-এর connection-এ সমস্যা হয়েছে সহজে identify করা যায়।

> **Easy troubleshooting → Star**

---

## Problem 6 — Circular Network

### Scenario

প্রতিটি computer তার পাশের দুইটি computer-এর সাথে connected এবং পুরো network একটি closed circle তৈরি করে।

### Question

Which topology is this?

### Answer

**Ring Topology**

```text
PC1 ── PC2
 |       |
PC4 ── PC3
```

> **Closed circle → Ring**

---

## Problem 7 — One Main Cable

### Scenario

একটি network-এ সব computers একটি **single main cable**-এর সাথে connected।

### Question

Which topology is used?

### Answer

**Bus Topology**

> **Single backbone cable → Bus**

---

## Problem 8 — Central Device

### Scenario

একটি network-এ সব computers একটি **central switch**-এর সাথে connected।

### Question

Which topology is used?

### Answer

**Star Topology**

> **Central device → Star**

---

## Problem 9 — Every Device Connected to Every Other Device

### Scenario

একটি network-এ প্রতিটি device অন্য প্রতিটি device-এর সাথে directly connected।

### Question

Which topology is used?

### Answer

**Full Mesh Topology**

For `n` devices:

```text
Number of links = n(n - 1) / 2
```

Example:

```text
4 devices
= 4(4-1)/2
= 6 links
```

---

## Problem 10 — Multiple Buildings

### Scenario

একটি university campus-এ:

* Building A → 3 floors
* Building B → 4 floors
* Building C → 5 floors

প্রতিটি building-এর ভিতরে আলাদা switches এবং buildingগুলোর মধ্যে higher-level connection থাকবে।

### Question

Which topology is suitable?

### Answer

**Tree / Hierarchical Topology**

### Why?

Network-টি hierarchical structure-এ organize করা যায়।

```text
                 Core
              /    |    \
             A     B     C
            /|\   /|\   /|\
         Floors Floors Floors
```

---

## Problem 11 — Different Topologies Combined

### Scenario

একটি network-এর একটি অংশে Star topology এবং অন্য অংশে Ring topology ব্যবহার করা হয়েছে।

### Question

Which topology is this?

### Answer

**Hybrid Topology**

> **Combination of different topologies → Hybrid**

---

## Problem 12 — One Link Failure

### Scenario

একটি network-এ একটি cable নষ্ট হলেও alternative path দিয়ে data transmission চালু রাখতে হবে।

### Question

Which topology is best?

### Answer

**Mesh Topology**

### Why?

Mesh topology provides **multiple paths** between devices.

---

# Quick Exam Tricks

| Requirement                   | Suitable Topology |
| ----------------------------- | ----------------- |
| Central device                | **Star**          |
| Single main cable             | **Bus**           |
| Circular connection           | **Ring**          |
| Maximum reliability           | **Mesh**          |
| Low cable cost                | **Bus**           |
| Easy troubleshooting          | **Star**          |
| Large hierarchical network    | **Tree**          |
| Multiple floors/buildings     | **Tree**          |
| Different topologies combined | **Hybrid**        |
| Multiple alternative paths    | **Mesh**          |
<img width="698" height="535" alt="image" src="https://github.com/user-attachments/assets/1fd7a6f7-3924-4060-b902-aa78015890b3" />

<img width="982" height="403" alt="image" src="https://github.com/user-attachments/assets/368d3692-e242-45d7-a892-09528d08c448" />
<img width="993" height="517" alt="image" src="https://github.com/user-attachments/assets/48877cad-b5bd-4e4d-a2ac-cfd39f56e5d1" />
<img width="729" height="567" alt="image" src="https://github.com/user-attachments/assets/aabd3f05-6e19-4e10-b0ea-cbc475c56cfb" />
<img width="733" height="601" alt="image" src="https://github.com/user-attachments/assets/b4dfe0c7-3e95-40c5-9318-b33dcbeab0ac" />
<img width="855" height="541" alt="image" src="https://github.com/user-attachments/assets/a3e1e47e-c397-411f-820b-8ec7f8aee874" />
<img width="852" height="564" alt="image" src="https://github.com/user-attachments/assets/9b9f90c4-8a29-4fb4-bc1c-5f71bce5f785" />

<img width="894" height="603" alt="image" src="https://github.com/user-attachments/assets/1638f51e-29a8-4e9b-9888-40f945f6cc12" />

<img width="995" height="576" alt="image" src="https://github.com/user-attachments/assets/ec6c446c-4b2c-4929-a83c-f9ad292f42ce" />

<img width="1001" height="590" alt="image" src="https://github.com/user-attachments/assets/361777c9-9402-40c1-b48d-008fef66ecf7" />
<img width="836" height="599" alt="image" src="https://github.com/user-attachments/assets/17ea3e24-4105-48e4-b11b-8bcfa974a093" />

<img width="723" height="567" alt="image" src="https://github.com/user-attachments/assets/16c679b3-b12b-476d-ae26-fca1797cda38" />
<img width="775" height="544" alt="image" src="https://github.com/user-attachments/assets/2fcd9b09-b640-4fb1-8a18-ffd0c65d7d82" />
<img width="979" height="546" alt="image" src="https://github.com/user-attachments/assets/30d4ed2c-b337-4a3a-a9c0-64d7a57867be" />

<img width="1037" height="617" alt="image" src="https://github.com/user-attachments/assets/55e3ed76-e9b7-4886-8911-5650519a88cb" />
<img width="1064" height="521" alt="image" src="https://github.com/user-attachments/assets/047e07dd-5c20-4bd4-8b14-8e37de3dd44c" />

<img width="1166" height="457" alt="image" src="https://github.com/user-attachments/assets/a524c8c7-0945-45a1-81e1-5d7612470492" />

<img width="1012" height="458" alt="image" src="https://github.com/user-attachments/assets/291575b6-1961-4476-99f9-bb33990facc5" />
<img width="996" height="482" alt="image" src="https://github.com/user-attachments/assets/403b6174-4abd-4b60-81a9-3b94b74e24bd" />
<img width="1030" height="438" alt="image" src="https://github.com/user-attachments/assets/c530603e-348c-424d-8c35-0d8d44db892e" />
<img width="1033" height="441" alt="image" src="https://github.com/user-attachments/assets/447f0c89-e614-4a35-adf0-c2422df5c04d" />
<img width="989" height="456" alt="image" src="https://github.com/user-attachments/assets/146ba3a7-338c-476d-b930-33e236e64f98" />
<img width="1036" height="427" alt="image" src="https://github.com/user-attachments/assets/c87589c0-4470-458e-a9e7-7c1258941dcb" />

<img width="821" height="109" alt="image" src="https://github.com/user-attachments/assets/c03e5deb-7972-4a89-9cf6-3cbcc0b5fa31" />
<img width="1096" height="519" alt="image" src="https://github.com/user-attachments/assets/f7761201-b7dc-4989-be9e-ba14f4421d28" />
<img width="1067" height="543" alt="image" src="https://github.com/user-attachments/assets/39f78902-4d4f-437c-892f-9da74ab441eb" />
<img width="1006" height="601" alt="image" src="https://github.com/user-attachments/assets/f7de78fa-0f8a-4a71-8867-b7c96ef811d9" />




