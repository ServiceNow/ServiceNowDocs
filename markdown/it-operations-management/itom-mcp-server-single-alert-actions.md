---
title: Perform actions on single alerts from an MCP Client
description: Use the Alert Actions tool in an MCP Client to perform single-alert operations. For example, to assign, close, reopen, acknowledge, or annotate one alert at a time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-single-alert-actions.html
release: australia
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
breadcrumb: [Alert actions, Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Perform actions on single alerts from an MCP Client

Use the Alert Actions tool in an MCP Client to perform single-alert operations. For example, to assign, close, reopen, acknowledge, or annotate one alert at a time.

## Before you begin

Verify that:

-   The ITOM MCP Server Console is active on your ServiceNow instance.
-   Your MCP Client application is connected to the ITOM MCP Server Console with valid OAuth credentials.

**Important:** The Alert Actions tool acts on alerts through an AI agent or MCP Client. You're interacting with AI. AI-generated responses may be inaccurate or incomplete. Review the confirmation and the linked alert after each action to verify the result.

For more information about the Alert Actions tool, see [Alert actions with an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-mcp-server-alert-actions.md).

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

Individual alerts require targeted action based on investigation. For example, to investigate and close an alert:

1.  In the MCP Client application \(such as AWS Claude\), ask: "Analyze alert 00100032."

    The alert details and analysis are retrieved from ITOM.

2.  Review the analysis and determine the root cause.
3.  Ask: "Close alert 00100032 with this note: Root cause identified as disk space depletion on DB server. Applied automated cleanup job."

    You receive confirmation: "Alert 00100032 closed. Work note added."

4.  Select the provided link to verify in the ServiceNow UI.

## Procedure

1.  Open your MCP Client application.

2.  Ask the MCP Client to perform an action on an alert.

    Use natural language to describe the action. For example:

    -   "Assign alert 00100032 to the network team."
    -   "Close alert 00100032. Root cause was a transient DNS issue."
    -   "Reopen alert 00100032. The issue is recurring."
    -   "Acknowledge alert 00100032."
    -   "Add a note to alert 00100032: Investigated at 10:15 UTC. CPU load returned to normal."
3.  Review the response from your MCP Client.

    The response includes:

    -   Confirmation of the action performed.
    -   The updated alert state or field values.
    -   A deep link to the alert in ServiceNow for verification.
4.  Verify the action in the ServiceNow UI.

    Select the deep link provided in the response to open the alert in ServiceNow and confirm the changes.


## Result

The Alert Actions tool performs your requested action on the alert. The alert state, assignment, or notes are updated in ServiceNow immediately.

## What to do next

After performing an action:

-   If you assigned the alert, notify the assigned user or team through your preferred communication channel.
-   If you closed the alert, monitor for recurring symptoms or related alerts.
-   If you reopened the alert, continue investigation or escalate if needed.

