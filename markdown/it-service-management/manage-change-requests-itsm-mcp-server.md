---
title: Manage change requests using the ITSM MCP Server
description: Use the ITSM MCP Server to create change requests, check their status, modify them, and approve or reject them. Interact through an MCP client application such as Moveworks or Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/manage-change-requests-itsm-mcp-server.html
release: brazil
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [ITSM MCP Server, change requests, change management, create change, check change status, modify change, approve change, natural language prompts, AI workflow]
breadcrumb: [Activate the ITSM MCP Server, ITSM MCP Server, IT Service Management]
---

# Manage change requests using the ITSM MCP Server

Use the ITSM MCP Server to create change requests, check their status, modify them, and approve or reject them. Interact through an MCP client application such as Moveworks or Claude.

## Before you begin

Role required: itil or change\_manager

## About this task

For information on tools, see [ITSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude, that is connected to your ServiceNow instance using the ITSM MCP Server.

    Your system administrator configures this integration during setup.

2.  To create or manage change requests, use the corresponding tools.

    The ITSM MCP Server uses four tools to handle change requests.

    The MCP client application automatically selects the right tool. The following examples show prompts for each tool.

    -   **1. change.create: Create a change request with required fields.**

        Example prompts:

        -   "Create a change request for database upgrade scheduled for next Friday."
        -   "I need to create a change for server maintenance on March 15."
    -   **2. change.check\_status: Check the status and details of change requests.**

        Example prompts:

        -   "What is the status of CHG0123456?"
        -   "Show me details for change request CHG0123456."
        -   "What are my open change requests?"
    -   **3. change.modify: Modify change request fields or add comments.**

        Example prompts:

        -   "Update CHG0123456 planned start date to March 20."
        -   "Add a comment to CHG0123456: Risk assessment completed."
        -   "Change the priority of CHG0123456 to Critical."
        **Important:**

        -   change.modify can update most change request fields and add customer-visible comments.
        -   You can't modify closed or canceled change requests using change.modify.
    -   **4. task\_approval\_decision: Approve or reject the caller's oldest pending approval on a change request.**

        Example prompts:

        -   "Approve CHG0123456."
        -   "Reject CHG0123456."
3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat.


## What to do next

After using the ITSM MCP Server to create or manage a change request, you can confirm the changes in the Change Management application.

