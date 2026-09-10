---
title: Using the ITOM MCP Server Console to perform ITOM tasks
description: Connect an AI-enabled MCP Client application to your ServiceNow environment using the ITOM MCP Server Console. Use the MCP Client to investigate alerts, review configuration item \(CI\) reliability, assess incident impact, and create service level objectives \(SLOs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/use-itom-mcp-server.html
release: australia
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [AI in ITOM, IT Operations Management]
---

# Using the ITOM MCP Server Console to perform ITOM tasks

Connect an AI-enabled MCP Client application to your ServiceNow environment using the ITOM MCP Server Console. Use the MCP Client to investigate alerts, review configuration item \(CI\) reliability, assess incident impact, and create service level objectives \(SLOs\).

## ITOM MCP Server Console overview

The ITOM MCP Server Console bridges your ServiceNow ITOM environment to any AI-enabled MCP Client, such as Moveworks or AWS Claude. When agents use an MCP Client to ask questions about alerts or CIs, the ITOM MCP Server Console fetches data from the ServiceNow ITOM environment. It performs actions on behalf of the agent through natural language conversation.

The ITOM MCP Server Console supports these core capabilities for alert investigation and CI reliability:

-   Retrieves a list of alerts based on parameters such as time frame, state, assignment, or severity.
-   Retrieves alert details based on the alert number.
-   Investigates, analyzes, and assesses potential impact of an alert.
-   Performs actions on alerts: assign, close, reopen, acknowledge, and add work notes or comments. Supports single-alert and bulk operations.
-   Reviews the reliability status of a CI, including related incidents, alerts, and SLOs.
-   Reviews the reliability topology of a CI across upstream and downstream dependencies.
-   Creates a standard availability SLO for a CI that doesn't already have one.

The ITOM MCP Server Console includes AIOps, SRM, and LEAP tools. For details on LEAP tools, see [LEAP MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/aiops-leap-mcp-server-overview.md).

## ITOM MCP Server users

|Users|Description|
|-----|-----------|
|**IT administrators**|Activate the ITOM MCP Server Console.|
|**IT operators**|Use the ITOM MCP Server Console to investigate alerts, review CI reliability, assess incident impact on reliability, and create SLOs from an MCP Client application without switching between windows. Ask questions through the MCP Client application and request actions directly in the chat. Perform alert actions such as assign, close, reopen, and acknowledge on single alerts or alert groups.|

## How the ITOM MCP Server Console works

The ITOM MCP Server Console operates as a secure intermediary between any MCP Client application and the ServiceNow instance:

1.  An agent opens their MCP Client application and asks a question about an alert.
2.  The MCP Client application sends the question to the ITOM MCP Server Console using the Model Context Protocol \(MCP\).
3.  The ITOM MCP Server Console authenticates the user against ServiceNow role-based access control.
4.  The ITOM MCP Server Console retrieves the requested data or performs the requested action in the ServiceNow instance.
5.  The ITOM MCP Server Console returns the result to the AI client application, which displays it to the agent.

