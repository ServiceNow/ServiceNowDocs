---
title: ITSM MCP Server release notes
description: The ServiceNow ITSM MCP Server application connects an AI-enabled Model Context Protocol \(MCP\) client application to your ServiceNow environment using the ITSM MCP Server. This connection enables incident and change management for service desk agents and IT managers, and enables requesters to check and manage their own tickets.Some of the ITSM MCP tools have been renamed and have also been made available to fulfillers and requesters in ITSM MCP Server in this release. Manage incidents, change requests, request items, and on-call schedules with the ITSM MCP Server. Empower requesters to handle their own tickets and access shared tools for approvals and ITSM data queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/itsm-mcp-server-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [ITSM MCP Server, Model Context Protocol, incident management, change management, ITSM MCP Server, ITSM MCP Server, change management, service catalog, change.query, change.relation, change.analyze]
breadcrumb: [IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# ITSM MCP Server release notes

The ServiceNow® ITSM MCP Server application connects an AI-enabled Model Context Protocol \(MCP\) client application to your ServiceNow environment using the ITSM MCP Server. This connection enables incident and change management for service desk agents and IT managers, and enables requesters to check and manage their own tickets.

## About ITSM MCP Server

Using ITSM MCP Server, manage incidents, change requests, and on-call schedule. You can also check the status of your own incidents and requested items, and escalate incidents.

-   **Incident management:** Retrieve, modify, and search incidents; answer natural-language questions about incident data.

-   **Change management:** Execute end-to-end change lifecycle with approvals, risk evaluation, and quality assurance across multiple tables.

-   **Request management:** Create incidents with knowledge deflection, check status, escalate, and add customer-visible comments.

-   **On-call scheduling:** Retrieve rosters and shifts, request time off, and query availability through natural-language questions.


See [ITSM MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-overview.md) for more information.

## Activation and other requirements

-   **Activation information**

    Activate these plugins to use ITSM MCP Server:

    -   Now Assist for ITSM plugin \(sn\_itsm\_gen\_ai\)
    -   Model Context Protocol Server \(sn\_mcp\_server\)
    -   ITSM MCP Server \(sn\_itsm\_mcp\_server\)
    For details, see [Activate the ITSM MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/set-up-itsm-mcp-server.md).


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-service-management-rn-landing.md)

## Brazil Patch 1 and Version 3.3

Some of the ITSM MCP tools have been renamed and have also been made available to fulfillers and requesters in ITSM MCP Server in this release.

### What's changed

-   **[Changes to the ITSM MCP Server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-tools-reference.md)**
    -   You need the sn\_mcp\_server.viewer role as the base role to access ITSM MCP server.
    -   The **sn\_itsm\_mcp\_server.incident.get\_details** and **sn\_itsm\_mcp\_server.incident.modify** incident tools are available to both fulfillers and requesters.
        -   As a fulfiller, you can use the **sn\_itsm\_mcp\_server.incident.modify** tool to also escalate incidents.
        -   As a requester, you can use the **sn\_itsm\_mcp\_server.incident.get\_details** to check the status of a specific incident.
    -   The **sn\_itsm\_mcp\_server.requester.add\_comment** tool has been renamed to **sn\_itsm\_mcp\_server.request.modify**.
        -   As a requester, you can use the **sn\_itsm\_mcp\_server.request.modify** tool to add customer-visible comments to the requested items.
        -   As a fulfiller, you can use the **sn\_itsm\_mcp\_server.incident.modify** to add customer-visible comments to incidents.

### What's deprecated or removed

-   **[Deprecated sn\_itsm\_mcp\_server.requester.escalate tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-employee-experience-itsm-mcp-server.md)**

    The **sn\_itsm\_mcp\_server.requester.escalate** tool is turned off by default. Use **sn\_itsm\_mcp\_server.incident.modify** with the **escalate** and **escalation\_reason** inputs instead.


## Brazil Patch 0 and Version 3.2

Manage incidents, change requests, request items, and on-call schedules with the ITSM MCP Server. Empower requesters to handle their own tickets and access shared tools for approvals and ITSM data queries.

### What's new

-   **[Managing incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-incidents-itsm-mcp-server.md)**

    Use incident management tools to get details, update fields, and find similar incidents in the ITSM MCP Server.

    For example:

    -   Get incident fields including state, priority, assignment, CI, description, and work notes with `incident.get_details`.
    -   Update incident fields and work notes through platform-native APIs with full business rule execution using `incident.modify`.
    -   Search for similar incidents using semantic search with `incident.search_similar`, and look up assignment groups and users with `lookup_assignment_groups` and `lookup_users`.
    -   Search similar Knowledge Base \(KB\) articles using `incident.search_similar_kb`, and retrieve details for a published KB article using `incident.get_kb_details`.
    -   Link a KB article to an incident as a related reference using `incident.attach_kb`.
-   **[Managing change requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-change-requests-itsm-mcp-server.md)**

    Use change management tools to query, analyze, and update change requests in the ITSM MCP Server.

    For example:

    -   Create and update change requests, calculate risk, and manage planned outages with `change.lifecycle`.
    -   Analyze changes by recommending assignment groups, retrieving risk and impact data, and suggesting configuration items and templates with `change.analyze`.
    -   Retrieve, search, and aggregate change data, check schedules and conflicts, and score data quality with `change.query`.
    -   List tasks, affected CIs, approvals, incidents, problems, outages, and change policies with `change.relation`.
-   **[Managing request items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-employee-experience-itsm-mcp-server.md)**

    Use request item tools to create and manage your own tickets in the ITSM MCP Server.

    For example:

    -   Create incidents or request catalog items through a guided workflow that includes knowledge base deflection, catalog item redirection, and duplicate detection using `requester.create_incident`.
    -   Escalate an incident's urgency with a mandatory reason using `requester.escalate`.
    -   Add customer-visible comments to your open incidents or requested items using `requester.add_comment`.
-   **[Managing on-call schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-on-call-schedule-itsm-mcp-server.md)**

    Use on-call management tools to look up coverage and manage your on-call schedule in the ITSM MCP Server.

    For example:

    -   Identify current on-call engineers by assignment group or shift name, and view your next or active on-call shift details using `oncall.on_call_lookup`.
    -   Request time off from an on-call shift and arrange coverage through a two-phase analyze-and-create workflow using `oncall.timeoff_request`.
-   **[Using ITSM MCP Server common tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-tools-reference.md)**

    Use common tools to use with the ITSM MCP Server.

    For example:

    -   Answer structured natural language questions about ITSM data, including details on incidents, change requests, and active catalog items using `itsm_knowledge_graph`.
    -   Approve or reject your oldest pending approval for a change or request items using `task_approval_decision`.
    -   Get the authenticated user's current session time zone and the current date and time in that time zone using `get_session_timezone`.

