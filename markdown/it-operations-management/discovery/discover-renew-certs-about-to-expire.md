---
title: Discover and renew certificates about to expire using AI
description: Use AI to find out which certificates expire on a certain date or within a certain date range. It produces a Unique Certificates list of these certificates and prompts you to renew them in a single click.
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

# Discover and renew certificates about to expire using AI

Use AI to find out which certificates expire on a certain date or within a certain date range. It produces a Unique Certificates list of these certificates and prompts you to renew them in a single click.

## Before you begin

Complete the following steps to configure your system for the certificate renewal AI agent:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role required: sn\_disco\_certmgmt.pki\_admin

## Procedure

1.  Navigate to **All** &gt; **Unique Certificates**.

2.  Select the ServiceNow Otto icon.

3.  Enter the date range for which you want the agent to fetch details.

    For example, `Fetch the certificates expiring between 1 May 2026 and 1 August 2026.`

4.  Select the **Certificates** link that the AI returns.


## Result

The AI displays a list of certificates that expire between the date range you specified \(in this example, 1 May 2026 and 1 August 2026\). It then asks if you want to renew these certificates. Renew them all at once by selecting **yes**.

