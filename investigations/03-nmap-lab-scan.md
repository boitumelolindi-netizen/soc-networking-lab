# Investigation 03: Nmap Practical Lab

## 1. Objective

Practise host discovery and TCP service scanning in a VirtualBox lab environment.

## 2. Environment

* Operating system: Kali Linux
* Nmap version: 7.95
* Host-only interface: eth1
* Host-only IP address: 192.168.56.103/24
* Host-only subnet: 192.168.56.0/24

## 3. Tests Performed

### Test A: Localhost service scan

Command: `sudo nmap -sV 127.0.0.1`

Result:

* Host was up.
* All 1,000 scanned TCP ports were closed.
* No open TCP ports were identified.

### Test B: Host discovery

Command: `sudo nmap -sn 192.168.56.0/24`

Result:

* Three hosts were reported as up:

  * 192.168.56.1
  * 192.168.56.100
  * 192.168.56.103

### Test C: TCP service scan

Command: `sudo nmap -sV 192.168.56.100`

Result:

* Host was up.
* All 1,000 scanned TCP ports were closed.
* No open TCP ports were identified.

### Test D: Local socket inspection

Commands:

* `sudo ss -lntup`
* `sudo ss -lntp`

Result:

* A UDP socket on port 546 was associated with NetworkManager.
* No TCP listening sockets were displayed by `ss -lntp`.

## 4. Findings

The host-discovery scan identified three responding hosts on the host-only subnet. The subsequent TCP scans found no open TCP ports among the 1,000 default ports checked on localhost and 192.168.56.100.

## 5. Limitations

The scans did not assess every TCP port, all UDP services, vulnerabilities, or the overall security posture of the hosts. The identity of 192.168.56.100 has not been confirmed.

## 6. Safety Note

The scans were limited to localhost and the configured VirtualBox host-only subnet. No scan of the bridged Wi-Fi subnet was intentionally performed.
