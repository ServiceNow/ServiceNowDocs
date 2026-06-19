---
title: Analyze alert impact in the Now Assist panel
description: Learn how to use the analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-use-aia.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Analyze alert impact agentic workflow, Use agentic AI, Now Assist for ITOM, IT Operations Management]
---

# Analyze alert impact in the Now Assist panel

Learn how to use the analyze alert impact agentic workflow in the Now Assist panel. The agentic workflow helps you investigate an alert and get the context that you need to respond efficiently.

## Before you begin

Make sure Now Assist for ITOM is installed and observability agents are configured for third-party vendors. For more information, see  and [Configure observability agents for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md).

Role masking enables users to limit the roles and privileges of agentic workflows during tool execution. Agentic workflows and their AI agents that get installed with Now Assist applications are assigned pre-defined roles. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. Data access settings must also include these roles. For the instructions to change the security controls, see Define security controls for an agentic workflow.

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \(\[Omitted image "express-list1.png"\] Alt text: Express list icon\).

3.  Select an alertfrom a source associated with an observability agent.

4.  Open the panel by selecting the Now Assist icon \(\[Omitted image "wwna-icon.png"\] Alt text: Now Assist icon.\).

5.  Ask a tool-specific question about the alert.

    For example, for New Relic alerts, you can ask `Have there been recent deployments for this alert?`. To better understand the type of data you can query, see the **Overview of data returned** row in the corresponding vendor's table in [Configure observability agents for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/configure-integration-agents-for-now-assist.md).

    Now Assist uses the relevant AI agents to analyze your question and respond with a summary or insight. The first response for an alert might take several seconds to appear.


## What to do next

Use the information that you received to understand the alert impact and respond accordingly. You can also ask more questions about the alert.

**Note:** Your conversation in the Now Assist panel is specific to the alert that you selected in Step 3. To ask about a different alert, open that alert and select the Now Assist icon \(\[Omitted image "wwna-icon.png"\] Alt text: Now Assist icon.\) to start a new conversation.

**Parent Topic:**[Analyze alert impact agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-agentic-aia.md)

