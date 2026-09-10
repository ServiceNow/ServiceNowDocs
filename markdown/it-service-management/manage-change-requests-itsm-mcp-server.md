---
title: Manage change requests using the ITSM MCP Server
description: Use the ITSM MCP Server to query change requests, assess risk and conflicts, evaluate change data quality, find similar past changes, create or update changes, and more. Manage the change lifecycle through an MCP client application such as Moveworks or Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/manage-change-requests-itsm-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 3
keywords: [ITSM MCP Server, change management, change requests, change summarization, risk explanation, natural language prompts, AI workflow, knowledge graph, similar changes, change scheduling, change conflicts, change lifecycle, change analysis, change query, risk and impact]
breadcrumb: [Activate the ITSM MCP Server, ITSM MCP Server, IT Service Management]
---

# Manage change requests using the ITSM MCP Server

Use the ITSM MCP Server to query change requests, assess risk and conflicts, evaluate change data quality, find similar past changes, create or update changes, and more. Manage the change lifecycle through an MCP client application such as Moveworks or Claude.

## Before you begin

**Note:** System administrators have the option of exposing the custom change request fields — such as environment type or CAB ticket reference — to the AI assistant in the ITSM MCP Server. After this is configured, the assistant uses those fields across all change-related operations without additional setup.

The `ITSMMCPChangeCustomFields` script include defines which custom fields are exposed:

```
var ITSMMCPChangeCustomFields = Object.assign({}, ITSMMCPChangeCustomFieldsSNC,
  {
 
    // Return your custom change_request column names.
    //
    // Example:
    //     return ['u_environment_type', 'u_business_owner', 'u_cab_ticket'];
    //
    // Ships empty, so out of the box the Change MCP tools behave exactly as they
    // did before this extension point existed.
    getCustomFields: function() {
        return ['u_production_gate_check'];
    },
 
    type: 'ITSMMCPChangeCustomFields'
}
);
```

Role required: itil

## About this task

For detailed information on each tool, supported operations, and operation-specific parameters, see [ITSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude, that is connected to your ServiceNow instance using the ITSM MCP Server.

    **Note:** Your system administrator configures this integration during setup.

2.  To query a change request, use the corresponding tools and operations.

    The ITSM MCP Server uses multiple tools to handle change management.

    The MCP client application automatically selects the right tool. The following examples show prompts for each tool.

    **Note:** Some common prompts such as, "Show me changes from the last 30 days that had issues. Who filed them? Are there any patterns to note?" apply to any of these tools.

    -   **1. __change.lifecycle__: Create, update, recalculate risk, and manage state transitions for change requests.**

        Example prompts:

        -   "Create a normal change to apply OS and DB security patches to the production database server."
        -   "Assign CHG0030014 to the Database team, add a work note that backups are verified, and move it to Assess."
        -   "Recalculate the risk and impact for CHG0030014."
        -   "Approve the CHG0030014."
        -   "Create change tasks for the implementation steps of CHG0030014."
        -   "Create a planned outage for CHG0030014."
        -   "Close CHG0030014 and mark it as successful."
    -   **2. __change.analyze__: Inspect a single change request for state, scheduling, risk, and CI impact details.**

        Example prompts:

        -   "What state is CHG0030014 in, and what can I move it to next?"
        -   "Are there any scheduling or CI conflicts for CHG0030014's maintenance window?"
        -   "Show me the current risk and blast radius for CHG0030014."
        -   "Can you suggest CIs for CHG0030014."
        -   "Assess the risk and impact for CHG0030014 before we proceed."
        -   "Assess the quality of CHG0030014."
    -   **3. __change.query__: Search, retrieve, and aggregate change requests from the change table.**

        Example prompts:

        -   "Get the full details of CHG0030014."
        -   "Summarize any high risk changes pending approval that are scheduled within the next two weeks."
        -   "List all open changes assigned to the Network team."
        -   "Find past changes similar to CHG0030014."
        -   "What's the status of open changes assigned to my group? Anything pending action from our team?"
        -   "Aggregate changes by priority and status to show our current change load."
        -   Summarize CHG0010001, CHG0010002, and CHG0010003.
        -   Show the latest emergency changes for the Network team with the newest ones first.
        -   "Show me changes broken down by risk, and separately by state, and separately by team."
    -   **4. __change.relation__: Retrieve related records for a change, including tasks, affected configuration items, approvals, incidents, problems, outages, and applied policies.**

        Example prompts:

        -   "What changes are pending my approval?"
        -   "Tell me more about CHG000001. What CIs/services are affected?"
        -   "Were there any recent incidents or outages against the CIs against this change?"
        -   "Which change policies have been applied to CHG000001?"
        -   "What implementation tasks are assigned to me for CHG000001?"
    -   **5.__task\_approval\_decision__: Approve or reject the caller's oldest pending approval for a change request or request item.**

        Example prompts:

        -   "Approve CHG000001."
        -   "Reject CHG000001."
3.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


## What to do next

After using the ITSM MCP Server to write or update a change request, verify the updates in your ServiceNow instance. Confirm that all fields, state transitions, risk assessments, and change tasks are accurate before proceeding with the change.

