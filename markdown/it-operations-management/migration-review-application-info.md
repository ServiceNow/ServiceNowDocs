---
title: Review detailed application information in Configurable Workspace
description: Review the information on the discovered applications to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Review your current infrastructure with Cloud Migration Assessment, Planning the migration process, Using Cloud Migration Assessment in Configurable Workspace, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Review detailed application information in Configurable Workspace

Review the information on the discovered applications to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.

## Before you begin

Discover resources on your current infrastructure using Discovery and Cloud Discovery. If your organization uses other solutions for discovery, make sure the discovered information is available in the CMDB.

Role required: cloud\_migration\_operator

## Procedure

1.  Navigate to **All** &gt; **** &gt; **Cloud Migration** &gt; **Cloud Migration Workspace**.

2.  Filter the information on the Migration Flows window by selecting the relevant category from the **Categories** list ![Categories list](../image/cm-workflows-categories-list-button.png).

    For example, select **Physical Server** to display only information related to physical servers. Alternatively, select **AWS** to see which resources are already on the Amazon AWS Cloud.

    All the information on the Migration Flows window matches the selected filter.

3.  Select the **Applications** tile.

    The **Discovered applications** list opens showing the information filtered to match the category you selected in the **Overview** window. For detailed information, see [Applications list in Cloud Migration Assessment](../reference/cloud-migration-applications-list.md).

    ![Applications filtered for the VMware virtualization category](../image/cm-workflows-apps-list.png "Discovered applications filtered for the VMware Virtualization category")

4.  Manipulate the list as necessary using the list buttons.

<table id="table_gky_2t4_zrb"><thead><tr><th>

Button

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Refresh list ![Refresh list button](../image/list-refresh-button.png)

</td><td>

Refreshes the list to display the most updated information.

</td></tr><tr><td>

List actions ![List actions button](../image/list-actions-button.png)

</td><td>

Selects actions supported for this list:-   **Edit columns** - Adjusts the list to display required columns in the order you choose.
-   **Save as** - Creates a copy of this list and save it under **My Lists**.
-   **Reset widths** - Returns the column width to default.


</td></tr><tr><td>

Show filter panel ![Show filter panel button](../image/show-filter-panel-button.png)

</td><td>

Displays the filter panel on the right. If there are filters applied to the list, the Show filter panel button has the number of active filters.

</td></tr></tbody>
</table>5.  Select the application name to review detailed information and metrics for this application.

    A new tab opens and displays the application information.

6.  Select the name of the server to view the info on the server that runs the application in interest.

7.  Close the tab.


**Parent Topic:**[Review your current infrastructure with Cloud Migration Assessment](migration-review-infrastructure.md)

**Related topics**  


[Work with lists in workspace](https://www.servicenow.com/docs/access?context=work-with-lists&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

