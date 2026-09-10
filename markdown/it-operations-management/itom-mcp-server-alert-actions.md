---
title: Alert actions with an MCP Client
description: Manage alerts through an AI agent or MCP Client. The Alert Actions tool lets the agent or client act on alerts directly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-mcp-server-alert-actions.html
release: australia
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 2
breadcrumb: [Use the ITOM MCP Server Console, AI in ITOM, IT Operations Management]
---

# Alert actions with an MCP Client

Manage alerts through an AI agent or MCP Client. The Alert Actions tool lets the agent or client act on alerts directly.

## Alert Actions tool overview

MCP tools retrieve data from your ServiceNow instance and perform alert actions.

The Alert Actions tool enables you to assign, close, reopen, acknowledge, and annotate alerts through natural language prompts without leaving your MCP Client. The tool complements capabilities for retrieving and investigating alerts.

**Important:** The Alert Actions tool acts on alerts through an AI agent or MCP Client. You're interacting with AI. AI-generated responses may be inaccurate or incomplete. Review the confirmation and the linked alert after each action to verify the result.

## Single vs. bulk alert operations

The Event Management Alerts table represents both individual alerts and alert groups. The Alert Actions tool automatically detects the scope:

-   Single-alert operations act on one alert at a time. Typical for direct investigation and targeted response.

    Users with the evt\_mgmt\_operator role can perform single-alert actions. They can assign to self, close after investigation, acknowledge receipt, and add diagnostic notes.

-   Bulk operations act on multiple related alerts \(alert group\) in a single request. Efficient for coordinated team response to widespread issues.

    Users with the evt\_mgmt\_admin role can perform bulk operations on alert groups. They can reassign multiple related alerts to the network team, close a batch of resolved alerts, and acknowledge a group of new alerts.


Both modes support all actions described in the Supported actions section.

## Supported actions

The Alert Actions tool supports the following operations on individual alerts and alert groups:

|Action|Description|
|------|-----------|
|Assign|Assign an alert to a user or group. Useful for routing work to the right team.|
|Close|Mark an alert as closed. Use when the underlying issue is resolved.|
|Reopen|Reopen a previously closed alert. Required if a closed alert recurs.|
|Acknowledge|Acknowledge receipt of an alert. Helps prevent duplicate escalations and signals active monitoring.|
|Add work notes|Add internal notes to an alert to record investigation details for other agents and operators.|
|Add comments|Add comments visible to other agents and operators working on the alert.|

## Use cases

The Alert Actions tool is useful in the following scenarios:

-   An operator investigates an alert in an MCP Client, identifies the root cause, and immediately closes it with a note—all in the chat.
-   A manager receives a notification about critical alerts, lists them in the MCP Client, assigns the entire batch to the on-call engineer, and tracks confirmation in real time.
-   An operator acknowledges time-sensitive alerts to help prevent duplicate escalations, without navigating to the ServiceNow Event Management UI.

## Workflow

The Alert Actions tool operates as part of the ITOM MCP Server Console workflow:

1.  An operator or manager opens their MCP Client application and describes the action they need.

    For example: "Assign this alert to the network team".

2.  The MCP Client sends the request to the ITOM MCP Server Console using the Model Context Protocol \(MCP\).
3.  The ITOM MCP Server Console authenticates the user against ServiceNow role-based access control \(RBAC\).
4.  The ITOM MCP Server Console performs the requested action on the alert record.
5.  The ITOM MCP Server Console returns a confirmation to the MCP Client, including a deep link to the alert for verification in the UI if needed.

