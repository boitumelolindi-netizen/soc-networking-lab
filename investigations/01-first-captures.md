# Investigation 01: Network Printing Traffic

## 1. Objective

Analyse a sample packet capture using Wireshark to identify the communicating hosts, protocol, service, and purpose of the traffic.

## 2. Evidence Collected

* Source IP: 10.10.10.49
* Destination IP: 10.10.10.251
* Destination port: 631/TCP
* Protocols observed: TCP, HTTP, IPP
* HTTP request: POST /ipp/
* Content-Type: application/ipp
* User-Agent: CUPS/1.3.4
* Requesting username: guest
* Declared Content-Length: 227309 bytes

## 3. Findings

The TCP conversation contains an HTTP POST request directed to an IPP service on port 631.

The request headers and payload are consistent with printing-related communication. The User-Agent identifies CUPS/1.3.4, and the request includes a printer URI.

## 4. Initial Assessment

The observed traffic appears consistent with a client submitting a printing-related request.

The available evidence does not establish malicious activity or unauthorised access.

## 5. Recommended Next Steps

1. Inspect the corresponding server response.
2. Review the beginning and end of the TCP stream for connection and transaction details.
3. Determine whether the printing activity is expected in the capture's environment.
4. Investigate further if additional evidence indicates suspicious behaviour.

## 6. Safety Note

This investigation uses a sample packet capture. Its addresses and activity are not evidence of activity on my own network.
