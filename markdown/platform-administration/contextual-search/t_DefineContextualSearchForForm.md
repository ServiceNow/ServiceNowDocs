---
title: Configure table for a contextual search
description: Configure the options for the contextual search that a table performs.
locale: en-US
release: zurich
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Contextual search, Search administration, Configure core features, Administer]
---

# Configure table for a contextual search

Configure the options for the contextual search that a table performs.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration** and click **New**.

2.  On the form, fill in the fields.

    ![Table configuration form when the UI type is platform](../image/ContextualSearchTableConfig.png "Table Configuration form")

<table id="table_gh2_gtj_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name and label of the table associated with the form. For example, Incident \[incident\].

</td></tr><tr><td>

UI type

</td><td>

User interface differs depending on whether you use the table configuration for Platform or Workspace. **Note:** The **When to display** section appears only when you select **Platform** from **UI type**.

 ![Table configuration when the UI type is Workspace](../image/cxs-table-config-workspace.png)

</td></tr><tr><td>

Search context

</td><td>

Lookup icon ![Lookup icon to select a search context](../image/look-up-icon.png) to select a search context for which you are configuring the table.

</td></tr><tr><td>

Title

</td><td>

Unique title for the search results area that appears in the form. For example, if you enter `Knowledge results` as the value in this field, the related search area displays **Knowledge results** as the title. ![Related search area](../image/related-search-results.png)

</td></tr><tr><td>

Enable related search box

</td><td>

Option to show the related search box in the form.

</td></tr><tr><td>

Show searcher first

</td><td>

Option to display searcher resources before additional resources in the search context. This field appears only when you select **Workspace** from **UI type**.

</td></tr><tr><td>

Enable source selector

</td><td>

Option to show the list of search sources that you can search from.**Note:** This field appears only when you select **Enable related search box**.

</td></tr><tr><td>

Application

</td><td>

Application scope of the table configuration. The configuration is available for all applications or for scoped applications.

</td></tr><tr><td>

Active

</td><td>

Option to activate the table configuration.

</td></tr><tr><td>

Limit

</td><td>

Maximum number of search results returned.

</td></tr><tr><td>

Results per page

</td><td>

Number of results to display per page.

</td></tr><tr><td>

Allow expand/collapse

</td><td>

Option to enable a user to collapse the search results in the form.

</td></tr><tr><td>

Enable preview buttons

</td><td>

Option to show a preview button \(platform only\) for each search result. The user can then use the preview button or the search result title to preview the result record.**Note:** The option is available from the London release. Clear the option to provide a more compact display for each search result.

</td></tr><tr><td>

Allow search with empty search text

</td><td>

Option to specify whether the search runs when there is no search text. **Note:** There is no search text when there is no **Search Field** specified or when there is a **Search Field** whose value is empty.

</td></tr><tr><td class="sub-head" colspan="2">

When to display

</td></tr><tr><td>

Required roles

</td><td>

List of roles that grant access to the related search results widget from the table. Users must have one of these roles to see the widget when viewing the table.

</td></tr><tr><td>

Condition

</td><td>

Conditions that records must satisfy to appear as related search results. For example, set **\[Active\] \[is\] \[true\]** to only enable the active records as related search results.

</td></tr><tr><td class="sub-head" colspan="2">

Search as

</td></tr><tr><td>

Enable search as

</td><td>

Option to enable searching as a different user. The message box describes the settings available when you select this option.![Search as field](../image/search-as.png) For more information on using **Search as**, see [Enable viewing of search results for the current and another selected user](t_SearchAsDifferentUser.md).

</td></tr></tbody>
</table>3.  Click **Submit**.

    The Search Fields, Filter Configurations, Email Configurations, and Search Action Configurations related lists appear. By default, the **Short description** field is added to the Search Fields related list.

    **Note:** Search results only appear for Search Fields that are visible on the form.


**Parent Topic:**[Configuring contextual search](../concept/configuring-contextual-search.md)

