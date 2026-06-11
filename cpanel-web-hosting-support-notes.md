# cPanel Web Hosting Support Notes

## Overview

This document outlines basic cPanel web hosting support tasks and troubleshooting steps. It is designed for IT support, technical support, and web hosting support portfolio use.

## Common cPanel Support Areas

- Uploading website files
- Managing public_html
- Creating email accounts
- Managing domains and subdomains
- Checking SSL certificate status
- Reviewing file permissions
- Managing backups
- Troubleshooting contact forms
- Checking disk usage
- Reviewing error pages

## Website Upload Checklist

1. Log in to cPanel.
2. Open File Manager.
3. Navigate to `public_html`.
4. Upload website files.
5. Confirm the homepage file is named `index.html`, `index.php`, or another supported index file.
6. Extract ZIP files if needed.
7. Confirm file paths are correct.
8. Test the website in a browser.
9. Check mobile and desktop display.
10. Confirm images, CSS, JavaScript, and forms load correctly.

## Common Website Issues

### Issue: Website shows a directory listing

**Possible Cause:** Missing index file.

**Resolution:** Upload or rename the homepage file to `index.html` or `index.php`.

### Issue: Website shows a 404 error

**Possible Causes:**

- File path is incorrect
- Page was deleted or renamed
- Link points to the wrong location

**Resolution:** Confirm file names, folder paths, and links.

### Issue: Website design looks broken

**Possible Causes:**

- CSS file missing
- Incorrect file path
- Assets not uploaded
- Browser cache issue

**Resolution:** Confirm CSS and asset folders are uploaded correctly.

## Email Support in cPanel

Common tasks include:

- Creating email accounts
- Resetting email passwords
- Checking mailbox storage
- Confirming incoming and outgoing server settings
- Reviewing SMTP authentication
- Testing webmail access

## SSL Troubleshooting

Check the following:

- SSL certificate is active
- Domain points to the hosting account
- HTTPS redirects are configured correctly
- Certificate matches the correct domain
- Mixed content is not blocking secure page loading

## Contact Form Troubleshooting

Possible causes of form issues:

- Incorrect recipient email
- Missing mail configuration
- SMTP authentication not configured
- Hosting provider mail restrictions
- Form script errors
- DNS/SPF issues

## Escalation Triggers

Escalate if:

- Hosting server errors continue
- SSL cannot be issued
- Malware or suspicious files are detected
- Email delivery failures continue after DNS checks
- File permission changes require administrator approval

## Skills Demonstrated

- cPanel basics
- Website upload support
- Hosting troubleshooting
- SSL support
- Email account support
- Contact form troubleshooting
- Technical documentation
