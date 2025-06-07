# 🌐 BGP Routing Practical in Cisco Packet Tracer

## 📘 Overview

This project demonstrates how to configure **Border Gateway Protocol (BGP)** on multiple Autonomous Systems (AS) in a complex Cisco network topology using **Cisco Packet Tracer**. The goal is to ensure inter-AS communication across 8 different AS numbers through proper BGP configuration.

---

## 🎯 Objectives

- Understand how BGP functions across multiple ASes.
- Learn how to advertise and propagate networks via BGP.
- Implement BGP peerings between routers in different ASes.
- Test connectivity using ICMP (ping) between PCs across different networks.

---

## 🧰 Tools & Technologies Used

- **Cisco Packet Tracer**
- **Routers**: 2621XM
- **Switches**: 2960 series
- **End Devices**: PC-PT
- **Protocol**: BGP (Border Gateway Protocol), ICMP (for testing)

---

## 🖥️ Topology Diagram

> 📷 Below is the actual topology used in this BGP practical:

![BGP Topology](./01-BGP-Topology.png)

---

## ⚙️ BGP Configuration Details

The network consists of **8 Autonomous Systems** with peering configured as follows:

---

### 🔹 Router 0 (AS 65001)

 <pre><code> router bgp 65001
 network 192.168.10.0 mask 255.255.255.0
 neighbor 10.0.0.2 remote-as 65002
 neighbor 20.0.0.2 remote-as 65003 </code></pre>

---

### 🔹 Router 1 (AS 65002)

 <pre><code> router bgp 65002
 network 192.168.40.0 mask 255.255.255.0
 neighbor 10.0.0.1 remote-as 65001
 neighbor 70.0.0.1 remote-as 65004 </code></pre>

---

### 🔹 Router 2 (AS 65003)

 <pre><code> router bgp 65003
 network 192.168.20.0 mask 255.255.255.0
 neighbor 20.0.0.1 remote-as 65001
 neighbor 40.0.0.2 remote-as 65005
 neighbor 30.0.0.2 remote-as 65007 </code></pre>

---

### 🔹 Router 3 (AS 65004)

 <pre><code> router bgp 65004
 network 192.168.50.0 mask 255.255.255.0
 neighbor 70.0.0.2 remote-as 65002
 neighbor 60.0.0.1 remote-as 65006
 neighbor 80.0.0.2 remote-as 65008 </code></pre>

---

### 🔹 Router 4 (AS 65005)
 
 <pre><code> router bgp 65005
 network 192.168.30.0 mask 255.255.255.0
 neighbor 40.0.0.1 remote-as 65003
 neighbor 50.0.0.2 remote-as 65006 </code></pre>

---

### 🔹 Router 5 (AS 65006)

 <pre><code> router bgp 65006
 network 192.168.60.0 mask 255.255.255.0
 neighbor 60.0.0.2 remote-as 65004
 neighbor 50.0.0.1 remote-as 65005 </code></pre>

---

### 🔹 Router 6 (AS 65007)

 <pre><code> router bgp 65007
 network 192.168.70.0 mask 255.255.255.0
 neighbor 30.0.0.1 remote-as 65003
 neighbor 90.0.0.2 remote-as 65008 </code></pre>

---

### 🔹 Router 7 (AS 65008)

 <pre><code> router bgp 65008
 network 192.168.80.0 mask 255.255.255.0
 neighbor 90.0.0.1 remote-as 65007
 neighbor 80.0.0.1 remote-as 65004 </code></pre>

---

### 🔹 Final Test Status
Source	Destination	Result
<pre> PC0 - PC7	✅ Success </pre>
<pre> PC9 - PC2	✅ Success </pre>

📷 Successful Ping:

![BGP Ping Successful](./02-BGP-Routing-Successfull.png)
