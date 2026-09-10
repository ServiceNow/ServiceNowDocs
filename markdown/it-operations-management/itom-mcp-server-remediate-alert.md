---
title: Remediate alerts with an MCP Client
description: Get and execute an alert remediation workflow or suggestion through an MCP Client.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-remediate-alert.html
release: australia
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 1
keywords: [alert remediation, ITOM MCP Server, AI agent]
breadcrumb: [Alert remediation, Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Remediate alerts with an MCP Client

Get and execute an alert remediation workflow or suggestion through an MCP Client.

## Before you begin

Verify that:

-   The ITOM MCP Server Console is active on your ServiceNow instance.
-   Your MCP Client application is connected to the ITOM MCP Server Console with valid OAuth credentials.
-   The AI Specialist worker has already investigated the alert you want to remediate.

    The Alert remediation tool returns a remediation recommendation only for alerts that the AI Specialist worker has investigated. If the worker isn't active for the alert, the tool reports that no remediation is available yet. For more information about the AI Specialist, see .


**Important:** The Alert remediation tool provides suggestions through an AI agent or MCP Client. You're interacting with AI. AI-generated responses may be inaccurate or incomplete.

For more information about the Alert remediation tool, see [Alert remediation with an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-mcp-server-alert-remediation.md).

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Open your MCP Client application.

2.  Ask the MCP Client how to handle a specified alert, using natural language.

    Either the recommended remediation workflow for the alert is returned, or if none is available, a remediation suggestion is returned.

3.  Confirm whether to execute or dismiss the recommendation.

    If you confirm, the remediation is executed.

4.  If the remediation fails to execute, confirm whether to proceed with the fallback action.

    For example, creating an incident.


