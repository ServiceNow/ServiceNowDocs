---
title: Manage incidents using the ITSM MCP Server
description: Use the ITSM MCP Server to retrieve and update incident details, find similar incidents, and look up assignment groups. Ask complex multi-hop questions through an MCP client application such as Moveworks or Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/manage-incidents-itsm-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-07-07"
reading_time_minutes: 4
keywords: [ITSM MCP Server, incident management, incidents, incident investigation, knowledge graph, SLA analysis, multi-hop queries, natural language prompts, AI workflow]
breadcrumb: [Activate the ITSM MCP Server, ITSM MCP Server, IT Service Management]
---

# Manage incidents using the ITSM MCP Server

Use the ITSM MCP Server to retrieve and update incident details, find similar incidents, and look up assignment groups. Ask complex multi-hop questions through an MCP client application such as Moveworks or Claude.

## Before you begin

Role required: itil, incident\_read, incident\_write

**Note:** The following roles determine which incident management tools a user can access:

-   itil - Access to all incident management tools.
-   sn\_incident\_read - Access to tools used for searching or viewing incident and KB details:
    -   incident.get\_details
    -   incident.search\_similar
    -   incident.search\_similar\_kb
    -   incident.get\_kb\_details
    -   lookup\_assignment\_groups
    -   lookup\_users
-   sn\_incident\_write - Access to all tools available to sn\_incident\_read, including the following tools for modifying incidents and attaching KB articles:

    -   incident.modify
    -   incident.attach\_kb
    Use the sn\_incident\_read role for read-only access to incident and KB data. Use sn\_incident\_write when users need to modify incidents or attach KB articles.


## About this task

For information on tools, see [ITSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/itsm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude, that is connected to your ServiceNow instance using the ITSM MCP Server.

    Your system administrator configures this integration during setup.

2.  To query or update an incident, use the corresponding tools and operations.

    The MCP client application automatically selects the right tool. The following examples show prompts for each tool.

    **Note:** Some common prompts such as, "Show me incidents from the last 30 days that breached SLA. Who was assigned? Are there any patterns to note?" apply to any of these tools.

    -   **1.__incident.get\_details__: Retrieve fields for a given incident, including state, priority, assignment, CI, description, and work notes.**

        Example prompts:

        -   "Get me up to speed on INC1359964."
        -   "What's going on with INC1359964?"
        -   "Show me the full details of INC1359964."
    -   **2.__incident.modify__: Update fields on an incident, including work notes, comments, assignee, and assignment group.**

        Example prompts:

        -   "Add this work note to INC1359964: Pre-production testing completed successfully."
        -   "Add a comment to INC1359964: Escalated to network team for review."
        -   "Assign INC1359964 to Abel Tuter."
        -   "Assign INC1359964 to the Network Operations group."
    -   **3.__incident.search\_similar__: Search for incidents similar to a given incident or natural language description using semantic search.**

        Example prompts:

        -   "Show me similar incidents from the last 90 days."
        -   "Find recent incidents related to database connectivity."
        -   "Are there other incidents like INC1359964 from the past month?"
    -   **4.__lookup\_assignment\_groups__: Look up available assignment groups and individual assignees.**

        Example prompts:

        -   "Who handles network incidents?"
        -   "What assignment groups are available for P1 incidents?"
        -   "List the members of the Network Operations assignment group."
    -   **5.__lookup\_users__: Look up users in the system by name, role, or group membership.**

        Example prompts:

        -   "Find the user Abel Tuter."
        -   "Who is on the Network Operations team?"
        -   "List users with the itil role."
3.  To search similar KB, get details and attach the KB to incident, use the corresponding tools and operations:

    -   **__incident.search\_similar\_kb__: Searches Knowledge Base \(KB\) articles to find existing content that documents the issue or its resolution.**

        A list of matching articles, each with article number, relevance score, knowledge base source, title, and KB URL, is displayed. Retrieves only active and  published  KB articles. You can use any of the inputs to get the required information.

        -   query  - Enter the description of the issues for which KBs must be searched.
        -   incident\_number  - Builds the query from an incident.

            The tool reads incident short description and details, and uses the information to search similar KB articles automatically.

        Example prompts:

        -   search similar KBs for "VPN keeps disconnecting on Windows"
        -   search similar KBs for "Email server is down"
    -   **__incident.get\_kb\_details__: Retrieves the details of a single published KB article using number or sys\_id.**

        The KB article details include the article title, knowledge base, state, publish date, and full body text.

        Example prompts: “Get details for KB0012345"

    -   **__incident.attach\_kb__: Links a KB article to an incident as a related reference.**

        Enter the incident number and the KB article that must be attached. You can also enter the sys\_id of the incident or KB instead of the number. Attaches only active and published  KB articles. After a KB article is attached to an incident, a confirmation message is display. For example:

        ```
        "result": {
        
            "status": "attached",
        
            "incident": "INC0010252",
        
            "kb_number": "KB99999999",
        
            "message": "Knowledge article KB99999999 attached to INC0010252."
        
          }
        
        ```

        Example prompts:

        -   “Attach KB0010001 to INC0012345“
        -   "Attach incident \(sys\_id\) to KB \(sys\_id\)“
4.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


## What to do next

After using the ITSM MCP Server to investigate or update an incident, verify the updates in your ServiceNow instance.

