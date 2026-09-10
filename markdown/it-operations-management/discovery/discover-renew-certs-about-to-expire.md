---
title: Find and renew expiring certificates using the AI agent
description: Describe the certificates that you want to renew, and the certificate renewal AI agent finds them and renews them after you confirm.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/discover-renew-certs-about-to-expire.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certificate renewal AI agent, Automated certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Find and renew expiring certificates using the AI agent

Describe the certificates that you want to renew, and the certificate renewal AI agent finds them and renews them after you confirm.

## Before you begin

Configure your system for certificate renewal:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role required: sn\_disco\_certmgmt.pki\_admin

## About this task

You can describe certificates by any field on the Certificate \[cmdb\_ci\_certificate\] table using the field label as it appears in the record. For example, expiration date, assigned user, description, or thumbprint.

## Procedure

1.  Navigate to **Workspaces** &gt; **Certificate Management**.

2.  Select the ServiceNow Otto icon to open the AI panel.

3.  Describe the certificates that you want to renew.

    For example,`Renew all certificates expiring in the next 5 days`, `Renew the certificates assigned to me that expire before 1 August 2026`, or `Show me certificates expiring between 1 May 2026 and 1 August 2026`.

4.  Review the list of certificates that the agent returns.

5.  Confirm the renewal.


## Result

The agent creates a renewal task for each certificate and returns links to the task records. If no certificates match your description, the agent tells you that none were found.

