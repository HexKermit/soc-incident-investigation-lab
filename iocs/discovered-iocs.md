# Indicators of Compromise (IOCs)

| IOC Type         | Value              | Description                                                        |
| ---------------- | ------------------ | ------------------------------------------------------------------ |
| IP Address       | 175.45.176.199     | Suspicious remote communication identified during network analysis |
| IP Address       | 175.45.176.200     | Suspicious established network connection                          |
| Process          | explorer.exe       | Process associated with suspicious outbound communication          |
| Process          | MSN.EXE            | Process observed with active network connection activity           |
| Tool/Artifact    | Autoruns Entry     | Suspicious persistence mechanism identified                        |
| Network Activity | SSH Traffic        | Encrypted SSH communication observed in packet analysis            |
| Analysis Tool    | Volatility netscan | Memory-based network connection analysis                           |
| Analysis Tool    | Wireshark          | Packet and traffic inspection performed                            |

---

# IOC Analysis Notes

The investigation identified suspicious outbound communication, persistence-related artifacts, and network activity associated with potentially compromised processes.

Several indicators were identified through process analysis, memory forensics, packet inspection, and persistence analysis workflows performed in a controlled lab environment.
