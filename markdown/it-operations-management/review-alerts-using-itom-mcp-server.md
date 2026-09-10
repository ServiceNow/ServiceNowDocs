---
title: Investigate alerts using an MCP Client
description: Use the ITOM MCP Server Console to investigate alerts through an MCP Client application, such as Moveworks or AWS Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/review-alerts-using-itom-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [ITOM MCP Server, natural language prompts, AI workflow]
breadcrumb: [Alert investigation, Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Investigate alerts using an MCP Client

Use the ITOM MCP Server Console to investigate alerts through an MCP Client application, such as Moveworks or AWS Claude.

## Before you begin

For more information about the Alert Investigation tool, see.

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## Procedure

1.  Open your MCP Client application, such as AWS Claude, that is connected to your ServiceNow instance using the ITOM MCP Server Console.

    Your system administrator configures this integration during setup.

2.  Ask the AI tool a question about an incident.

    Use natural language to ask questions. Here are common types of prompts:

    -   Retrieve a list of alerts for today: "List alerts created today."
    -   List only critical alerts: "List only the critical alerts created today."
    -   Analyze and investigate the alerts: "Analyze and investigate the alerts."

        **Note:** Information returned through alert analysis may include several lines of text per alert.

    -   Analyze a specific alert: "Analyze Alert 00100032."
3.  Review the MCP Client application response.

    The MCP Client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


