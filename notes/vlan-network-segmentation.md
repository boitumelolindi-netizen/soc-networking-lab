# VLAN and Network Segmentation

## 1. What is a VLAN?

VLAN stands for Virtual Local Area Network.

A VLAN divides one physical network into multiple logical networks. It allows organisations to separate devices and users into different network segments, even when they are connected to the same physical switch.

## 2. Example of VLAN Segmentation

Imagine a company with three departments:

| Department      | VLAN ID | Network         |
| --------------- | ------- | --------------- |
| Human Resources | VLAN 10 | 192.168.10.0/24 |
| Finance         | VLAN 20 | 192.168.20.0/24 |
| IT              | VLAN 30 | 192.168.30.0/24 |

Each department belongs to a separate VLAN.

## 3. Why Do Organisations Use VLANs?

* **Security:** Separates sensitive departments and systems.
* **Traffic management:** Reduces unnecessary broadcast traffic.
* **Access control:** Helps control communication between departments.
* **Organisation:** Groups devices according to their functions.

## 4. Important VLAN Terminology

| Term               | Meaning                                                                          |
| ------------------ | -------------------------------------------------------------------------------- |
| VLAN               | Virtual Local Area Network; a logical network segment.                           |
| Access Port        | A switch port assigned to a single VLAN.                                         |
| Trunk Port         | A switch port that carries traffic for multiple VLANs.                           |
| VLAN ID            | A unique identification number assigned to a VLAN.                               |
| Inter-VLAN Routing | Allows communication between different VLANs through a router or Layer 3 switch. |

## 5. VLANs and Cybersecurity

VLANs are important in cybersecurity because they help organisations separate network traffic and restrict unnecessary communication between devices.

For example, a company can separate its HR, Finance and IT departments into different VLANs.

This helps limit unauthorised access and can reduce the impact of security incidents.

## 6. SOC Analyst Perspective

Imagine an employee's computer in the HR department suddenly communicating with a Finance server.

A SOC analyst should investigate:

1. Is the communication authorised?
2. Should the HR VLAN have access to the Finance VLAN?
3. Were firewall rules allowing this communication?
4. Could this activity indicate lateral movement?
5. Are there unusual connections or suspicious network events?

## 7. Key Takeaways

* VLAN stands for Virtual Local Area Network.
* VLANs logically separate devices on a physical network.
* Each VLAN has a unique VLAN ID.
* Access ports typically belong to one VLAN.
* Trunk ports carry traffic from multiple VLANs.
* Inter-VLAN routing enables communication between separate VLANs.
* VLANs improve network organisation and support security segmentation.

## 8. Practical Learning Reflection

I learned how VLANs divide physical networks into logical segments and how organisations use network segmentation to improve security and manage network traffic.

Although I did not complete a Packet Tracer simulation, I studied VLAN concepts and explored how network segmentation supports SOC investigations.
