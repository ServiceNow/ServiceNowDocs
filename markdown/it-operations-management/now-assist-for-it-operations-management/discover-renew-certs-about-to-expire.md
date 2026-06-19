---
title: Discover and renew certificates about to expire using Now Assist
description: Use Now Assist to find out which certificates expire on a certain date or within a certain date range. Now Assist produces a Unique Certificates list of these certificates and prompts you to renew them in a single click.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/now-assist-for-it-operations-management/discover-renew-certs-about-to-expire.html
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist certificate renewal AI agent, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Discover and renew certificates about to expire using Now Assist

Use Now Assist to find out which certificates expire on a certain date or within a certain date range. Now Assist produces a Unique Certificates list of these certificates and prompts you to renew them in a single click.

## Before you begin

Complete the following steps to configure your system for the Now Assist certificate renewal AI agent:

1.  [Configure the MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role required: sn\_disco\_certmgmt.pki\_admin

## Procedure

1.  Navigate to **All** &gt; **Unique Certificates**.

2.  Select the Now Assist icon \[Omitted image "wwna-icon.png"\] Alt text:.

3.  Enter `Fetch the certificates expiring between 1 May 2026 and 1 August 2026.`

    **Note:** You can choose any date range that you need.

4.  Select the **Certificates** link that Now Assist returns.


## Result

Now Assist directs you to a list of certificates that expire between 1 May 2026 and 1 August 2026. Now Assist then asks you if you want to renew these certificates. Renew them all at once by selecting **yes**.

