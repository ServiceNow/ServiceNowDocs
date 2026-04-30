---
title: Use Now Assist to renew a certificate set to renew manually
description: Use the Now Assist certificate renewal AI agent to immediately renew certificates set to renew manually.
locale: en-US
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-09-18"
reading_time_minutes: 1
breadcrumb: [Now Assist certificate renewal AI agent, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Use Now Assist to renew a certificate set to renew manually

Use the Now Assist certificate renewal AI agent to immediately renew certificates set to renew manually.

## Before you begin

Complete the following steps to configure your system for the Now Assist certificate renewal AI agent:

1.  [Configure your MID Server for automatic certificate renewal](configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](add-req-apps-capabilities-to-mid-server.md)

[Role masking](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) enables users to limit the roles and privileges of AI agents during tool execution. AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://www.servicenow.com/docs/access?context=define-sec-controls-aia&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

Role required: sn\_disco\_certmgmt.pki\_admin

## About this task

Find tasks that require you to renew your certificates manually and renew them immediately using the Now Assist AI certificate renewal agent.

## Procedure

1.  Navigate to **Workspaces** &gt; **Certificate Management**.

2.  Select **Tasks**.

3.  In the **Renewal Tasks** space, select the number of renewal tasks.

4.  Select the number of the renewal task that you want to auto-renew.

5.  In the **Unique Certificate** field, select the search icon ![](../../service-operations-workspace-itom/image/icon-information-1.png).

    **Note:** Selecting the icon opens the certificate record.

6.  Select your Now Assist AI tool.

7.  In the prompt field of Now Assist, enter `Renew this certificate`.

8.  Answer the questions that Now Assist asks you.


## Result

The certificate is renewed by the Now Assist AI certificate renewal agent.

**Parent Topic:**[Now Assist certificate renewal AI agent](../../it-operations-management/concept/now-assist-cert-renewal-ai-agent.md)

