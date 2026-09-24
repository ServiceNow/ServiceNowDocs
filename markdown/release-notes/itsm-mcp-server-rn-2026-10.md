---
title: Brazil Patch 1 and Version 3.3
description: Add comments, escalate, and combine the check incident status with get incident details tool.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/itsm-mcp-server-rn-2026-10.html
release: brazil
topic_type: topic
last_updated: "2026-09-17"
reading_time_minutes: 1
breadcrumb: [ITSM MCP Server release notes, IT Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Brazil Patch 1 and Version 3.3

Add comments, escalate, and combine the check incident status with get incident details tool.

## What's new

## What's changed

-   **[Changes to ITSM MCP server tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/itsm-mcp-server-tools-reference.md)**
    -   Added role restrictions for the ITSM MCP Change management tools.
    -   The **sn\_itsm\_mcp\_server.incident.get\_details**and **sn\_itsm\_mcp\_server.incident.modify** incident tools are available to both fulfillers and requesters. You use the **sn\_itsm\_mcp\_server.incident.modify** tool to also escalate incidents.
    -   The **sn\_itsm\_mcp\_server.requester.add\_comment** tool has been renamed to **sn\_itsm\_mcp\_server.request.modify**. Using this tool the requester can add customer-visible comments to their Requested Items. To add customer-visible comments to incidents, use the **sn\_itsm\_mcp\_server.incident.modify** tool.

## What's deprecated or removed

-   **[Deprecated sn\_itsm\_mcp\_server.requester.escalate tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/manage-employee-experience-itsm-mcp-server.md)**

    The **sn\_itsm\_mcp\_server.requester.escalate** tool is disabled by default. Use **sn\_itsm\_mcp\_server.incident.modify** with the **escalate** and **escalation\_reason** inputs instead.


## Plugin information

-   **New plugins**

     \(\): 

-   **Deprecated plugins**

     \(\): 

-   **Plugins planned for deprecation**

     \(\): Planned for deprecation in . 

-   **Renamed or changed plugins**

     \(\): 


**Parent Topic:**[ITSM MCP Server release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itsm-mcp-server-rn.md)

