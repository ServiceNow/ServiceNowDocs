---
title: Combined ITSM MCP Server release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for ITSM MCP Server from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-itsmmcpserver-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 8
breadcrumb: [Products combined by family]
---

# Combined ITSM MCP Server release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for ITSM MCP Server from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family ITSM MCP Server release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading ITSM MCP Server to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for ITSM MCP Server.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[Managing incidents](https://www.servicenow.com/docs/access?context=manage-incidents-itsm-mcp-server&family=zurich&ft:locale=en-US)**

Use incident management tools to get details, update fields, and find similar incidents in the ITSM MCP Server.

For example:

    -   Get incident fields including state, priority, assignment, CI, description, and work notes with `incident.get_details`.
    -   Update incident fields and work notes through platform-native APIs with full business rule execution using `incident.modify`.
    -   Search for similar incidents using semantic search with `incident.search_similar`, and look up assignment groups and users with `lookup_assignment_groups` and `lookup_users`.
    -   Search similar Knowledge Base \(KB\) articles using `incident.search_similar_kb`, and retrieve details for a published KB article using `incident.get_kb_details`.
    -   Link a KB article to an incident as a related reference using `incident.attach_kb`.
-   **[Managing change requests](https://www.servicenow.com/docs/access?context=manage-change-requests-itsm-mcp-server&family=zurich&ft:locale=en-US)**

Use change management tools to query, analyze, and update change requests in the ITSM MCP Server.

For example:

    -   Create and update change requests, calculate risk, and manage planned outages with `change.lifecycle`.
    -   Analyze changes by recommending assignment groups, retrieving risk and impact data, and suggesting configuration items and templates with `change.analyze`.
    -   Retrieve, search, and aggregate change data, check schedules and conflicts, and score data quality with `change.query`.
    -   List tasks, affected CIs, approvals, incidents, problems, outages, and change policies with `change.relation`.
-   **[Managing request items](https://www.servicenow.com/docs/access?context=manage-employee-experience-itsm-mcp-server&family=zurich&ft:locale=en-US)**

Use request item tools to create and manage your own tickets in the ITSM MCP Server.

For example:

    -   Create incidents or request catalog items through a guided workflow that includes knowledge base deflection, catalog item redirection, and duplicate detection using `requester.create_incident`.
    -   Escalate an incident's urgency with a mandatory reason using `requester.escalate`.
    -   Add customer-visible comments to your open incidents or requested items using `requester.add_comment`.
-   **[Managing on-call schedules](https://www.servicenow.com/docs/access?context=manage-on-call-schedule-itsm-mcp-server&family=zurich&ft:locale=en-US)**

Use on-call management tools to look up coverage and manage your on-call schedule in the ITSM MCP Server.

For example:

    -   Identify current on-call engineers by assignment group or shift name, and view your next or active on-call shift details using `oncall.on_call_lookup`.
    -   Request time off from an on-call shift and arrange coverage through a two-phase analyze-and-create workflow using `oncall.timeoff_request`.
-   **[Using ITSM MCP Server common tools](https://www.servicenow.com/docs/access?context=itsm-mcp-server-tools-reference&family=zurich&ft:locale=en-US)**

Use common tools to use with the ITSM MCP Server.

For example:

    -   Answer structured natural language questions about ITSM data, including details on incidents, change requests, and active catalog items using `itsm_knowledge_graph`.
    -   Approve or reject your oldest pending approval for a change or request items using `task_approval_decision`.
    -   Get the authenticated user's current session time zone and the current date and time in that time zone using `get_session_timezone`.

</td></tr><tr><td>

Australia

</td><td>

-   **[Managing incidents](https://www.servicenow.com/docs/access?context=manage-incidents-itsm-mcp-server&family=australia&ft:locale=en-US)**

Use incident management tools to get details, update fields, and find similar incidents in the ITSM MCP Server.

For example:

    -   Get incident fields including state, priority, assignment, CI, description, and work notes with `incident.get_details`.
    -   Update incident fields and work notes through platform-native APIs with full business rule execution using `incident.modify`.
    -   Search for similar incidents using semantic search with `incident.search_similar`, and look up assignment groups and users with `lookup_assignment_groups` and `lookup_users`.
    -   Search similar Knowledge Base \(KB\) articles using `incident.search_similar_kb`, and retrieve details for a published KB article using `incident.get_kb_details`.
    -   Link a KB article to an incident as a related reference using `incident.attach_kb`.
-   **[Managing change requests](https://www.servicenow.com/docs/access?context=manage-change-requests-itsm-mcp-server&family=australia&ft:locale=en-US)**

Use change management tools to query, analyze, and update change requests in the ITSM MCP Server.

For example:

    -   Create and update change requests, calculate risk, and manage planned outages with `change.lifecycle`.
    -   Analyze changes by recommending assignment groups, retrieving risk and impact data, and suggesting configuration items and templates with `change.analyze`.
    -   Retrieve, search, and aggregate change data, check schedules and conflicts, and score data quality with `change.query`.
    -   List tasks, affected CIs, approvals, incidents, problems, outages, and change policies with `change.relation`.
-   **[Managing request items](https://www.servicenow.com/docs/access?context=manage-employee-experience-itsm-mcp-server&family=australia&ft:locale=en-US)**

Use request item tools to create and manage your own tickets in the ITSM MCP Server.

For example:

    -   Create incidents or request catalog items through a guided workflow that includes knowledge base deflection, catalog item redirection, and duplicate detection using `requester.create_incident`.
    -   Escalate an incident's urgency with a mandatory reason using `requester.escalate`.
    -   Add customer-visible comments to your open incidents or requested items using `requester.add_comment`.
-   **[Managing on-call schedules](https://www.servicenow.com/docs/access?context=manage-on-call-schedule-itsm-mcp-server&family=australia&ft:locale=en-US)**

Use on-call management tools to look up coverage and manage your on-call schedule in the ITSM MCP Server.

For example:

    -   Identify current on-call engineers by assignment group or shift name, and view your next or active on-call shift details using `oncall.on_call_lookup`.
    -   Request time off from an on-call shift and arrange coverage through a two-phase analyze-and-create workflow using `oncall.timeoff_request`.
-   **[Using ITSM MCP Server common tools](https://www.servicenow.com/docs/access?context=itsm-mcp-server-tools-reference&family=australia&ft:locale=en-US)**

Use common tools to use with the ITSM MCP Server.

For example:

    -   Answer structured natural language questions about ITSM data, including details on incidents, change requests, and active catalog items using `itsm_knowledge_graph`.
    -   Approve or reject your oldest pending approval for a change or request items using `task_approval_decision`.
    -   Get the authenticated user's current session time zone and the current date and time in that time zone using `get_session_timezone`.

</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing ITSM MCP Server features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some ITSM MCP Server features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some ITSM MCP Server features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate ITSM MCP Server.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

ITSM MCP Server is available with activation of the following plugins:

    -   ServiceNow Otto for IT Service Management \(ITSM\) plugin \(sn\_itsm\_gen\_ai\)
    -   Model Context Protocol Server \(sn\_mcp\_server\)
    -   ITSM MCP Server \(sn\_itsm\_mcp\_server\)
For details, see [\[Placeholder link text to key set-up-itsm-mcp-server\]](https://www.servicenow.com/docs/access?context=set-up-itsm-mcp-server&family=zurich&ft:locale=en-US).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

ITSM MCP Server is available with activation of the following plugins:

    -   ServiceNow Otto for IT Service Management \(ITSM\) plugin \(sn\_itsm\_gen\_ai\)
    -   Model Context Protocol Server \(sn\_mcp\_server\)
    -   ITSM MCP Server \(sn\_itsm\_mcp\_server\)
For details, see [\[Placeholder link text to key set-up-itsm-mcp-server\]](https://www.servicenow.com/docs/access?context=set-up-itsm-mcp-server&family=australia&ft:locale=en-US).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for ITSM MCP Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for ITSM MCP Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for ITSM MCP Server, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for ITSM MCP Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for ITSM MCP Server we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

Using ITSM MCP Server, manage incidents, change requests, and on-call schedule. You can also check the status of your own incidents and requested items, and escalate incidents.

-   **Incident management:** Retrieve, modify, and search incidents; answer natural-language questions about incident data.

-   **Change management:** Execute end-to-end change lifecycle with approvals, risk evaluation, and quality assurance across multiple tables.

-   **Request management:** Create incidents with knowledge deflection, check status, escalate, and add customer-visible comments.

-   **On-call scheduling:** Retrieve rosters and shifts, request time off, and query availability through natural-language questions.


 See [\[Placeholder link text to key itsm-mcp-server-overview\]](https://www.servicenow.com/docs/access?context=itsm-mcp-server-overview&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

Using ITSM MCP Server, manage incidents, change requests, and on-call schedule. You can also check the status of your own incidents and requested items, and escalate incidents.

-   **Incident management:** Retrieve, modify, and search incidents; answer natural-language questions about incident data.

-   **Change management:** Execute end-to-end change lifecycle with approvals, risk evaluation, and quality assurance across multiple tables.

-   **Request management:** Create incidents with knowledge deflection, check status, escalate, and add customer-visible comments.

-   **On-call scheduling:** Retrieve rosters and shifts, request time off, and query availability through natural-language questions.


 See [\[Placeholder link text to key itsm-mcp-server-overview\]](https://www.servicenow.com/docs/access?context=itsm-mcp-server-overview&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

