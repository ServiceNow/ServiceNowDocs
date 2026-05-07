---
title: Analyze alerts using the ITOM MCP Server with MCP client applications
description: Use the ITOM MCP Server to analyze and investigate alerts through an MCP client application such as Moveworks or Claude.
locale: en-US
release: australia
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2026-04-27"
reading_time_minutes: 1
keywords: [ITOM MCP Server, natural language prompts, AI workflow]
breadcrumb: [Use the ITOM MCP Server, Now Assist for ITOM, IT Operations Management]
---

# Analyze alerts using the ITOM MCP Server with MCP client applications

Use the ITOM MCP Server to analyze and investigate alerts through an MCP client application such as Moveworks or Claude.

## About this task

The ITOM MCP Server allows you to analyze and investigate alerts through MCP client applications connected to your ServiceNow instance. You can ask the AI client applications questions about alerts. The MCP tools retrieve data from your ServiceNow instance and perform actions on your behalf.

The following tools are available to investigate and analyze alerts.

<table id="table_wqr_nkm_bjc"><thead><tr><th>

Tools

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List Alert Record

</td><td>

Provides a list of alert records using parameters provided in the search query.**Note:** Alert record lists are limited to the first 50 alerts.

</td></tr><tr><td>

Alert Analysis

</td><td>

Provides a summary and analysis of an alert identified by the alert number.

</td></tr><tr><td>

Alert Investigation

</td><td>

Delivers insights from historical incidents and past resolutions, to aid in alert investigation.

</td></tr><tr><td>

Alert Impact Analysis

</td><td>

Delivers insights from related incidents, cases, and affected services.

</td></tr><tr><td>

Alert Hypothesizer

</td><td>

Presents potential impact of an alert by analyzing alert context and relevant information.**Note:** This tool is available for Health Log Analytics \(HLA\) alerts only.

</td></tr></tbody>
</table>## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator

## Procedure

1.  Open your MCP client application such as Claude, that is connected to your ServiceNow instance using the ITOM MCP Server.

    Your system administrator configures this integration during setup.

2.  Ask the AI tool a question about an incident.

    Use natural language to ask questions. Here are common types of prompts:

    -   **Retrieve a list of alerts for today:** "List alerts created today."
    -   **List only critical alerts:** "List only the critical alerts created today."
    -   **Analyze and investigate the alerts:** "Analyze and investigate the alerts."

        **Note:** Information returned through alert analysis may include several lines of text per alert.

    -   **Analyze a specific alert:** "Analyze Alert 00100032."
3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


