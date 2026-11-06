---
title: CRM Workspace list pages
description: List pages in CRM Workspace provide agents with filtered lists of cases, interactions, and other records including accounts and contacts. Agents can use lists to search for records, sort and group records, and select records to view information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/csm-config-workspace-list-views.html
release: australia
topic_type: concept
last_updated: "2026-10-26"
reading_time_minutes: 2
breadcrumb: [CRM Workspace features, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CRM Workspace list pages

List pages in CRM Workspace provide agents with filtered lists of cases, interactions, and other records including accounts and contacts. Agents can use lists to search for records, sort and group records, and select records to view information.

\[Omitted image "csm-config-ws-lists.png"\] Alt text: CRM Workspace includes several filtered lists that display database table, record, and field data

A list page is a content page that displays records from a table, such as cases or case tasks. List pages help agents navigate and manage records.

## Using lists in CRM Workspace

From a list page, agents can:

-   Select a filtered list of records such as **Cases** &gt; **My Cases**.
-   Create a list of records by selecting the table, the columns to display in the list, and filter conditions that apply to the list.
-   Search a list of records
-   Filter, sort, and group records in a list

For more information, see the following topics:

-   [Search and filter lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-ws-search-filter-lists.md)
-   [Create a customized list of records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-ws-create-custom-list.md)
-   [Manage customized record lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-ws-manage-custom-list.md)
-   [Using lists in Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/using-lists-configurable-workspace.md)

## Configuring lists in CRM Workspace

Users with the administrator role can configure [list components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md) in UI Builder.

Additional list features are configured using system properties. For more information about setting these properties, see [Administering lists for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/administer-lists-configurable-workspace.md).

## List components

List pages in CRM Workspace are made up of multiple components that present information and enable agents to search, sort and filter, and select records.

<table id="table_owv_yzq_xkc"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[List menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md)

</td><td>

Enables agents to navigate between lists. This component includes two tabs:-   **Default lists**: admin-configured lists
-   **My lists**: agent-created lists

</td></tr><tr><td>

[Record List component bundle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md)

</td><td>

Combines the following components:-   Record list header
-   Presentational list
-   Pagination control

</td></tr><tr><td>

[Record list header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md)

</td><td>

Displays the list title, actions agents can take on the list, and a button to create records. Agents can filter, sort, and group list items.

</td></tr><tr><td>

[Predicate Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md)

</td><td>

Enables users to set conditions from the record list header to filter which records appear in a list.

</td></tr><tr><td>

[Presentational list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md)

</td><td>

Displays data from the source table in columns and rows.

</td></tr><tr><td>

[Pagination control](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/csm-config-workspace-list-components.md)

</td><td>

Enables users to navigate pages of records and set the number of records displayed per page.

</td></tr></tbody>
</table>## Open multiple lists in workspace tabs

Agents can open a list in a new workspace primary tab from the list menu by using **Cmd/Ctrl + click**. Agents can also select **Open in new session tab** from the list menu or right-click the context menu.

For example, an agent may have the Open Cases list open and receive a link to a filtered list for an escalated customer. The agent can open the filtered list in a separate tab and switch between both lists without losing their place. The tab label displays the list name for easy identification.

## Additional information

For more information about working with lists, see the following topics in the [Configurable Workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/workspace-landing-page.md) documentation:

-   [Lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/lists-configurable-workspace.md)
-   [Administering lists for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/administer-lists-configurable-workspace.md)
-   [Using lists in Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/using-lists-configurable-workspace.md)

