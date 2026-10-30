# Firewall Logs and SOC Analysis

## 1. What is a Firewall?

A firewall is a network security system that monitors and controls incoming and outgoing network traffic based on predefined security rules.

Firewalls help organisations:

* Allow legitimate network connections.
* Block unauthorised connections.
* Restrict access to specific ports.
* Monitor and record network activity.

## 2. Firewall Actions

| Action | Meaning                                           |
| ------ | ------------------------------------------------- |
| ALLOW  | Traffic is permitted.                             |
| DENY   | Traffic is rejected.                              |
| DROP   | Traffic is silently discarded without a response. |

## 3. Important Firewall Log Fields

| Field            | Meaning                          |
| ---------------- | -------------------------------- |
| Timestamp        | When the event occurred.         |
| Source IP        | Where the traffic originated.    |
| Destination IP   | Where the traffic is going.      |
| Source Port      | Port used by the sending device. |
| Destination Port | Port targeted by the traffic.    |
| Protocol         | TCP, UDP or ICMP.                |
| Action           | ALLOW, DENY or DROP.             |

## 4. Common Network Ports

| Port | Service | Purpose                           |
| ---- | ------- | --------------------------------- |
| 53   | DNS     | Domain name resolution.           |
| 80   | HTTP    | Web traffic.                      |
| 443  | HTTPS   | Secure web traffic.               |
| 445  | SMB     | Windows file and printer sharing. |
| 3389 | RDP     | Remote Desktop Protocol.          |

## 5. Firewall Investigation Example

A company firewall records the following events:

| Time     | Source IP    | Destination IP | Port | Protocol | Action |
| -------- | ------------ | -------------- | ---- | -------- | ------ |
| 09:00:01 | 192.168.1.15 | 8.8.8.8        | 53   | UDP      | ALLOW  |
| 09:00:05 | 192.168.1.20 | 192.168.1.100  | 445  | TCP      | DENY   |
| 09:00:08 | 192.168.1.30 | 192.168.1.50   | 3389 | TCP      | DENY   |
| 09:00:12 | 192.168.1.15 | 1.1.1.1        | 53   | UDP      | ALLOW  |
| 09:00:15 | 192.168.1.20 | 192.168.1.100  | 445  | TCP      | DENY   |
| 09:00:18 | 192.168.1.20 | 192.168.1.100  | 445  | TCP      | DENY   |

### Observations

1. The device 192.168.1.15 communicates with DNS servers using port 53.
2. The device 192.168.1.20 repeatedly attempts to access port 445 (SMB), but the firewall denies the connections.
3. The device 192.168.1.30 attempts to access port 3389 (RDP), but the firewall denies the connection.

These events should be investigated to determine whether the activity is authorised or suspicious.

## 6. SOC Analyst Responsibilities

A SOC analyst investigating firewall alerts should:

1. Identify the source and destination IP addresses.
2. Identify the ports and protocols involved.
3. Review the firewall action.
4. Check how frequently the events occur.
5. Investigate whether the activity is authorised.
6. Correlate the events with other security logs.
7. Document findings and recommend further action.

## 7. Key Takeaways

* Firewalls monitor and control network traffic.
* ALLOW means traffic is permitted.
* DENY means traffic is rejected.
* DROP means traffic is silently discarded.
* Port 445 is commonly associated with SMB.
* Port 3389 is commonly associated with RDP.
* Repeated denied connections may require investigation.
* Firewall logs provide valuable evidence during security investigations.

## 8. Practical Learning Reflection

I learned how firewalls control network traffic and how to interpret firewall log entries. I also learned how SOC analysts investigate denied connections by examining source addresses, destination addresses, ports, protocols and event frequency.
