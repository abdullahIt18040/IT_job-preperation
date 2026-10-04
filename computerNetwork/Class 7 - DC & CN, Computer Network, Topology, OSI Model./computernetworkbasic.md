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




