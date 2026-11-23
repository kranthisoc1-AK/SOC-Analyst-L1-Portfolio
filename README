# Wazuh SIEM – Security Monitoring and Threat Detection

## Project Overview

This project focuses on implementing Wazuh SIEM for endpoint security monitoring, Windows event analysis, file integrity monitoring, and security investigation.

A Wazuh single-node environment was deployed using Docker, and a Windows endpoint was integrated using the Wazuh agent.

The project demonstrates practical experience in SIEM deployment, endpoint monitoring, security event investigation, and threat detection.

## Objectives

- Deploy and configure Wazuh SIEM.
- Integrate a Windows endpoint with Wazuh.
- Monitor Windows Security Event Logs.
- Detect and investigate failed login attempts.
- Configure File Integrity Monitoring (FIM).
- Monitor file and directory modifications.
- Analyse process-related security events.
- Investigate security alerts using the Wazuh dashboard.

## Tools & Technologies

- Wazuh 4.14.10
- Wazuh Manager
- Wazuh Indexer
- Wazuh Dashboard
- Docker Desktop
- Docker Compose
- Windows 11
- Wazuh Windows Agent
- Sysmon
- Ubuntu 24.04 (WSL2)

## Implementation Activities

### 1. Wazuh Installation and Configuration

- Installed Docker Desktop.
- Configured Ubuntu 24.04 through WSL2.
- Deployed Wazuh using the single-node Docker environment.
- Started and verified Wazuh services.
- Accessed the Wazuh dashboard.

### 2. Windows Endpoint Integration

- Installed the Wazuh Windows Agent.
- Connected the Windows endpoint to the Wazuh Manager.
- Verified agent connectivity and status.
- Monitored endpoint security events.

### 3. Windows Security Event Monitoring

- Configured Windows Security event collection.
- Monitored failed login attempts.
- Investigated Windows Security Event ID 4625.
- Analysed authentication-related security events.

### 4. File Integrity Monitoring (FIM)

- Configured monitored Windows directories.
- Enabled real-time file monitoring.
- Created test files and modified existing files.
- Observed file integrity alerts in Wazuh.
- Examined Syscheck event information.

### 5. Security Event Investigation

- Investigated security alerts using Wazuh Threat Hunting.
- Examined Windows event information.
- Analysed process creation telemetry.
- Reviewed security-related activity from the monitored endpoint.

### 6. Security Visualization

- Used Wazuh visualizations to examine security events.
- Created a visualization for login-related activity.
- Reviewed collected security data and alerts.

## Wazuh Search Queries

The following queries use Wazuh Dashboard Discover/Threat Hunting search syntax (DQL).

### 1. Search for Failed Login Attempts

Finds Windows failed login events using Event ID 4625.

```text
data.win.system.eventID:4625
```

### 2. Search for File Integrity Monitoring Alerts

Finds alerts associated with file integrity monitoring.

```text
rule.groups:syscheck
```

### 3. Search for a Specific FIM Detection Rule

Searches for the FIM rule ID observed during the lab investigation.

```text
rule.id:60122
```

### 4. Search for Windows Process Creation Events

Finds Windows process creation events using Sysmon Event ID 1.

```text
data.win.system.eventID:1
```

### 5. Search for Multiple Failed Login Events

Searches for Windows failed login events from Event ID 4625 and displays matching records for investigation.

```text
data.win.system.eventID:4625 AND agent.name:DESKTOP-L29HLL9
```

**Note:** These are Wazuh Dashboard search filters, not KQL or SPL. They filter indexed Wazuh alert documents. Field availability depends on the collected event data and indexing configuration.

## Key Results

- Successfully deployed Wazuh SIEM.
- Integrated a Windows endpoint.
- Verified Windows Security Event ID 4625 collection.
- Successfully generated File Integrity Monitoring alerts.
- Observed process creation events.
- Used Wazuh Threat Hunting and visualizations for investigation.

## Skills Demonstrated

- SIEM Deployment and Configuration
- Endpoint Security Monitoring
- Windows Event Log Analysis
- Failed Login Investigation
- File Integrity Monitoring
- Process Monitoring
- Security Event Investigation
- Docker and WSL2
- Security Dashboard Analysis

## Project Evidence

Refer to the Screenshots folder for installation, agent connectivity, security events, FIM alerts, and dashboard evidence.

## Project Report

See `Wazuh-SIEM-Project-Report.pdf` for detailed implementation and investigation documentation.

## Environment

- Host OS: Windows 11
- Linux Environment: Ubuntu 24.04 (WSL2)
- SIEM Platform: Wazuh 4.14.10
- Deployment: Docker Single-Node Environment

**Note:** This project was conducted in a controlled cybersecurity lab environment.
