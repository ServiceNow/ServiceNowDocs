---
title: Manage incidents using the ITSM MCP Server
description: Use the ITSM MCP Server to retrieve and update incident details, find similar incidents, and look up assignment groups. Ask complex multi-hop questions through an MCP client application such as Moveworks or Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/manage-incidents-itsm-mcp-server.html
release: australia
topic_type: task
last_updated: "2026-09-10"
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


No special role is required to use incident.modify and incident.get\_details on an incident you own as a requester. As a requester, the access is scoped to your own incidents, and the fields and actions available to you are based on your access. As a fulfiller, to access to any incident, you need one of the roles listed in the role required section.

## About this task

For information on tools, see [ITSM MCP Server tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/itsm-mcp-server-tools-reference.md).

## Procedure

1.  Open your MCP client application such as Moveworks or Claude, that is connected to your ServiceNow instance using the ITSM MCP Server.

    Your system administrator configured this integration during setup.

2.  To query or update an incident, use the corresponding tools.

    The MCP client application determines the right tool based on your prompt. The following examples show prompts for each tool.

    **Note:** Some common prompts such as, "Show me incidents from the last 30 days that breached SLA. Who was assigned? Are there any patterns to note?" apply to any of these tools.

    -   **1.incident.get\_details: Retrieve fields for a given incident, including state, priority, assignment, CI, description, and work notes.**

        Example prompts:

        -   "Get me up to speed on INC1359964."
        -   "What's going on with INC1359964?"
        -   "Show me the full details of INC1359964."
    -   **2.incident.modify: Update fields on an incident, including work notes, comments, assignee, assignment group and escalate incidents, and mark incidents as resolved.**

        Example prompts:

        -   "Add this work note to INC1359964: Pre-production testing completed successfully."
        -   "Add a comment to INC1359964: Escalated to network team for review."
        -   "Assign INC1359964 to Abel Tuter."
        -   "Assign INC1359964 to the Network Operations group."
        As a requester, you can also use this tool on an incident you own:

        -   "Add a comment to INC1359964: I've provided the requested information."
        -   "Escalate INC1359964, production is down."
        -   "Mark INC1359964 as resolved."
        **Note:** Escalation requires a reason and applies only when the incident is not in a Resolved, Closed, or Canceled state, the urgency is not already High, and the incident was not escalated within the last 24 hours.

    -   **3.incident.search\_similar: Search for incidents similar to a given incident or natural language description using semantic search.**

        Example prompts:

        -   "Show me similar incidents from the last 90 days."
        -   "Find recent incidents related to database connectivity."
        -   "Are there other incidents like INC1359964 from the past month?"
    -   **4.lookup\_assignment\_groups: Look up available assignment groups and individual assignees.**

        Example prompts:

        -   "Who handles network incidents?"
        -   "What assignment groups are available for P1 incidents?"
        -   "List the members of the Network Operations assignment group."
    -   **5.lookup\_users: Look up users in the system by name, role, or group membership.**

        Example prompts:

        -   "Find the user Abel Tuter."
        -   "Who is on the Network Operations team?"
        -   "List users with the itil role."
3.  To search similar KB, get details and attach the KB to incident, use the corresponding tools and operations:

    -   **incident.search\_similar\_kb: Searches Knowledge Base \(KB\) articles to find existing content that documents the issue or its resolution.**

        A list of matching articles, each with article number, relevance score, knowledge base source, title, and KB URL, is displayed. Retrieves only active and published KB articles. You can use any of the inputs to get the required information.

        -   **query** - Enter the description of the issues for which KBs must be searched.
        -   **incident\_number** - Builds the query from an incident.

            The tool reads incident short description and details, and uses the information to search similar KB articles automatically.

        Example prompts:

        -   search similar KBs for "VPN keeps disconnecting on Windows"
        -   search similar KBs for "Email server is down"
    -   **incident.get\_kb\_details: Retrieves the details of a single published KB article using number or __sys\_id__.**

        The KB article details include the article title, knowledge base, state, publish date, and full body text.

        Example prompts: "Get details for KB0012345"

    -   **incident.attach\_kb: Links a KB article to an incident as a related reference.**

        Enter the incident number and the KB article to attach. You can also enter the **sys\_id** of the incident or KB instead of the number. Attaches only active and published KB articles. After you attach a KB article to an incident, the system displays a confirmation message. For example:

        ```
        "result": {
        
            "status": "attached",
        
            "incident": "INC0010252",
        
            "kb_number": "KB99999999",
        
            "message": "Knowledge article KB99999999 attached to INC0010252."
        
          }
        
        ```

        Example prompts:

        -   "Attach KB0010001 to INC0012345"
        -   "Attach incident \(sys\_id\) to KB \(sys\_id\)"
4.  Review the MCP client application response.

    The MCP client application retrieves data from your ServiceNow instance and presents it in the chat. The response includes only data you have permission to access.


## What to do next

After using the ITSM MCP Server to investigate or update an incident, verify the updates in your ServiceNow instance.

