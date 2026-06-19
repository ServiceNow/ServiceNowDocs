---
title: Automatically renew a certificate using the Now Assist certificate renewal AI agent
description: Automatically renew a single certificate using the Now Assist certificate renewal AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/automatically-renew-cert-now-assist.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-09-16"
reading_time_minutes: 1
breadcrumb: [Now Assist certificate renewal AI agent, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Automatically renew a certificate using the Now Assist certificate renewal AI agent

Automatically renew a single certificate using the Now Assist certificate renewal AI agent.

## Before you begin

Complete the following steps to configure your system for the Now Assist certificate renewal AI agent:

1.  [Configure your MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role masking enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an AI agent.

Role required: sn\_disco\_certmgmt.pki\_admin

## About this task

Navigate to the certificate that you want to renew and use the Now Assist certificate renewal AI agent to renew the certificate.

## Procedure

1.  Navigate to **All** &gt; **Unique Certificates**.

2.  Select the certificate that you want to renew.

3.  Select the Now Assist icon \[Omitted image "wwna-icon.png"\] Alt text:.

    **Warning:** Make sure that you are on the unique certificate page of the certificate that you want to renew.

4.  Enter the prompt `Renew this certificate`

5.  Answer the questions that Now Assist asks you.


## Result

Now Assist updates you on its progress in renewing your certificate. The certificate renewal AI agent gives you a link to the task record that displays the status of the renewed certificate.

**Parent Topic:**[Now Assist certificate renewal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-cert-renewal-ai-agent.md)

