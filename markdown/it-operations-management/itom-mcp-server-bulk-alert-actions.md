---
title: Perform bulk alert actions from an MCP Client
description: Use the Alert Actions tool in an MCP Client to assign, close, reopen, or acknowledge multiple related alerts as a group in a single request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-bulk-alert-actions.html
release: australia
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 2
breadcrumb: [Alert actions, Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Perform bulk alert actions from an MCP Client

Use the Alert Actions tool in an MCP Client to assign, close, reopen, or acknowledge multiple related alerts as a group in a single request.

## Before you begin

Verify that:

-   The ITOM MCP Server Console is active on your ServiceNow instance.
-   Your MCP Client application is connected to the ITOM MCP Server Console with valid OAuth credentials.

**Important:** The Alert Actions tool acts on alerts through an AI agent or MCP Client. You're interacting with AI. AI-generated responses may be inaccurate or incomplete. Review the confirmation and the linked alert after each action to verify the result.

For more information about the Alert Actions tool, see [Alert actions with an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-mcp-server-alert-actions.md).

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

Alerts often occur in groups related to the same underlying issue or infrastructure failure. The Alert Actions tool performs bulk operations that coordinate a response across multiple related alerts. Bulk operations apply the same action to every alert in the group, which keeps handling consistent across the group.

For example, to respond to a widespread outage:

1.  In the MCP Client application \(such as AWS Claude\), ask: "List all critical alerts created in the last hour."

    12 related alerts are returned. These alerts span database, network, and storage systems.

2.  Determine the root cause affects all systems.

    Ask: "Assign all 12 of these alerts to the infrastructure team. Add note: Outage traced to power supply failure in DC1. Maintenance started at 14:30 UTC."

    You receive: "All 12 alerts assigned to infrastructure team. Work note added to each alert."

3.  Verify by clicking the link to the alert group.
4.  Later, after the issue is resolved, ask: "Close all 12 of these alerts. Add note: Power supply replaced. Full system recovery confirmed."

    You receive: "All 12 alerts closed."


## Procedure

1.  Open your MCP Client application.

2.  Ask the MCP Client to list related alerts.

3.  Identify the alert group or set of related alerts you want to manage.

    For example: "List all critical alerts related to the database service created in the last 2 hours."

4.  Request a bulk action on the alert group.

    Use natural language to describe the bulk action. For example:

    -   "Assign all these alerts to the database team."
    -   "Close all database-related alerts created today. Add note: Issue resolved by maintenance window."
    -   "Reopen all alerts related to the load balancer. New symptoms detected."
    -   "Acknowledge the 5 network alerts listed above."
    -   "Add this note to all storage alerts: Escalated to infrastructure team for investigation."
5.  Review the response from your MCP Client.

    The response includes:

    -   Count of alerts affected by the bulk action.
    -   Confirmation that the action succeeded.
    -   Deep links to the alert group or individual alerts for verification.
6.  Verify the bulk action in the ServiceNow UI.

    Select the provided link to open the alert group and confirm all changes were applied correctly.


## Result

The Alert Actions tool performs the bulk action on all selected alerts. Each alert is updated with the new state, assignment, or notes in ServiceNow immediately.

## What to do next

After performing a bulk action:

-   If you assigned a group of alerts, notify the assigned team about the scope and nature of the alerts.
-   If you closed a group, monitor for recurrence or new related alerts that might indicate incomplete resolution.
-   If you made bulk assignments, follow up to confirm the team is investigating.

