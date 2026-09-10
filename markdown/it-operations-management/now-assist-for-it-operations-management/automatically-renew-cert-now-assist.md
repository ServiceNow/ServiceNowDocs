---
title: Renew certificates using the AI agent
description: Renew a specific certificate by opening it and asking the certificate renewal AI agent to renew it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/automatically-renew-cert-now-assist.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certificate renewal AI agent, Use agentic AI, ServiceNow Otto for ITOM, IT Operations Management]
---

# Renew certificates using the AI agent

Renew a specific certificate by opening it and asking the certificate renewal AI agent to renew it.

## Before you begin

Configure your system for certificate renewal:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role required: sn\_disco\_certmgmt.pki\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Certificate Management**.

2.  Open the certificate that you want to renew.

3.  Select the ServiceNow Otto icon to open the AI panel.

    The agent identifies the certificate you're viewing and asks whether you want to renew it. Confirm that the certificate name in the agent's prompt matches the certificate you intend to renew before you continue.

4.  Confirm the renewal.


## Result

The agent creates a certificate renewal task and returns a link to the task record. Select the link to track the status of the renewal.

**Parent Topic:**[Certificate renewal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-cert-renewal-ai-agent.md)

