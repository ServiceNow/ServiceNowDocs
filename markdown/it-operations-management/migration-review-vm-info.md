---
title: Review detailed information on virtual machines in Configurable Workspace
description: Review the information on the discovered virtual machines \(VMs\) to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Review your current infrastructure with Cloud Migration Assessment, Planning the migration process, Using Cloud Migration Assessment in Configurable Workspace, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Review detailed information on virtual machines in Configurable Workspace

Review the information on the discovered virtual machines \(VMs\) to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.

## Before you begin

Discover resources on your current infrastructure using Discovery and Cloud Discovery. If your organization uses other solutions for discovery, make sure the discovered information is available in the CMDB.

Role required: sn\_cloud\_migration.operator

## About this task

When you use horizontal discovery by Discovery, VMs are discovered together with the their relations to the servers. Cloud Discovery finds VMs without their related servers.

## Procedure

1.  Navigate to **All** &gt; **** &gt; **Cloud Migration** &gt; **Cloud Migration Workspace**.

2.  Filter the information on the Migration Flows window by selecting the relevant category from the **Categories** list ![Categories list](../image/cm-workflows-categories-list-button.png).

    For example, select **Physical Server** to display only information related to physical servers. Alternatively, select **AWS** to see which resources are already on the Amazon AWS Cloud.

    All the information on the Migration Flows window matches the selected filter.

3.  To review the information related to VMs discovered by Cloud Discovery, select the **VMs on undiscovered servers** tile.

    Alternatively, for VMs that have been discovered together with their related servers, review VMs as described in [Review detailed server information in Configurable Workspace](migration-review-server-info.md).

    The **VMs on undiscovered servers** list opens, showing the information filtered to match the category you selected in the **Overview** window.

4.  To hide a resource that you are not planning to migrate from any list in Cloud Migration Assessment, select this resource, and then select the **Ignore** button.

5.  Change the list view or export the list, using the list buttons.

<table id="table_mym_gbp_zrb"><thead><tr><th>

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

</td></tr><tr><td>

Export

</td><td>

Saves the list in one of the supported formats: Excel, CSV, JSON, PDF.

</td></tr></tbody>
</table>
**Parent Topic:**[Review your current infrastructure with Cloud Migration Assessment](migration-review-infrastructure.md)

