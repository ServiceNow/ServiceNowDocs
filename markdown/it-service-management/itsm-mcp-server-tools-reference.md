---
title: ITSM MCP Server tools reference
description: Reference for all tools available in the ITSM MCP Server, organized by functional area: incident management, change management, and employee experience.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/itsm-mcp-server-tools-reference.html
release: australia
topic_type: reference
last_updated: "2026-08-25"
reading_time_minutes: 5
keywords: [ITSM MCP Server, MCP tools, incident management, change management, on-call management, on-call schedule, knowledge graph, natural language prompts, AI workflow, change lifecycle, change.query, change.analyze, change.lifecycle, oncall.who\_is\_on\_call, oncall.my\_next\_shift, oncall.timeoff\_request, service catalog, catalog items, catalog discovery, lookup\_catalog\_items]
breadcrumb: [ITSM MCP Server, IT Service Management]
---

# ITSM MCP Server tools reference

Reference for all tools available in the ITSM MCP Server, organized by functional area: incident management, change management, and employee experience.

**Important:** Only the tools listed here are available. If any other tools display in the Tools definition, you must review and resolve the skipped records for those tools. For information on reviewing and resolving skipped records, see [Review skipped records using related lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/uc-access-rl.md).

## Incident management tools

The following tools are available for incident management in the ITSM MCP Server.

<table id="table-incident-management-tools"><thead><tr><th>

Tool name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_itsm\_mcp\_server.incident.get\_details**

</td><td>

Returns incident fields for a given incident number, including state, priority, assignment, CI, description, and work notes.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.incident.modify**

</td><td>

Updates fields on an incident, including work notes, comments, assignee, and assignment group. Updates run through platform-native APIs with full business rule execution.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.incident.search\_similar**

</td><td>

Searches for incidents similar to a given incident or natural language description using semantic search and returns ranked results.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.lookup\_assignment\_groups**

</td><td>

Looks up available assignment groups and individual assignees.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.lookup\_users**

</td><td>

Looks up users in the system by name, role, or group membership.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server .incident.search\_similar\_kb**

</td><td>

Searches similar Knowledge Base \(KB\) articles based on the input query or details, to find existing content that has already documented the issue or its resolution.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server .incident.get\_kb\_details**

</td><td>

Retrieves details for a single published KB article using number or sys\_id, that includes title, knowledge base, state, publish date, and full body text.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.incident.attach\_kb**

</td><td>

Links a knowledge base article to an incident as a related reference.

</td></tr></tbody>
</table>## Change management tools

The following tools are available to query, analyze, and update change requests in the ITSM MCP Server. Each tool supports multiple operations specified by a required `operation` parameter.

<table id="table-change-management-tools-overview"><thead><tr><th>

Tool name

</th><th>

Operations

</th></tr></thead><tbody><tr><td>

**sn\_itsm\_mcp\_server.change.lifecycle**

</td><td>

-   create—Creates a change request from a model, template, or type
-   update—Updates fields, transitions state, or adds journal entries
-   calculate\_risk—Runs the risk calculator and handles the assessment questionnaire flow
-   upsert\_task—Creates or updates a change task
-   planned\_outage—Creates a planned outage record for the change

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.change.analyze**

</td><td>

-   suggest\_assignment\_groups—Recommends assignment groups based on similar changes, team history, or keyword search
-   get\_risk\_and\_impact\_data—Retrieves the risk score and blast radius for a change
-   suggest\_cis—Recommends configuration items to attach to the change, ranked by confidence score
-   suggest\_models\_and\_templates—Retrieves available change models, standard templates, and custom templates

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.change.query**

</td><td>

-   read—Retrieves one or more change requests by number, including summaries
-   search—Retrieves paginated results using field-based queries, filters, or text search
-   similar\_change\_and\_issues—Returns similar past changes with linked incidents and outages; requires incident-read access
-   aggregate\_by—Returns grouped counts and statistics as cross-tab or independent breakdowns
-   get\_state\_info—Returns the current state, valid next transitions, and mandatory fields
-   check\_schedules\_and\_conflicts—Checks for schedule and CI conflicts, with a freshness indicator
-   data\_quality—Scores a change's data quality and provides improvement guidance

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.change.relation**

</td><td>

-   list\_tasks—Lists change tasks associated with a change
-   list\_affected\_cis—Lists affected configuration items and impacted services
-   list\_approvals—Returns pending approvals for the caller or all approvers on a change
-   list\_incidents—Lists incidents fixed by or caused by the change, including incidents on affected configuration items
-   list\_problems—Lists problems that the change resolves
-   list\_outages—Lists outages linked to the change or to affected configuration items
-   list\_change\_policies—Lists change policies applied to the change, grouped by policy with first and last applied dates

</td></tr></tbody>
</table>## Employee experience tools

The following tools are available for employees and requesters to manage their own tickets in the ITSM MCP Server. These tools apply only to tickets where the authenticated user is the caller or requester.

|Tool name|Description|
|---------|-----------|
|**sn\_itsm\_mcp\_server.requester.create\_incident**|Guides a requester through a multi-step workflow to create a new incident or request a catalog item. The workflow includes knowledge base deflection \(searches for self-service articles\), catalog item redirection \(searches for matching service catalog items\), duplicate detection \(identifies similar open incidents by the requester\), and incident creation with field review. Returns an incident number with portal link or a request item number depending on the path taken.|
|**sn\_itsm\_mcp\_server.requester.check\_status**|Returns the status and details of an incident or requested item \(RITM\) owned by the authenticated user. Accepts a ticket number or a natural language reference such as `my VPN ticket` or `my latest request`. For incidents, returns ticket number, short description, description, priority, urgency, impact, state, created by, and created on. For RITMs, returns the ticket number, approval status, state of the requested item, stage, estimated delivery, and whether the authenticated user is the requested-for user.|
|**sn\_itsm\_mcp\_server.requester.escalate**|Escalates an incident owned by the authenticated user by raising its urgency one level \(**Low** to **Medium**, or **Medium** to **High**\). Requires a mandatory reason that is recorded on the incident. Returns the previous and new urgency values. Escalation does not occur if the urgency is already **High**, the incident is in a **Resolved**, **Closed**, or **Canceled** state, or the incident was escalated within the last 24 hours.|
|**sn\_itsm\_mcp\_server.requester.add\_comment**|Adds a customer-visible comment to an incident or requested item owned by the authenticated user. The comment is attributed to the authenticated requester. Closed or canceled tickets cannot be commented on.|

## On-call management tools

The following tools are available to look up on-call coverage and manage your own on-call schedule in the ITSM MCP Server.

<table id="table-oncall-management-tools"><thead><tr><th>

Tool name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_itsm\_mcp\_server.oncall.on\_call\_lookup**

</td><td>

Looks up on-call coverage. -   **who\_is\_on\_call** — Identifies the current on-call engineers by assignment group or shift name, returning on-call member name and contact details.
-   **my\_next\_shift** — Returns the authenticated user's next or active on-call shift, including assignment group, shift name, shift times and responder level.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.oncall.timeoff\_request**

</td><td>

Requests time off from an on-call shift and arranges coverage. Runs in two phases: -   **analyze** — Performs a read-only check that identifies affected on-call groups, per-group PTO policy, coverage requirements, eligible cover personnel, and conflicting time-off requests for a proposed time window.
-   **create** — Submits the time-off request based on a user-confirmed coverage plan.

 **Important:** The request is submitted only after explicit user confirmation.

</td></tr></tbody>
</table>## Common tools

Common tools for the ITSM MCP Server.

<table id="table_kh5_x2d_xjc"><thead><tr><th>

Tool name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**sn\_itsm\_mcp\_server.itsm\_knowledge\_graph**

</td><td>

Answers structured natural language questions about ITSM data.Using this tool:

-   Get details on incidents or change requests that aren't in the **Closed Complete** state.
-   Get information on available request items and catalog items that are in **Active** state.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.get\_session\_timezone**

</td><td>

Returns the authenticated user's current session time zone and the current date and time in that time zone. Call this tool before interpreting any date and time values or relative date references in user input. No input parameters are required.

</td></tr><tr><td>

**sn\_itsm\_mcp\_server.task\_approval\_decision**

</td><td>

Approves or rejects the caller's oldest pending approval for a change request or request item.

</td></tr></tbody>
</table>