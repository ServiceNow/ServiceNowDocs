---
title: Use the ITOM MCP server
description: Connect an AI-enabled MCP client application to your ServiceNow environment using the ITOM MCP Server to investigate alerts, review configuration item \(CI\) reliability, assess incident impact, and create service level objectives \(SLOs\).
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2026-04-23"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Now Assist for ITOM, IT Operations Management]
---

# Use the ITOM MCP server

Connect an AI-enabled MCP client application to your ServiceNow environment using the ITOM MCP Server to investigate alerts, review configuration item \(CI\) reliability, assess incident impact, and create service level objectives \(SLOs\).

## ITOM MCP Server overview

The ITOM MCP Server bridges your ServiceNow ITOM environment to any AI-enabled MCP client, also referred to as MCP client, such as Moveworks, or Claude. When agents use an MCP client to ask questions about alerts or CIs, the ITOM MCP server fetches data from the ServiceNow ITOM environment and performs actions on behalf of the agent—all through natural language conversation.

The server supports these core capabilities for alert investigation and CI reliability:

-   Retrieves a list of alerts based on parameters such as time frame, state, assignment, or severity.
-   Retrieves alert details based on the alert number.
-   Investigates, analyzes, and assesses potential impact of an alert.
-   Reviews the reliability status of a CI, including related incidents, alerts, and SLOs.
-   Reviews the reliability topology of a CI across upstream and downstream dependencies.
-   Creates a standard availability SLO for a CI that doesn't already have one.

## ITOM MCP Server users

|Users|Description|
|-----|-----------|
|**IT administrators**|Activate the ITOM MCP Server.|
|**IT operators**|Use the ITOM MCP Server to investigate alerts, review CI reliability, assess incident impact on reliability, and create SLOs from an MCP client application without switching between windows. Ask questions through the MCP client application and request actions directly in the chat.|

## How the server works

The ITOM MCP Server operates as a secure intermediary between any MCP client application and the ServiceNow instance:

1.  An agent opens their MCP client application such as Moveworks or Claude and asks a question about an alert.
2.  The MCP client application sends the question to the ITOM MCP Server using the Model Context Protocol.
3.  The ITOM MCP Server authenticates the user against ServiceNow's role-based access control.
4.  The ITOM MCP Server retrieves the requested data or performs the requested action in the ServiceNow instance.
5.  The ITOM MCP Server returns the result to the AI client application, which displays it to the agent.

