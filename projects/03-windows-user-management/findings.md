# Findings

### Project Overview
This document summarizes account management and access control observations from Windows 11 ARM virtual lab running in UTM on a MacBook Air M4. 
The findings focus on privileged access, account lifecycle management, and the principle of least privilege.

## Finding 01 - Privileged Account Management
### Observation
ITAdmin was assigned administrator privileges.

### Security Impact
Administrator accounts have increased access and should be limited to authorized users. If an administrative account is compromised, an attacker may gain greater control over the system.

### Recommendation
Limit administrator group membership to authorized users. Use separate standard and administrative accounts when practical, and review privileged group regularly. 

---

## Findings 02 - Disabled User Accounts

### Observation
The Intern account was disabled.

### Security Impact
Disabled accounts that are no longer needed helps prevent those accounts from being used to access the system.

### Recommendation
Disable accounts when access is no longer required. Periodically review inactive accounts and follow established retention policies before deleting accounts. 

---

## Findings 03 - Standard User Permissions

### Observation
Employee1 remained a standard user account rather than being assigned local administrator privileges.

### Security Impact
Standard user accounts generally have fewer privileges than administrators, which can help limit the potential impact of a compromised account.

### Recommendation
Apply the principle of least privilege by granting users only the access necessary for their responsibilities. Review group membership and resource permissions periodically. 
