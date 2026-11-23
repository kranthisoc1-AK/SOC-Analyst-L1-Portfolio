# Splunk – Brute Force Attack Detection

## Project Overview

This project focuses on detecting potential brute-force login attempts using Splunk SIEM. Windows Security Event Logs were collected and analysed to identify repeated failed authentication attempts.

The project demonstrates how SIEM tools can be used for security monitoring, log analysis, alert creation, and dashboard development.

## Objectives

- Configure Windows Security Event Log collection in Splunk.
- Monitor failed login attempts.
- Identify suspicious authentication activities.
- Create a brute-force detection alert.
- Develop a dashboard for security monitoring.
- Understand SIEM-based threat detection.

## Tools & Technologies

- Splunk Enterprise
- Windows 11
- Windows Security Event Logs
- Splunk Search Processing Language (SPL)

## Implementation Activities

### 1. Splunk Installation and Configuration

- Installed and configured Splunk Enterprise.
- Accessed the Splunk Web Interface.
- Configured Windows Event Log collection.

### 2. Windows Event Log Collection

- Configured System and Security event log inputs.
- Collected Windows Security events.
- Analysed authentication-related activities.

### 3. Brute Force Detection

- Investigated failed login events.
- Used Splunk searches to identify repeated authentication failures.
- Created a scheduled alert named Brute Force Attack Alert.
- Configured the alert with High severity.

### 4. Dashboard Development

- Created a dashboard titled Brute Force Attack Detection.
- Added visualizations for monitoring authentication-related events.
- Used dashboard results to support security investigations.

## SPL Queries

### 1. Search for Failed Login Attempts

Identifies Windows failed login events using Event ID 4625.

```spl
index=main sourcetype="WinEventLog:Security" EventCode=4625
| table _time host EventCode Message
| sort - _time
```

### 2. Count Failed Login Attempts

Counts failed login events grouped by host.

```spl
index=main sourcetype="WinEventLog:Security" EventCode=4625
| stats count AS Failed_Login_Attempts by host
| sort - Failed_Login_Attempts
```

### 3. Detect Potential Brute Force Activity

Identifies hosts with 5 or more failed login events.

```spl
index=main sourcetype="WinEventLog:Security" EventCode=4625
| bin _time span=5m
| stats count AS Failed_Attempts by host _time
| where Failed_Attempts >= 5
| sort - Failed_Attempts
```

**Note:** These are example detection searches. Adjust the index and field names if your Splunk environment uses different values. The threshold of 5 is an example detection threshold, not a confirmed threshold from your original alert configuration.

## Key Findings

- Successfully collected Windows Security Event Logs.
- Identified failed login events.
- Created a scheduled brute-force detection alert.
- Developed a security monitoring dashboard.
- Observed alert execution results during testing.

## Skills Demonstrated

- SIEM Configuration
- Log Collection and Analysis
- Splunk SPL
- Brute Force Detection
- Security Alert Configuration
- Dashboard Development
- Windows Event Log Monitoring

## Project Evidence

Refer to the Screenshots folder for Splunk configuration, search results, alert settings, and dashboard evidence.

## Project Report

See `Brute_Force_Attack_Detection_Report.pdf` for detailed project documentation.

## Environment

Windows 11 – Local SOC Lab Environment.

**Note:** This project was conducted in a controlled learning environment for cybersecurity training.
