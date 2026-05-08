---
title: Filters and breadcrumbs
description: A filter is a set of conditions applied to a table to help you find and work with a subset of the data in that table.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Filters and breadcrumbs

A filter is a set of conditions applied to a table to help you find and work with a subset of the data in that table.

You can apply, modify, create, and save filters. A hierarchical list of conditions at the top of the table — breadcrumbs — indicates the current filter.

Breadcrumbs offer a quick form of filter navigation. They are ordered from left to right. The left condition is the most general, and the right condition is the most specific. Clicking a breadcrumb removes all the conditions to its right. Clicking the condition separator \(&gt;\) before a condition removes only that condition.

By default, a user with no roles cannot see the breadcrumbs or filter. Administrators can configure the ESS portal to allow unauthenticated users to see breadcrumbs and filters by using a script include. For more information on using script includes to suppress breadcrumbs and filters, see Use script includes to suppress filters and breadcrumbs .

![Breadcrumbs.](../image/BreadcrumbsUI.png "Breadcrumbs, List v2")

Examples:

-   Clicking **Priority = 2** removes the condition **Category = Software** and returns all active incidents with a priority of 2.
-   Clicking the condition separator \(&gt;\) before **Priority = 2** removes the condition **Priority = 2** and returns all active incidents in the software category.
-   Clicking **All** removes all conditions and returns all incidents in the system.

Click a breadcrumb to refresh the list of records and show the latest information for those records.

**Note:** Clicking the **New** button in a filtered list automatically applies the same filter to the new record. For example, clicking **New** in the Resolved Incidents list opens a record preset with **State** set to **Resolved**. In a list filtered for active, priority 1 incidents, clicking **New** opens a record preset with **Active** selected and **Priority** set to **1 - Critical**.

You can change the preset values on the form as needed. If there is a field you do not want to have populated in this way, you can add the following dictionary attribute to the field: **ignore\_filter\_on\_new=true**.

Additional navigational functions are available when you right-click a breadcrumb.

<table id="table_wr2_3mw_tt"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Open new window

</td><td>

Opens the results list for the breadcrumb in a new tab or window.

</td></tr><tr><td>

Copy URL

</td><td>

Copies the URL to the clipboard for the results list of the breadcrumb. Follow browser instructions if browser security measures restrict this function.

</td></tr><tr><td>

Copy query

</td><td>

Copies the encoded query to the clipboard for the breadcrumb. You can use this query in the URL of an instance or in the reference qualifier field of a dictionary entry.For example, if you are viewing a list of all active incidents with a high or medium impact, right-click the breadcrumb and copy the query **active=true^impact=1^ORimpact=2**. You can append this query to the end of the instance URL as follows:

 `https://{instance_name}/incident_list.do?sysparm_query=active=true^impact=1^ORimpact=2`

 This selection is not available for the **All** breadcrumb.

</td></tr></tbody>
</table>-   **[Quick filters](c_QuickFilters.md)**  
To quickly filter a list using a value in a field, right-click in the field and select **Show Matching** or **Filter Out**. For date fields, choose from **Show Before**, **Show After**, and **Filter Out**.
-   **[Filters](c_Filters.md)**  
A filter restricts what records appear in a list by providing a set of conditions each record must meet to be included in the list.
-   **[Save and use filters in a list view](../task/t_SavingFilters.md)**  
Depending on your access rights, you may save filters for everyone, a user group, or yourself. You can apply saved filters and edit or delete them.
-   **[Filter admin functions](filter-admin-functions.md)**  
Administrators can work with filters in the Filters table \[sys\_filter\], including creating, editing, and deleting filters.
-   **[Encoded query strings](c_EncodedQueryStrings.md)**  
An encoded query string represents a complex filter on a list of records.

**Parent Topic:**[Lists in the classic environment](c_UseLists.md)

**Related topics**  


[bundle-platadm.c_DictionaryAttributes]

[Generate an encoded query string through a filter](../task/t_GenEncodQueryStringFilter.md)

