---
title: Use AI to renew certificate set to renew manually
description: Use the certificate renewal AI agent to immediately renew certificates set to renew manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/renew-cert-set-to-renew-manually.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certificate renewal AI agent, Use agentic AI, ServiceNow Otto for ITOM, IT Operations Management]
---

# Use AI to renew certificate set to renew manually

Use the certificate renewal AI agent to immediately renew certificates set to renew manually.

## Before you begin

Complete the following steps to configure your system for the certificate renewal AI agent:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role required: sn\_disco\_certmgmt.pki\_admin

## About this task

Find tasks that require you to renew your certificates manually and renew them immediately using the AI certificate renewal agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **Certificate Management**.

2.  Select **Tasks**.

3.  In the **Renewal Tasks** space, select the number of renewal tasks.

4.  Select the number of the renewal task that you want to auto-renew.

5.  In the **Unique Certificate** field, select the Search icon \[Omitted image "icon-information-1.png"\] Alt text:.

    **Note:** Selecting the icon opens the certificate record.

6.  Select your AI tool.

7.  In the prompt field, enter `Renew this certificate`.

8.  Answer the prompts.


## Result

The certificate is renewed by the AI certificate renewal agent.

**Parent Topic:**[Certificate renewal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-cert-renewal-ai-agent.md)

