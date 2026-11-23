# Windows Security Event Monitoring – Wazuh

## Objective
Monitor Windows Security events using Wazuh SIEM and investigate account-related security activities.

## Environment
- SIEM Wazuh 4.14.10
- Endpoint Windows 11 Pro
- Agent DESKTOP-L29HLL9
- Agent ID 002

## Event IDs Investigated

 Event ID  Description 
------
 4624  Successful login 
 4625  Failed login 
 4740  Account locked out 
 4723  Password change attempt 
 4724  Password reset attempt 
 4725  User account disabled 
 4726  User account deleted 

## Investigation Process
1. Generated test Windows Security events.
2. Checked events in Windows Event Viewer.
3. Searched for corresponding events in Wazuh Threat Hunting.
4. Examined account names, event IDs, timestamps and available source information.
5. Identified events requiring further investigation.

## Conclusion
Configured Wazuh to collect Windows Security events and practised investigating authentication and user account management activities.

Note Record an event as detected in Wazuh only after confirming it appears in the dashboard. Windows Event Viewer confirmation alone does not prove Wazuh detection.

## Evidence
Add screenshots of verified events and their investigation details.
