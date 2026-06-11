# Active Directory Password Reset Notes

## Overview

This document summarizes basic Active Directory password reset concepts and support steps. It is intended for IT support, service desk, and desktop support portfolio documentation.

## Common Password-Related Issues

- User forgot password
- Account locked after failed login attempts
- Password expired
- User cannot sign in after password change
- VPN not accepting updated password
- Cached credentials issue
- User entering incorrect username format

## Password Reset Workflow

1. Verify the user's identity according to company policy.
2. Confirm the username or email address.
3. Locate the user account in Active Directory or the approved admin portal.
4. Check whether the account is locked.
5. Unlock the account if required.
6. Reset the password using a temporary password.
7. Select the option requiring the user to change password at next login, if required by policy.
8. Ask the user to sign in and create a new password.
9. Confirm access to required systems.
10. Document the ticket.

## Account Lockout Checks

When a user is locked out, check:

- Number of failed login attempts
- Recent password change
- Old password saved on phone, Outlook, Wi-Fi, or VPN
- Mapped drives using old credentials
- Remote desktop sessions
- Mobile email apps repeatedly trying old credentials

## Best Practices

- Never ask users to share their password.
- Confirm identity before resetting passwords.
- Use temporary passwords only when required.
- Encourage users to create strong passwords.
- Follow company password policy.
- Document all actions in the ticket.
- Escalate repeated lockouts for deeper investigation.

## Example Ticket Note

User reported being unable to sign in after several failed attempts. Identity was verified. Account was found locked in Active Directory. Account was unlocked and a temporary password reset was completed. User changed password successfully and confirmed access to Microsoft 365 and workstation login.

## Escalation Triggers

Escalate the issue if:

- The account locks repeatedly
- Suspicious login activity is detected
- The user reports unfamiliar MFA prompts
- Multiple users are affected
- The account appears disabled or permission changes are required

## Skills Demonstrated

- Active Directory basics
- Account lockout troubleshooting
- Password reset process
- Security awareness
- User verification
- Technical documentation
