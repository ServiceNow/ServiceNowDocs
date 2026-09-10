---
title: Manage on-call schedule using the ITSM MCP Server
description: Use the ITSM MCP Server to find out who is on call, check your next on-call shift, and request time off. Manage your on-call schedule through an MCP client application such as Moveworks or Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/manage-on-call-schedule-itsm-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-07-29"
reading_time_minutes: 2
keywords: [ITSM MCP Server, on-call schedule, on-call rotation, who is on call, on-call shift, time off request, on-call coverage, rota, roster, natural language prompts, AI workflow]
breadcrumb: [Activate the ITSM MCP Server, ITSM MCP Server, IT Service Management]
---

# Manage on-call schedule using the ITSM MCP Server

Use the ITSM MCP Server to find out who is on call, check your next on-call shift, and request time off. Manage your on-call schedule through an MCP client application such as Moveworks or Claude.

## Before you begin

Role required: itil, roster\_admin, rota\_admin, rota\_manager, or oc\_read.

**Note:** These are the out-of-box roles. An administrator can configure additional roles using the `com.snc.on_call_rotation.calendar_read_roles` system property. For more information, see [System properties for On-Call Scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/on-call-scheduling/on-call-properties.md).

## About this task

For detailed information on each tool, supported operations, and operation-specific parameters, see [ITSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude, that is connected to your ServiceNow instance using the ITSM MCP Server.

    Your system administrator configures this integration during setup.

2.  To find who is on call, check your next shift, or request time off, use the corresponding tools.

    The ITSM MCP Server uses two tools to handle on-call schedule management.

    The MCP client application automatically selects the right tool. The following examples show prompts for each tool.

    -   **1. __oncall.on\_call\_lookup__: Find the on-call engineer or engineers for an assignment group or shift, or find your next upcoming or currently in-progress on-call shift.**

        Example prompts:

        -   "Who is on call for the Network Operations group right now?"
        -   "Who is on call as primary on the Service Desk group?"
        -   "When is my next on-call shift?"
        -   "Am I on call right now?"
        **Note:** You can be on more than one roster at a time, such as different assignment groups or multiple roster tiers on the same rota. The response lists one entry for each roster.

    -   **2. __oncall.timeoff\_request__: Request time off and arrange coverage.**

        Example prompts:

        -   "I need time off from my on-call shift next Monday and Tuesday."
        -   "Request time off for my on-call shift from July 10 to July 12."
        **Note:** The tool first analyzes the request, identifying affected groups, approval requirements, and who is eligible to cover, and presents the plan for your confirmation. The time off request is created only after you confirm.

3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


## What to do next

After using the ITSM MCP Server to request time off, verify that request and coverage assignments in your ServiceNow instance.

