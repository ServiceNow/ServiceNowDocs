---
title: Review CI reliability with the ITOM MCP Server
description: Use the ITOM MCP Server to review configuration item \(CI\) reliability and topology, assess incident impact on reliability, and create service level objectives \(SLOs\).
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use the ITOM MCP Server, Now Assist for ITOM, IT Operations Management]
---

# Review CI reliability with the ITOM MCP Server

Use the ITOM MCP Server to review configuration item \(CI\) reliability and topology, assess incident impact on reliability, and create service level objectives \(SLOs\).

## About this task

Use an MCP client application, such as Moveworks or Claude, with the ITOM MCP Server to review CI reliability information, assess incident impact, and create SLOs. The following MCP tools retrieve information from your ServiceNow instance and, in some cases, perform actions.

|Tool|Description|
|----|-----------|
|CMDB CI Reliability Status|Review the current reliability status of a CI, including active SLOs, related incidents and alerts, and affected dependent CIs.|
|CMDB CI Reliability Topology|Review the reliability topology of CI across upstream and downstream dependencies.|
|Create SLO for CMDB CI|Create a standard availability SLO for a CI that doesn't already have one.|
|Incident linked CI reliability|Review the reliability impact of an incident on a linked CI, including related alerts and impacted SLOs.|

## Before you begin

Verify that the ITOM MCP Server is active and the required plugins are installed on your instance. For more information, see [Activate the ITOM MCP server](activate-itom-mcp-server.md).

Role required: sn\_sow\_slo.slo\_operator

## Procedure

1.  Open your MCP client application, such as Claude.

2.  In the MCP client application, ask a question or request an action for a CI.

    The following are common types of prompts:

    -   **Review the reliability impact of an incident:** "What is the reliability impact of incident INC0010217?"
    -   **Review CI reliability status:** "Show the reliability status of Customer Portal Service."
    -   **Review CI reliability topology:** "Show the reliability topology of Customer Portal Service. I want to understand whether other CIs are affected."
    -   **Create an SLO for a CI:** "Create an SLO for Auth Service."
3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data that you can access.


## What to do next

If you created an SLO, you can learn more about SLOs, including SLO types and compliance periods, in [Working with reliability metrics](../../slo-management/concept/sr-work-SLI-SLO.md). To edit or deactivate an SLO, see [Edit a reliability metric](../../slo-management/task/sr-edit-sli-slo.md).

