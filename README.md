# Incident Forensic Report: Natureforce AD Compromise

# 1. Executive Summary
- **Incident Type:** Unauthorized Executable Deployment & C2 Communication
- **Target Network:** Natureforce Active Directory Domain (`natureforce.com`)
- **Impact:** Compromise of an internal workstation via unverified external payload over non-standard TCP ports.

---

## 2. Compromised Host Artifacts (IOCs)
The following forensic indicators were extracted from the network traffic capture (`.pcap`) using Wireshark and DHCP analysis:

| Indicator Category   | Forensic Value |

| **Infected Host IP** | `10.10.1.128` |
| **MAC Address**      | `00:22:fb:fe:7e:e7` |
| **Hostname**         | `DESKTOP-4V6YQX7` |
| **User Account**     | `bdiaz` |
| **C2 Destination IP**| `107.175.82.242:9000` |

---

# 3. Malware Payload & Cryptographic Hash
The suspicious binary file (`runner_jlove.exe`) downloaded during the incident was extracted from the packet capture and analyzed:

- **Filename:** `runner_jlove.exe`
- **SHA-256 Hash:** `b789adce70c028a6d17be45ec34667aa95586350ee0c4057e75b138b1ad35061`

```bash
# Verification command executed in analysis environment:
sha256sum runner_jlove.exetureforce-Incident-Report
