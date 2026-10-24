# Windows Logging Lab Findings

## Baseline Collection 

Date: October 22, 2026

Purpose: Establish a baseline of Windows logging activity before adding additional monitoring tools.

## System Information 
- Operating System: Windows 11
- Virtualization: UTM
- MacBook Air M4 
- Architecture: ARM64

## Event Viewer

### Security Logs
- The Security log contains Windows security-related events.
- Event ID 4624 was located, representing a successful logon.
- Event ID 4625 was located, representing a failed logon.
- One Event ID 4625 entry displayed the failure reason Unknown user name and Logon Type 2 (interactive logon).
- The cause of the failed logon has not yet been confirmed.  

### System Logs

#### Oberservation 1: Microsoft Edge Update Service Failure

- **Source:** Service Control Manager
- **Event ID:** 7000
- **Message:** Microsoft Edge Update service failed to respond to a start or control request in a timely fashion.

**Analysis:**
Windows reports that the Microsoft Edge Update service did not respond within the expected time. This may indicate a temporary service startup or responsiveness issue.

**Conclusion:**
The event alone does not establish a security incident. Additional context would be needed to determine whether the issue persisted.

#### Observation 2: LUAFV Service Failure

- **Source:** Service Control Manager
- **Event ID:** 7000
- **Service:** 'luafv'
- **Message:** The service failed to start because its driver was blocked from loading.

**Analysis:**
The 'luafv' component is associated with Windows UAC file virtualization. The event indicated a driver-loading problem, but the specific cause has not been confirmed.

**Conclusion:**
The event is documented for further review. It should not be classified as malicious without additional evidence.

### Application Logs
Observations: To be documented after reviewing the Application log.

## Notes
- Event Viewer was used to review Windows event logs.
- The audit policy was inspected using auditpol /get /category:*
- The Logon audit setting displayed Success and Failure.
- The Logoff audit setting displayed Success.
- The Account Logon audit setting displayed No Auditing.
- No audit policy changed have been made as part of baseline review. 
