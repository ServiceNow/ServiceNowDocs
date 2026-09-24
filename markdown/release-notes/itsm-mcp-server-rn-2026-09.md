---
title: Brazil Patch 0 and Version 3.2
description: Manage incidents, change requests, request items, and on-call schedules with the ITSM MCP Server. Empower requesters to handle their own tickets and access shared tools for approvals and ITSM data queries.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/itsm-mcp-server-rn-2026-09.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ITSM MCP Server, change management, service catalog, change.query, change.relation, change.analyze]
breadcrumb: [ITSM MCP Server release notes, IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Brazil Patch 0 and Version 3.2

Manage incidents, change requests, request items, and on-call schedules with the ITSM MCP Server. Empower requesters to handle their own tickets and access shared tools for approvals and ITSM data queries.

## What's new

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

**Parent Topic:**[ITSM MCP Server release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itsm-mcp-server-rn.md)

