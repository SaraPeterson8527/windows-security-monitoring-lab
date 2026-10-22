# Investigation 01: Failed Windows Logon

## Overview

- Event ID: 4625
- Log Source: Windows Security
- Observed Date/Time: October 22, 2026, approximately 1:30pm
- Account Name: LabUser
- Logon Type: 2 - Interactive
- Process Name: msedge.exe

## Evidence

The Windows Security log contained an Event ID 4625, which records a failed logon attempt.

The event showed the following details:

- Failed Reason: Unknown user name
- Status: 0xC000006D
- SubStatus: 0xC000006A
- Process Name: msedge.exe

The status code indicate a general logon failed and an incorrect-password substatus. However, the displayed failure reason appears inconsistent with the substatus, so the exact cause has not been conclusively established.

## Analysis

The event records a failed interactive logon involving the account name LabUser. The process information references Microsoft Edge (msedge.exe).

The available evidence does not establish why the logon attempt occurred or whether it was malicious. The process name alone does not prove that Microsoft Edge initiated an authorized sign-in.

## Conclusion

A failed logon was recorded, but its cause and context remain unconfirmed. Additional review of nearby events and the full event details would be needed before determining whether this was ordinary activity or a potential security concern.
