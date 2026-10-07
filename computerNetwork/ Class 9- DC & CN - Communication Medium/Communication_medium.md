
<img width="1135" height="539" alt="image" src="https://github.com/user-attachments/assets/ff70e41c-6cd3-4a3c-979c-fa822212d3a8" />
# Communication Media
**Communication medium** is the path through which data travels from a **sender to a receiver**.

Communication media are mainly divided into two types:

---

## 1. Guided Media(Wired Media)

**Guided media** is a communication medium where signals travel through a **physical cable or wire**.

### Types

* **Twisted Pair Cable** → UTP, STP
* **Coaxial Cable**
* **Fiber Optic Cable**

### Example

```text
Computer → Ethernet Cable → Switch → Computer
```

### Features

* Uses a physical transmission path
* Generally more secure
* Less mobility
* Suitable for wired networks

---

## 2. Unguided(Wireless) Media

**Unguided media** is a communication medium where signals travel through **air or space without a physical cable**.

### Types

* **Radio Waves**
* **Microwaves**
* **Infrared**
* **Satellite Communication**

### Example

```text
Mobile → Radio Waves → Wi-Fi Router
```

### Features

* No physical cable required
* Provides mobility
* Easy to deploy
* More affected by interference and obstacles

---

## Guided vs Unguided Media

| Feature           | Guided Media        | Unguided Media             |
| ----------------- | ------------------- | -------------------------- |
| Transmission Path | Physical cable      | Air/Space                  |
| Also Called       | Wired               | Wireless                   |
| Examples          | UTP, Coaxial, Fiber | Radio, Microwave, Infrared |
| Mobility          | Low                 | High                       |
| Cable Required    | Yes                 | No                         |
| Interference      | Generally lower     | Generally higher           |

<img width="649" height="434" alt="image" src="https://github.com/user-attachments/assets/6b7ac28c-1f21-478c-99d6-022995206786" />
# Twisted Pair Cable

**Twisted Pair Cable** is a **guided/wired transmission medium** made of pairs of **insulated copper wires twisted together**.

The twisting helps reduce **electromagnetic interference (EMI)** and **crosstalk**.

---

## Types

### 1. UTP — Unshielded Twisted Pair

* No additional shielding
* Low cost
* Lightweight
* Commonly used in Ethernet/LAN

### 2. STP — Shielded Twisted Pair

* Has additional shielding
* Better protection against interference
* More expensive than UTP

---

## Features

* Uses copper wires
* Two insulated wires are twisted together
* Reduces interference and crosstalk
* Used mainly in LAN/Ethernet networks
* Supports different Ethernet speeds depending on cable category

---

## Coverage Area

* A common Ethernet twisted-pair cable supports up to **100 meters per cable segment**.
* For longer distances, switches, fiber optic cables, or other network equipment may be required.

---

## Connector

**RJ-45 (8P8C)** is commonly used for Ethernet twisted-pair cables.

```text
Computer → RJ-45 → Twisted Pair Cable → RJ-45 → Switch
```

---

## Advantages

* Low cost
* Easy to install
* Lightweight
* Flexible
* Widely available
* Suitable for LAN networks

---

## Disadvantages

* Limited transmission distance
* More susceptible to electromagnetic interference than fiber optic cable
* Signal attenuation increases with distance
* Generally less suitable than fiber for very high-speed, long-distance communication

---
# Twisted Pair Cable

**Twisted Pair Cable** is a type of **guided transmission medium** made of two insulated copper wires twisted together to reduce **electromagnetic interference (EMI)** and **crosstalk**.

## Types of Twisted Pair Cable

There are two main types:

1. **UTP — Unshielded Twisted Pair**
2. **STP — Shielded Twisted Pair**

---

## 1. UTP — Unshielded Twisted Pair

**UTP** is a twisted pair cable that has **no additional metallic shielding** around the twisted wire pairs.

### Features

* No additional shielding
* Lightweight and flexible
* Low cost
* Easy to install
* Commonly used in **LAN/Ethernet**
* More affected by **EMI** than STP

### Examples

* Cat5e
* Cat6
* Cat6a

---

## 2. STP — Shielded Twisted Pair

**STP** is a twisted pair cable that has **metallic shielding** to protect the cable from electromagnetic interference.

### Features

* Has additional metallic shielding
* Better protection against **EMI**
* More expensive than UTP
* Heavier and less flexible
* Used in environments with high electrical interference

---

## STP vs UTP

| Feature        | UTP                     | STP                              |
| -------------- | ----------------------- | -------------------------------- |
| Full Form      | Unshielded Twisted Pair | Shielded Twisted Pair            |
| Shielding      | No                      | Yes                              |
| EMI Protection | Low                     | High                             |
| Cost           | Low                     | Higher                           |
| Installation   | Easy                    | More difficult                   |
| Flexibility    | High                    | Lower                            |
| Common Use     | Home/Office LAN         | Industrial/High-EMI environments |

## Easy Remember

```text
UTP → No Shield → Cheap + Flexible + Easy

STP → Shield → Better EMI Protection + More Expensive
```

### Key Point

> **UTP is cheaper and easier to install, while STP provides better protection against electromagnetic interference.**


# Ushieded twisted pair cable (UTP) two type 1) Cat5 2. Cat6


> **Cat6 provides higher bandwidth, better performance, and lower crosstalk than Cat5.**

| Feature     | Cat5           | Cat6           |
| ----------- | -------------- | -------------- |
| Bandwidth   | 100 MHz        | 250 MHz        |
| Speed       | Up to 100 Mbps | Up to 1 Gbps   |
| Crosstalk   | Higher         | Lower          |
| Performance | Lower          | Higher         |
| Cost        | Cheaper        | More expensive |
| Common Use  | Older networks | Modern LAN     |

# Standerd Twisted pair  eithernet cable 
<img width="460" height="285" alt="image" src="https://github.com/user-attachments/assets/82be76ec-b7fe-4244-babf-ebfeb7f1dc30" />

# Straight-Through vs Crossover Cable

## 1. Straight-Through Cable

A **straight-through cable** uses the **same wiring standard on both ends**.

```text
End A              End B
T568A  ──────────  T568A
   OR
T568B  ──────────  T568B
```

### Used to connect:
সাধারণত ভিন্ন ধরনের device connect করতে used hoi. :
* PC → Switch
* PC → Hub
* Router → Switch

---

## 2. Crossover Cable

A **crossover cable** uses **different wiring standards** on the two ends.

```text
End A              End B
T568A  ──────────  T568B
```

The **Transmit (TX)** and **Receive (RX)** pairs are crossed.

### Used traditionally to connect:
কোথায় ব্যবহার করা হতো?

সাধারণত একই ধরনের device connect করতে:

* PC → PC
* Switch → Switch
* Hub → Hub
* Router → Router

---

## T568A vs T568B

| Pin | T568A        | T568B        |
| --- | ------------ | ------------ |
| 1   | White/Green  | White/Orange |
| 2   | Green        | Orange       |
| 3   | White/Orange | White/Green  |
| 4   | Blue         | Blue         |
| 5   | White/Blue   | White/Blue   |
| 6   | Orange       | Green        |
| 7   | White/Brown  | White/Brown  |
| 8   | Brown        | Brown        |

### Easy Remember

```text
Straight-Through → Same standard → A-A or B-B

Crossover       → Different standard → A-B
```

> **Important:** Modern Ethernet devices commonly support **Auto-MDI/MDIX**, so many modern devices can automatically detect and correct TX/RX pairs. Therefore, crossover cables are much less necessary today.


