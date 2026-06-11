# VPN Troubleshooting Ticket Example

## Ticket Summary

**Issue Type:** Remote Access  
**Category:** VPN / Network Connectivity  
**Priority:** Medium  
**Status:** Resolved  
**Affected User:** Remote User  
**System:** VPN Client / Company Network  

## Scenario

A remote user reported that they were unable to connect to the company VPN. The VPN client displayed a connection failure message after the user entered their credentials.

## User Impact

The user could not access internal resources, shared drives, or company applications that require VPN connectivity.

## Initial Questions Asked

- Are you connected to the internet?
- Are you using home Wi-Fi, mobile hotspot, or public Wi-Fi?
- What error message appears in the VPN client?
- Did the issue start today or has it happened before?
- Can you sign in to Microsoft 365 or other cloud services?
- Have you recently changed your password?

## Troubleshooting Steps

1. Confirmed the user had working internet access.
2. Verified that the user could access external websites.
3. Confirmed the VPN username and sign-in format.
4. Checked whether the user's password had recently changed.
5. Asked the user to restart the VPN client.
6. Confirmed that the VPN client was up to date.
7. Asked the user to restart the workstation.
8. Tested VPN connection again.
9. Verified that multi-factor authentication was completed successfully.
10. Confirmed that internal resources were accessible after connection.

## Root Cause

The VPN client was not completing authentication properly after the user's recent password change.

## Resolution

The user restarted the VPN client, signed in with the updated password, completed MFA, and successfully connected to the VPN.

## User Communication

The user was advised to use their most recent password when connecting to VPN and to restart the VPN client after password changes. The user was also reminded to complete MFA prompts quickly to avoid connection timeout.

## Escalation Notes

No escalation was required. If the issue continued, the next step would be to review VPN logs, confirm account permissions, and escalate to network administration.

## Skills Demonstrated

- VPN troubleshooting
- Remote support
- Network connectivity checks
- Authentication troubleshooting
- MFA awareness
- User-focused communication
