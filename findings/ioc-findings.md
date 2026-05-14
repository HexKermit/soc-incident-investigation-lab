# IOC Findings Report

## Investigation Summary

A simulated SOC investigation was performed against a compromised Windows system in a controlled lab environment.

The objective of the investigation was to identify indicators of compromise (IOCs), suspicious persistence mechanisms, malicious processes, and unauthorized network activity.

---

## Observed Indicators of Compromise

| Indicator Type          | Observation                                     | Security Impact                             |
| ----------------------- | ----------------------------------------------- | ------------------------------------------- |
| Suspicious Process      | Unknown process identified in memory            | Possible malware execution                  |
| Unauthorized Connection | Suspicious outbound network connection observed | Potential command-and-control communication |
| Persistence Mechanism   | Startup-related persistence identified          | Malware persistence across reboots          |
| Suspicious Service      | Unknown service configured on system            | Potential attacker foothold                 |
| Log Artifacts           | Unusual authentication and process activity     | Possible unauthorized access                |

---

## Investigation Techniques Used

* Process analysis using Process Explorer
* Network connection review using netstat
* Startup persistence review using Autoruns
* Log review using Splunk and Linux log analysis tools
* Packet analysis using Wireshark
* Forensic workflow review using Autopsy

---

## Initial Mitigation Recommendations

* Isolate affected systems from the network
* Investigate suspicious outbound traffic
* Disable unauthorized services
* Review persistence mechanisms
* Reset potentially compromised credentials
* Perform full malware and forensic analysis

---

## Lessons Learned

* Indicators of compromise can appear in processes, logs, memory, and network traffic.
* Continuous monitoring and log visibility are critical for incident response.
* Persistence mechanisms are commonly used to maintain attacker access.
* Proper documentation improves incident response workflows.
