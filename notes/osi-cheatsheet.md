# OSI and TCP/IP Model Cheat Sheet

## 1. Purpose

The OSI model explains network communication using seven layers.
The TCP/IP model groups networking functions into four layers.

SOC analysts use networking knowledge to investigate suspicious
connections, unusual traffic, and potential attacks.

## 2. OSI Model

| Layer | Name | Example | SOC Relevance |
|---|---|---|---|
| 7 | Application | HTTP, DNS | Investigate suspicious URLs and DNS queries |
| 6 | Presentation | TLS, data encoding | Understand encryption and data formatting |
| 5 | Session | Session management | Investigate unexpected session activity |
| 4 | Transport | TCP, UDP | Investigate port scans and connections |
| 3 | Network | IPv4, IPv6, routers | Investigate suspicious IP addresses |
| 2 | Data Link | Ethernet, ARP | Investigate possible ARP spoofing |
| 1 | Physical | Cables, radio signals | Understand physical connectivity issues |

## 3. TCP/IP Model

| Layer | Examples |
|---|---|
| Application | HTTP, DNS, DHCP |
| Transport | TCP, UDP |
| Internet | IPv4, IPv6, ICMP |
| Network Access | Ethernet, Wi-Fi, ARP |

## 4. Key Differences

- The OSI model has seven layers.
- The TCP/IP model has four layers.
- The OSI model is a conceptual reference model.
- The TCP/IP model describes the networking architecture used
  by the internet.

## 5. Why This Matters in a SOC

A SOC analyst uses network evidence to investigate security alerts.

Examples include:
- Identifying suspicious source and destination IP addresses.
- Investigating unusual destination ports.
- Recognising suspicious DNS requests.
- Examining network traffic in Wireshark.

## 6. What I Learned

- The seven OSI layers and their responsibilities.
- The four TCP/IP layers.
- How network layers relate to security investigations.
