File Integrity Monitoring (FIM) – Wazuh

Objective: Monitor important files and detect unauthorized modifications or deletions.

Environment:
- SIEM: Wazuh 4.14.10
- Endpoint: Windows 11
- Agent name: DESKTOP-L29HLL9
- Agent ID: 002
- Monitoring mode: Real-time

Configuration: Configured the Windows Wazuh agent to monitor the folder `C:\Users\DELL\Desktop\Wazuh-FIM-Test` using real-time file integrity monitoring.

Modification Detection:
- Modified a test file.
- Wazuh generated an integrity-change alert.
- Rule ID: 550
- Severity level: 7
- Detected changes in file size, modification time, MD5, SHA-1 and SHA-256 hashes.

**MITRE ATT&CK:** T1565.001 – Stored Data Manipulation.

**Result:** Successfully verified real-time file modification detection.

**Deletion Detection:** Pending confirmation of the deletion alert.