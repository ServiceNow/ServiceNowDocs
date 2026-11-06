---
title: CMDB MCP Server release notes
description: Version history for the ServiceNow CMDB MCP Server application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-cmdb-mcp-server.html
release: store
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 1
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# CMDB MCP Server release notes

Version history for the ServiceNow® CMDB MCP Server application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.1.0 - November 2026**
    -   New: The Get CI Topology and Get Impacted Items tools use the V2 Impact Analysis agent.
    -   Changed: Get CI Topology takes a change request or incident number in the task\_number parameter instead of a CI sys\_id in ci\_sys\_id. Update MCP clients to pass task\_number. Get Impacted Items continues to take change\_request\_number.
-   **Version 2.0.1 - October 2026**

    Fixed: Added missing tooltip descriptions to tools.

-   **Version 2.0.0 - September 2026**

    Initial release.

-   **Version 1.0.1 - July 2026**
    -   Securely connect AI agents to your ServiceNow CMDB and Visibility data via the Model Context Protocol \(MCP\). Query CIs and relationships and get service mapping-related information.
    -   The ServiceNow CMDB and Visibility MCP Server exposes specific, read-only tools so AI clients \(like Claude, ChatGPT, or ServiceNow's own AI agents\) can discover assets and pull infrastructure relationship data without human intervention.

**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

