---
title: AI Search Admin console Shared Configurations page
description: This page is where you view and manage all configurations shared by AI Search and other applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [AI Search Admin console reference, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Admin console Shared Configurations page

This page is where you view and manage all configurations shared by AI Search and other applications.

![AI Search Admin console Shared Configurations Summary view with 3 callouts highlighted. For a text description, see the table that follows.](../image/ais-admin-shared-config.png "AI Search Admin console Shared Configurations")

<table id="table_lyh_wwg_rhb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Navigation bar

</td><td>

Tabs to navigate between Home, Applications, and Shared Configurations pages.

</td></tr><tr><td>

2. Configurations sidebar

</td><td>

Tabs for navigating the types of Shared Configurations tables. Select a tab to view the table:-   Summary
-   Search profiles \[ais\_search\_profile\] table
-   Search sources \[ais\_search\_source\] table
-   Indexed Sources \[ais\_datasource\] table
-   Dictionaries \[ais\_dictionary\] table
-   Genius Results \[ais\_genius\_result\_configuration\] table
-   Search application configurations \[sys\_search\_context\_config\] table
-   Result-card interfaces \[sys\_ux\_composite\_data\]

</td></tr><tr><td>

3. Shared Configurations

</td><td>

Cards for navigating the types of Shared Configurations tables. These cards match the entries in the Tab sidebar. Select a card to view the table.

</td></tr></tbody>
</table>## Shared Configurations tables

![AI Search Admin console Shared Configurations page, showing the Search Profiles table.](../image/ais-admin-03a.png "Sample Shared Configuration Table")

All Shared Configurations tables use the same controls to manage their entries.

|Field|Description|
|-----|-----------|
|Refresh list ![Refresh list icon.](../image/refresh-list-icon.png)|Button to refresh list of table entries.|
|List Actions ![List actions icon.](../image/list-actions-icon.png)|Button to open list actions. Select **Edit columns** to add or remove columns from the table. Select **Reset widths** if you have adjusted any column widths.|
|Show/Hide Filter panel ![Filter panel icon.](../image/filter-panel-icon.png)|Button to open filter conditions panel. Select the clear input icon \(![Clear input icon.](../image/icon-clear-input.png)\) next to any defined conditions to remove them. Select **Restore defaults** to reset default filters, or **Advanced view** to define filter conditions. For more information, see [Set filter conditions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining/filter-conditions.md).|
|New|Button to create a record.|
|Delete|Button to delete records. Select one or more entries before selecting **Delete**|

For further information on using these tables, see [Create an AI Search configuration](../task/ais-admin-console-create-config.md).

