---
title: CSM Configurable Workspace list views
description: The CSM Configurable Workspace list views provide filtered lists of cases, interactions, and other records such as accounts and contacts. Agents can also create and save their own lists.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace list views

The CSM Configurable Workspace list views provide filtered lists of cases, interactions, and other records such as accounts and contacts. Agents can also create and save their own lists.

A list displays records from a database table. Each list includes rows and columns of data. Each row is a record in a table and each column is a field from the record. CSM Configurable Workspace uses list pages to display list information such as cases and case tasks. These pages are designed to help agents navigate, filter, and manage records.

CSM Configurable Workspace presents the Core UI lists and forms in one interface and consolidates multiple tabs into a single, focused work area. From this single view, agents can:

-   Work on multiple issues concurrently in an intuitive layout, reducing context and tab switching.
-   Resolve issues faster with automated suggestions powered by machine learning.
-   Get notified of potential major incidents based on issue frequency and impact.
-   Keep informed of updates and surface important insights with a live activity feed and analytics.

## List pages in CSM Configurable Workspace

List pages for CSM Configurable Workspace are created with the List page template in UI Builder. The List page template includes the Record List component bundle and List menu component.

![CSM Configurable Workspace includes several filtered lists that display database table, record, and field data](../image/csm-config-ws-lists.png "CSM Configurable Workspace lists")

## Record List component bundle

The Record List component bundle includes the following components:

-   Record List Header: Shows contextual information about the list.
-   Presentational List: Displays the list of records from any data source in a tabular format.

The Record List component bundle is configured by admins in UI Builder. For more information, see [Record list UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/record%20list/overview).

## List menu component

The List menu component displays all available and saved lists for the selected source. It's not included in the Record List component bundle itself but exists within a list page.

The List menu component includes the following tabs:

-   Default lists: This tab displays all available lists based on the selected source. These lists gives agents quick access to relevant records.
-   My lists: This tab enables agents to access their saved lists that help streamline repeat workflows and create their own lists from an existing list or by selecting a new source.

The List menu component is configured by admins in UI Builder. For information on List menu component configurations, see [List menu UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-record-list-menu-connected/uib-setup).

## Predicate Builder

The Predicate Builder component enables agents to set conditions from the list header to filter which records appear in a list.

![Predicate Builder for a Configurable Workspace](../../../administer/workspace/image/configurable-workspace-predicate-builder.png)

The Predicate Builder is configured by admins in UI Builder. For more information, see [Predicate Builder UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-predicate-builder/overview).

## Open multiple lists in workspace tabs

Agents can open a list in a new workspace primary tab from the list menu by using **Cmd/Ctrl + click**, or by selecting **Open in new session tab** from the list menu or right-click context menu.

For example, an agent may have the Open Cases list open and receive a link to a filtered list for an escalated customer. The agent can open the filtered list in a separate tab and switch between both lists without losing their place. The tab label displays the list name for easy identification.

## Additional information

For more information about working with lists, see the following topics in the [Configurable Workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/workspace-landing-page.md) documentation:

-   [Administering lists for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/administer-lists-configurable-workspace.md)
-   [Using lists in Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/using-lists-configurable-workspace.md)

