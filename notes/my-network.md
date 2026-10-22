# My Network

## 1. Objective

The purpose of this exercise is to identify my Windows laptop's network configuration and understand how IP addresses, subnet masks, default gateways, DHCP, and DNS work.

## 2. Active Wi-Fi Network

| Property        | Value           |
| --------------- | --------------- |
| Interface       | Wi-Fi 2         |
| IPv4 address    | 172.20.10.4     |
| Subnet mask     | 255.255.255.240 |
| CIDR prefix     | /28             |
| Default gateway | 172.20.10.1     |
| DHCP server     | 172.20.10.1     |
| DNS server      | 172.20.10.1     |

The Wi-Fi interface uses a private IPv4 address. Its subnet is 172.20.10.0/28, with a broadcast address of 172.20.10.15.

## 3. VirtualBox Host-Only Network

| Property          | Value                                 |
| ----------------- | ------------------------------------- |
| Interface         | Ethernet 3                            |
| Adapter type      | VirtualBox Host-Only Ethernet Adapter |
| Host IPv4 address | 192.168.56.1                          |
| Subnet mask       | 255.255.255.0                         |
| CIDR prefix       | /24                                   |
| Default gateway   | None configured on this interface     |
| DHCP enabled      | No                                    |

The host-only adapter provides a private virtual network interface for communication between the Windows host and appropriately configured virtual machines.

The Kali VM's host-only configuration still needs to be verified.

## 4. Key Networking Concepts

* **IP address:** A logical address used to identify a network interface and route traffic.
* **MAC address:** A link-layer address used to deliver frames over a local network link.
* **Subnet mask:** Determines which IPv4 addresses belong to the same subnet.
* **Default gateway:** The next-hop device used to reach destinations outside the local subnet.
* **DHCP:** Automatically provides network configuration to a device.
* **DNS:** Resolves domain names into IP addresses and supports other DNS record lookups.

## 5. Why This Matters to a SOC Analyst

Understanding network configuration helps a SOC analyst determine whether an IP address belongs to a known internal subnet, identify relevant network interfaces, and interpret network traffic and security alerts.

## 6. Privacy and Safety

This documentation excludes MAC addresses, public IP addresses, passwords, and other unnecessary identifying information.

All future scanning exercises will be restricted to authorised lab systems.
