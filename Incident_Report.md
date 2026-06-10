# SOC Incident Investigation Report

## Incident Title

Investigation of Multiple Failed Logins and User Account Creation

## Incident Summary

A security investigation was conducted using Splunk SIEM on the Windows host DESKTOP-KMMVJUP. Multiple failed login attempts were detected against the account "hacker". Following these authentication failures, successful logon events were observed. Additional investigation revealed user account creation activity on the same host.

## Affected Host

DESKTOP-KMMVJUP

## Investigation Findings

### Failed Login Activity (Event ID 4625)

A total of 8 failed login attempts were identified for the account "hacker".

### Successful Login Activity (Event ID 4624)

Multiple successful logon events were observed on the affected host after authentication activity.

### User Account Creation (Event ID 4720)

Three user account creation events were detected on the affected host.

### Process Activity

Event monitoring identified process-related activity on the Windows system during the investigation period.

## Incident Timeline

10:59:37 - Failed Login Detected

11:02:13 - Failed Login Detected

11:02:25 - Failed Login Detected

13:49:56 - User Account Creation Detected

14:05:36 - User Account Creation Detected

14:11:40 - User Account Creation Detected

19:34:16 - Failed Login Detected

19:34:41 - Failed Login Detected

20:02:02 - Successful Login Detected

20:07:23 - Successful Login Detected

## Indicators of Compromise (IOC)

* Event ID 4625 (Failed Login Attempts)
* Event ID 4624 (Successful Logon Events)
* Event ID 4720 (User Account Creation)
* Username: hacker
* Host: DESKTOP-KMMVJUP

## Root Cause

The activity indicates repeated authentication failures against a user account followed by successful authentication and account management activity. This behavior is consistent with password guessing, brute-force attempts, or unauthorized access testing performed in a lab environment.

## Mitigation Recommendations

* Enable Multi-Factor Authentication (MFA)
* Enforce strong password policies
* Monitor Event IDs 4624, 4625, and 4720
* Configure real-time SIEM alerts
* Review newly created user accounts regularly
* Restrict administrative privileges where possible

## Conclusion

The investigation successfully identified authentication-related events and account management activity using Splunk SIEM. Event correlation, timeline creation, and IOC identification were performed to understand the sequence of activity and improve monitoring capabilities.
