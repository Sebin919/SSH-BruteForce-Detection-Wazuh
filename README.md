# SSH-BruteForce-Detection-Wazuh
Detection and analysis of SSH brute-force attacks using Wazuh SIEM, Hydra, and Metasploitable 2 with MITRE ATT&amp;CK mapping and real-time alert monitoring.

# SSH Brute Force Attack Detection using Wazuh SIEM

## Project Overview

This project demonstrates the detection and analysis of SSH brute-force attacks using Wazuh SIEM in a controlled virtual lab environment.

The attack was simulated from a Kali Linux machine against a Metasploitable 2 target system using Hydra. Authentication logs generated during the attack were collected and analyzed by Wazuh SIEM, enabling real-time detection of failed login attempts and security monitoring.

This lab replicates a common Security Operations Center (SOC) use case where analysts investigate unauthorized access attempts and monitor authentication events across enterprise systems.

---

## Objectives

- Deploy Wazuh SIEM for centralized security monitoring
- Simulate SSH brute-force attacks using Hydra
- Monitor authentication logs from Linux systems
- Detect failed login attempts in real time
- Analyze attack indicators through Wazuh Dashboard
- Map detections to MITRE ATT&CK techniques
- Practice SOC investigation workflows

---

## Lab Environment

| Machine | Purpose |
|----------|----------|
| Kali Linux | Attack Machine |
| Metasploitable 2 | Target System |
| Ubuntu Server | Wazuh Manager |
| Wazuh Dashboard | Security Monitoring |

---

## Tools Used

- Wazuh SIEM
- Kali Linux
- Metasploitable 2
- Hydra
- Ubuntu Server
- VirtualBox
- SSH
- Linux Authentication Logs

---

## Attack Scenario

A brute-force attack was launched from Kali Linux against the SSH service running on Metasploitable 2.

Hydra generated multiple authentication attempts using a predefined username and password list.

Wazuh monitored `/var/log/auth.log` on the target machine and generated alerts whenever authentication failures occurred.

---

## Detection Workflow

```text
Kali Linux
     │
     │ SSH Brute Force (Hydra)
     ▼
Metasploitable 2
     │
     │ Authentication Logs
     ▼
Wazuh Agent
     │
     ▼
Wazuh Manager
     │
     ▼
Wazuh Dashboard
     │
     ▼
Security Alert & Investigation
```

---

## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|----------|----------|----------|
| Credential Access | Brute Force | T1110 |
| Credential Access | Password Guessing | T1110.001 |

---

## Key Findings

- Detected multiple failed SSH login attempts.
- Identified attack source IP address.
- Captured authentication failures from Linux logs.
- Generated security events in Wazuh Dashboard.
- Correlated attack behavior with MITRE ATT&CK framework.
- Demonstrated real-time SIEM-based threat detection.

---

## Screenshots

### Wazuh Dashboard Overview

<img width="1918" height="980" alt="wazuh bruteforce 1" src="https://github.com/user-attachments/assets/4183b356-9ea8-4e04-a6a4-49f19b039a72" />


Displays overall security monitoring status, connected agents, and alert severity levels.

---

### Agent Monitoring

<img width="1912" height="871" alt="wazuh bruteforce 2" src="https://github.com/user-attachments/assets/f6c1798d-bc8e-469a-a51b-7079187fd6d6" />


Shows active endpoints including Kali Linux, Metasploitable 2, and Windows systems connected to Wazuh.

---

### SSH Authentication Failure Events

<img width="1917" height="912" alt="wazuh bruteforce 3" src="https://github.com/user-attachments/assets/47d8fcba-e22e-466d-9e20-192f20f8be92" />


Failed SSH login attempts detected from the attacking host and ingested into Wazuh for analysis.

---

### Alert Investigation

<img width="1915" height="903" alt="wazuh bruteforce 4" src="https://github.com/user-attachments/assets/c0dae003-15b7-4bc7-9910-742eba6962ba" />


Detailed alert view displaying:

- Source IP Address
- Username targeted
- Authentication failure events
- Log source
- Timestamp
- Wazuh Manager information

---

## SOC Analyst Investigation

### Indicators Observed

| Indicator | Value |
|------------|------------|
| Target Host | Metasploitable 2 |
| Attack Source | 192.168.56.1 |
| Service Targeted | SSH |
| Username | msfadmin |
| Log Source | /var/log/auth.log |
| Detection Platform | Wazuh SIEM |

### Investigation Steps

1. Review authentication logs.
2. Identify repeated failed login attempts.
3. Verify source IP address.
4. Correlate attack activity.
5. Map to MITRE ATT&CK.
6. Document findings.

---

## Skills Demonstrated

- Security Monitoring
- SIEM Management
- Threat Detection
- Incident Investigation
- Log Analysis
- Linux Security
- MITRE ATT&CK Mapping
- SOC Operations
- Authentication Monitoring

---

## Author

**Sebin Mathai**

LinkedIn: https://linkedin.com/in/sebinmathai

Email: sebinmathai919@gmail.com

Kerala, India
