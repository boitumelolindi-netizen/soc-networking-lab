# Investigation 02: Nmap Port Scan Analysis

## 1. Objective

Analyse a sample packet capture in Wireshark to identify potential port-scanning activity.

## 2. Capture Details

* Capture file: `nmap_standard_scan`
* Source IP: `192.168.100.103`
* Destination IP: `192.168.100.102`
* Tool identified by capture filename: Nmap

## 3. Evidence Collected

* TCP SYN packets were observed.
* The SYN flag was set, while the ACK flag was absent in the inspected probe.
* Multiple destination ports were observed, including ports 23, 25, 135, 445, 3389 and 5900.
* Display filters for TCP RST responses and SYN-ACK responses returned no matching packets.

## 4. Findings

The source host sent TCP SYN packets to multiple destination ports on the target host. This pattern is consistent with TCP SYN port-scanning activity.

## 5. Initial Assessment

The capture provides evidence consistent with an Nmap port scan.

The available analysis did not identify TCP RST or SYN-ACK responses using the filters applied. Therefore, the status of the scanned ports cannot be established from these results alone.

## 6. Recommended Next Steps

1. Review the complete packet capture to verify whether responses use different addresses or protocols.
2. Confirm the scan technique using additional packet details and the capture documentation.
3. Correlate the activity with authorised scanning records if this were a real SOC investigation.

## 7. Safety Note

This investigation used a downloaded sample packet capture. The addresses and activity observed are not evidence of scanning on my own network.
