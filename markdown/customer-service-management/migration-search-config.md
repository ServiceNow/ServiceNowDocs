---
title: Global Search in CSM Configurable Workspace
description: Learn about how the CSM Agent Workspace Global Search functions with CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-search-config.html
release: zurich
topic_type: concept
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Global Search in CSM Configurable Workspace

Learn about how the CSM Agent Workspace Global Search functions with CSM Configurable Workspace.

Global Search provides users with the ability to search for information within the defined search sources.

If search sources aren't configured correctly, agents may get incomplete results or no results when they search in CSM Configurable Workspace. Existing search source configurations carry over, but the global search configuration itself uses the UX page property table instead of the legacy global search configuration table. After migration, verify that the search sources you had in CSM Agent Workspace are mapped correctly.

|Legacy table name|UIB table name|
|-----------------|--------------|
|sys\_aw\_global\_search\_config|sys\_ux\_page\_property|

For more information, see [Using AI Search with CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-ai-search.md).

## Verify global search after migration

Role required: admin

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **Experiences** and select **CSM/FSM Configurable Workspace**.
2.  In the **UX Page Properties** related list, open the **globalSearchDataConfigId** property.

    The property value is the sys\_id of the search application configuration that the workspace uses.

3.  Verify that the search sources you had in CSM Agent Workspace are mapped correctly, and add or adjust search sources as needed.

    Make sure that search sources are mapped to guidance inputs so that agents get accurate results.


