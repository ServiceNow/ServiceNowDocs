---
title: Alert investigation with an AI client
description: Investigate alerts using the ITOM MCP Server Console with an MCP Client application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-mcp-server-alert-investigation.html
release: australia
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 1
keywords: [ITOM MCP Server, investigate, analyze, alert, natural language prompts, AI workflow]
breadcrumb: [Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Alert investigation with an AI client

Investigate alerts using the ITOM MCP Server Console with an MCP Client application.

The ITOMMCP Server Console enables you to analyze and investigate alerts using an MCP Client application, such as Moveworks or AWS Claude, connected to your ServiceNow instance. You can ask the AI client application questions about alerts through natural language prompts. MCP tools retrieve data from your ServiceNow instance and perform actions on your behalf.

The following tools are available to investigate alerts.

<table><thead><tr><th>

Tools

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List Alert Record

</td><td>

Provides a list of alert records using parameters provided in the search query.**Note:** Alert record lists are limited to the first 50 alerts.

</td></tr><tr><td>

Alert Investigation

</td><td>

Checks for existing AI-generated investigation results for the alert and returns them if available. If no results exist, triggers the alert investigation pipeline in the background and returns a processing status until results are ready. This tool consolidates three separate tools: Alert Investigation, Alert Analysis, and Alert Impact Analysis.

</td></tr></tbody>
</table>