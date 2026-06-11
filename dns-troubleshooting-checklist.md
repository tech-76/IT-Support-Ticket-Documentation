# DNS Troubleshooting Checklist

## Overview

This checklist provides a structured approach to troubleshooting common DNS-related issues. DNS problems can affect websites, email delivery, VPN access, internal applications, and cloud services.

## Common DNS Issues

- Website not loading
- Domain pointing to the wrong server
- Email not sending or receiving
- New DNS changes not working yet
- SSL certificate validation issues
- Incorrect MX records
- Incorrect A record or CNAME record
- DNS propagation delays

## Initial Questions

- What domain or hostname is affected?
- When did the issue start?
- Was a DNS change recently made?
- Is the issue affecting one user or everyone?
- Is the problem related to website access, email, or another service?
- What error message appears?

## Basic DNS Record Types

| Record Type | Purpose |
|---|---|
| A Record | Points a domain or subdomain to an IPv4 address |
| AAAA Record | Points a domain or subdomain to an IPv6 address |
| CNAME | Points one hostname to another hostname |
| MX Record | Directs email to the correct mail server |
| TXT Record | Used for SPF, DKIM, DMARC, and verification records |
| NS Record | Identifies authoritative name servers |

## Troubleshooting Steps

1. Confirm the correct domain name.
2. Check whether the domain is active and not expired.
3. Confirm the authoritative name servers.
4. Review recent DNS changes.
5. Check the A record for website hosting.
6. Check the CNAME record for subdomains.
7. Check MX records for email routing.
8. Check TXT records for SPF, DKIM, or DMARC.
9. Test the domain from another network or device.
10. Allow time for DNS propagation if changes were recently made.
11. Document findings and next steps.

## Website DNS Checklist

- Domain is registered and active
- Name servers are correct
- A record points to the correct hosting IP
- CNAME records are configured correctly
- SSL certificate matches the domain
- No duplicate or conflicting records exist

## Email DNS Checklist

- MX records point to the correct email provider
- SPF record includes approved sending services
- DKIM is enabled if supported
- DMARC record is configured if required
- No conflicting TXT records exist
- Mailbox exists and is licensed if using Microsoft 365 or Google Workspace

## Escalation Triggers

Escalate if:

- DNS records are correct but the service still fails
- Name server changes are required
- The domain appears expired or suspended
- Email authentication failures continue
- Multiple services are affected

## Skills Demonstrated

- DNS troubleshooting
- Domain support
- Email routing basics
- Web hosting support
- Technical checklist documentation
