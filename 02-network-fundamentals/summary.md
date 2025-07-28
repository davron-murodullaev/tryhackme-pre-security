# SECTION 2: Network Fundamentals

## 1. Objectives
In this section you will learn:
- **What is Networking?** basic purpose and components
- **Intro to LAN:** local area networks and topology
- **OSI Model:** seven-layer model for network communication
- **Packets & Frames:** how data is encapsulated and transmitted
- **Extending Your Network:** routers, switches, subnets

## 2. Key Commands & Concepts

| Command / Concept       | Description                                      |
|-------------------------|--------------------------------------------------|
| `ping HOST`             | Test basic connectivity and measure latency      |
| `traceroute HOST`       | Show path and hops from source to destination    |
| OSI Model (Layers 1–7)  | Physical, Data Link, Network, Transport, etc.    |
| Packet vs Frame         | Packet has network header; frame has link header |

## 3. Hands-On Example

1. **Task:** Map the route to a target server  
2. **Steps:**  
   ```bash
   # Check connectivity
   ping 8.8.8.8

   # Trace path
   traceroute tryhackme.com
