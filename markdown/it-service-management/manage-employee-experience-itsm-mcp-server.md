---
title: Manage request items using the ITSM MCP Server
description: Use the ITSM MCP Server to create incidents, check the status of your own incidents and requested items, and escalate incidents. Add comments through an MCP client application such as Moveworks or Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/manage-employee-experience-itsm-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 2
keywords: [ITSM MCP Server, employee experience, requester, create incident, ticket status, escalate incident, add comments, knowledge base deflection, natural language prompts, AI workflow, service catalog, catalog items, lookup\_catalog\_items]
breadcrumb: [Activate the ITSM MCP Server, ITSM MCP Server, IT Service Management]
---

# Manage request items using the ITSM MCP Server

Use the ITSM MCP Server to create incidents, check the status of your own incidents and requested items, and escalate incidents. Add comments through an MCP client application such as Moveworks or Claude.

## Before you begin

Role required: authenticated user

**Note:** An authenticated user is either a caller on an incident record or a requested-for user on the requested item record. These tools are scoped to tickets where you are the caller or requester.

## About this task

For information on tools, see [ITSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude, that is connected to your ServiceNow instance using the ITSM MCP Server.

    Your system administrator configures this integration during setup.

2.  To create or manage your own tickets, use the corresponding tools.

    The ITSM MCP Server uses five tools to handle the employee experience.

    The MCP client application automatically selects the right tool. The following examples show prompts for each tool.

    **Note:** The tools enforce ownership. You can access only tickets where you are the caller or requester.

    -   **1. __requester.create\_incident__: Create an incident through a guided workflow that searches for self-service solutions, redirects to matching catalog items, and detects duplicate incidents before creating a ticket.**

        Example prompts:

        -   "Create an incident. My laptop won't start."
        -   "I need to log an issue. My VPN keeps disconnecting."
        -   "File a ticket. I can't access my email."
    -   **2. __requester.check\_status__: Check the status and details of your own incidents and requested items.**

        Example prompts:

        -   "What is the status of INC0123456?"
        -   "Show me details for RITM0123456."
        -   "What is the status of my VPN ticket?"
        -   "Show me all my open requests."
    -   **3. __requester.escalate__: Request escalation of your incident to raise its urgency by one level.**

        Example prompts:

        -   "Escalate INC0123456. Production is down and 200 users are affected."
        -   "I need INC0012345 escalated. The system is completely unavailable."
        **Note:** Escalation requires a reason and applies only when the incident is not in a Resolved, Closed, or Canceled state, the urgency is not already High, and the incident was not escalated within the last 24 hours.

    -   **4. __requester.add\_comment__: Add a customer-visible comment to your incident or requested item.**

        Example prompts:

        -   "Add a comment to INC0123456: I've provided the requested information."
        -   "Add a comment to RITM0123456: The issue persists after the fix."
        **Note:** Comments are customer-visible only. Work notes aren't accessible to requesters. You can't add comments to closed or canceled tickets.

    -   **5. __task\_approval\_decision__: Approve or reject the caller's oldest pending approval on a request item.**

        Example prompts:

        -   "Approve RITM1359964."
        -   "Reject RITM1359964."
3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data from tickets you own.


## What to do next

After using the ITSM MCP Server to create or manage a ticket, you can confirm the changes in the Employee Center.

