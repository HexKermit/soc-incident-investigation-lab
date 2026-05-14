# SOC Incident Investigation: Compromised Windows Host Analysis

## Overview

This hands-on SOC investigation project simulates the analysis of a compromised Windows system in a controlled lab environment. The investigation focuses on identifying indicators of compromise (IOCs), analyzing suspicious processes and network connections, reviewing logs, and documenting incident response findings.

The project combines Windows host investigation, log analysis, packet analysis, Splunk investigation workflows, and forensic methodology.

---

## Objectives

* Investigate indicators of compromise (IOCs)
* Analyze suspicious processes and network connections
* Review Windows and Linux logs
* Examine persistence mechanisms
* Perform packet and traffic analysis
* Understand incident response and forensic workflows
* Document findings and remediation steps

---

## Skills Demonstrated

* Incident Response
* SOC Investigation
* Log Analysis
* Splunk
* Wireshark
* Windows Forensics
* IOC Analysis
* Threat Detection
* Network Traffic Analysis
* Process Investigation
* Vulnerability Analysis

---

## Tools Used

* Splunk
* Wireshark
* NetworkMiner
* Process Explorer
* Autoruns
* Netstat
* Nmap
* OpenVAS
* Autopsy
* Kali Linux
* Windows Server
* Linux CLI tools

---

## Lab Components

### 1. Investigating a Network Compromise

* Volatile data collection
* RAM analysis
* Scheduled task investigation
* Service analysis
* File artifact investigation

### 2. Finding Malicious Indicators

* Process analysis
* Suspicious connection analysis
* Registry persistence investigation
* IOC discovery

### 3. Log Analysis in Linux and Splunk

* Linux authentication logs
* Apache access logs
* Splunk investigation workflows
* Threat hunting basics

### 4. Deep Packet Analysis

* Protocol analysis
* Packet inspection
* Traffic filtering
* Network artifact analysis

### 5. Digital Forensics Workflow

* Evidence handling
* Chain of custody concepts
* Forensic reporting
* Autopsy investigation basics

---

## Key Takeaways

* Attackers often leave indicators in processes, logs, memory, and network traffic.
* Log analysis and packet analysis are critical during incident response.
* Visibility and monitoring are essential for threat detection.
* Documentation and reporting are important parts of security operations.

---

## Status

Project documentation and investigation reports are currently being added.

---

# Investigation Evidence

## Process Investigation

### Process Explorer TCP/IP Analysis

The investigation identified suspicious outbound network connections associated with active processes. Process Explorer was used to correlate running processes with active TCP/IP connections and identify unusual remote communication.

![Process Explorer Analysis](screenshots/process-analysis/process-explorer-tcp-analysis.png)

---

### Persistence Mechanism Analysis

Autoruns was used to identify suspicious startup persistence entries and unauthorized application execution paths. Persistence mechanisms are commonly used by attackers to maintain long-term access.

![Autoruns Persistence Analysis](screenshots/process-analysis/autoruns-persistence-analysis.png)

---

### Memory Process Analysis

Volatility Framework was used to review running processes from a memory image and identify potentially suspicious activity within system memory artifacts.

![Volatility Process Analysis](screenshots/process-analysis/volatility-pslist-analysis.png)

---

# Network Investigation

### Suspicious Network Connections

Netstat analysis identified active established connections and associated process identifiers (PIDs), helping correlate suspicious communication with running processes.

![Netstat Connection Analysis](screenshots/network-analysis/netstat-established-connections.png)

---

### Memory-Based Network Analysis

Volatility netscan analysis was performed to identify active and historical network connections from memory artifacts.

![Volatility Netscan Analysis](screenshots/network-analysis/volatility-netscan-analysis.png)

---

### Packet and Traffic Analysis

Wireshark was used to inspect network traffic, review SSH communication, and analyze packet-level activity associated with suspicious connections.

![Wireshark SSH Analysis](screenshots/network-analysis/wireshark-ssh-analysis.png)

---

# Security Recommendations

Based on the investigation findings, the following remediation and hardening actions are recommended:

* Investigate suspicious outbound network communication
* Review and disable unauthorized startup persistence entries
* Perform malware scanning and forensic validation
* Restrict unnecessary outbound connections
* Monitor network traffic for unusual SSH communication
* Improve endpoint logging and centralized monitoring
* Review process execution and startup behavior
* Apply security patches and endpoint hardening controls
* Implement SIEM alerting for suspicious process and connection activity
* Perform continuous log monitoring and threat hunting activities

---

# Conclusion

This project demonstrates a hands-on SOC investigation workflow involving process analysis, memory analysis, network traffic inspection, persistence analysis, and incident investigation techniques in a controlled lab environment.

The investigation highlights how attackers may leave indicators across processes, memory, logs, persistence mechanisms, and network communications, emphasizing the importance of visibility, monitoring, and incident response readiness.

