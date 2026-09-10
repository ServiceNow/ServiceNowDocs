---
title: ITSM MCP Server release notes
description: Using the ServiceNow ITSM MCP Server application connect an AI-enabled Model Context Protocol \(MCP\) client application to your ServiceNow environment using the ITSM MCP Server. This connection enables incident and change management for service desk agents and IT managers, and enables requesters to check and manage their own tickets.Manage incidents, change requests, request items, and on-call schedules with the ITSM MCP Server. Empower requesters to handle their own tickets and access shared tools for approvals and ITSM data queries.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-08-25"
reading_time_minutes: 3
keywords: [ITSM MCP Server, change management, service catalog, change.query, change.relation, change.analyze]
---

# ITSM MCP Server release notes

Using the ServiceNow® ITSM MCP Server application connect an AI-enabled Model Context Protocol \(MCP\) client application to your ServiceNow environment using the ITSM MCP Server. This connection enables incident and change management for service desk agents and IT managers, and enables requesters to check and manage their own tickets.

## About ITSM MCP Server

Using ITSM MCP Server, manage incidents, change requests, and on-call schedule. You can also check the status of your own incidents and requested items, and escalate incidents.

-   **Incident management:** Retrieve, modify, and search incidents; answer natural-language questions about incident data.

-   **Change management:** Execute end-to-end change lifecycle with approvals, risk evaluation, and quality assurance across multiple tables.

-   **Request management:** Create incidents with knowledge deflection, check status, escalate, and add customer-visible comments.

-   **On-call scheduling:** Retrieve rosters and shifts, request time off, and query availability through natural-language questions.


See  for more information.

## Activation and other requirements

-   **Activation information**

    ITSM MCP Server is available with activation of the following plugins:

    -   ServiceNow Otto for IT Service Management \(ITSM\) plugin \(sn\_itsm\_gen\_ai\)
    -   Model Context Protocol Server \(sn\_mcp\_server\)
    -   ITSM MCP Server \(sn\_itsm\_mcp\_server\)
    For details, see .


**Parent Topic:**[IT Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-service-management-rn-landing.md)

## Australia Patch 4 and Version 3.2

Manage incidents, change requests, request items, and on-call schedules with the ITSM MCP Server. Empower requesters to handle their own tickets and access shared tools for approvals and ITSM data queries.

### What's new

-   **[Managing incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/manage-incidents-itsm-mcp-server.md)**

    Use incident management tools to get details, update fields, and find similar incidents in the ITSM MCP Server.

    For example:

    -   Get incident fields including state, priority, assignment, CI, description, and work notes with `incident.get_details`.
    -   Update incident fields and work notes through platform-native APIs with full business rule execution using `incident.modify`.
    -   Search for similar incidents using semantic search with `incident.search_similar`, and look up assignment groups and users with `lookup_assignment_groups` and `lookup_users`.
    -   Search similar Knowledge Base \(KB\) articles using `incident.search_similar_kb`, and retrieve details for a published KB article using `incident.get_kb_details`.
    -   Link a KB article to an incident as a related reference using `incident.attach_kb`.
-   **Managing change requests**

    Use change management tools to query, analyze, and update change requests in the ITSM MCP Server.

    For example:

    -   Create and update change requests, calculate risk, and manage planned outages with `change.lifecycle`.
    -   Analyze changes by recommending assignment groups, retrieving risk and impact data, and suggesting configuration items and templates with `change.analyze`.
    -   Retrieve, search, and aggregate change data, check schedules and conflicts, and score data quality with `change.query`.
    -   List tasks, affected CIs, approvals, incidents, problems, outages, and change policies with `change.relation`.
-   **Managing request items**

    Use request item tools to create and manage your own tickets in the ITSM MCP Server.

    For example:

    -   Create incidents or request catalog items through a guided workflow that includes knowledge base deflection, catalog item redirection, and duplicate detection using `requester.create_incident`.
    -   Escalate an incident's urgency with a mandatory reason using `requester.escalate`.
    -   Add customer-visible comments to your open incidents or requested items using `requester.add_comment`.
-   **Managing on-call schedules**

    Use on-call management tools to look up coverage and manage your on-call schedule in the ITSM MCP Server.

    For example:

    -   Identify current on-call engineers by assignment group or shift name, and view your next or active on-call shift details using `oncall.on_call_lookup`.
    -   Request time off from an on-call shift and arrange coverage through a two-phase analyze-and-create workflow using `oncall.timeoff_request`.
-   **Using ITSM MCP Server common tools**

    Use common tools to use with the ITSM MCP Server.

    For example:

    -   Answer structured natural language questions about ITSM data, including details on incidents, change requests, and active catalog items using `itsm_knowledge_graph`.
    -   Approve or reject your oldest pending approval for a change or request items using `task_approval_decision`.
    -   Get the authenticated user's current session time zone and the current date and time in that time zone using `get_session_timezone`.

