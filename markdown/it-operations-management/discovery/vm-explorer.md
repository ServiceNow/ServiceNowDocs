---
title: Virtual Machine Explorer dashboard
description: The Discovery Admin Workspace Virtual Machine Explorer dashboard displays information on the activity and capacity of your virtual machine \(VM\) instances as revealed by the discovery process.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Virtual Machine Explorer dashboard

The Discovery Admin Workspace Virtual Machine Explorer dashboard displays information on the activity and capacity of your virtual machine \(VM\) instances as revealed by the discovery process.

![VM dashboard](../image/vm_daw.png)

To access the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Virtual Machine Explorer**.

## Key features

The VM Explorer dashboard enables you to make data-driven decisions through powerful visualizations.

Select the **More options** icon \(![More options icon](../../health-log-analytics-operator/image/icon-menu-sow.png)\), then select **Refresh** to refresh the data for each visualization in this section.

<table id="table_jsk_zl3_cfc"><thead><tr><th>

Report title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Virtual machines with server CI

</td><td>

Indicator and line chart

</td><td>

Displays the total number and trend of VMs that have a server configuration item \(CI\) discovered since a given date.

</td></tr><tr><td>

Virtual machines with no deep dive discovery

</td><td>

Indicator and line chart

</td><td>

Displays the total number and trend of the VMs that have no created CI relationships discovered since a given date.

</td></tr><tr><td>

Virtual machine by class

</td><td>

Bar chart

</td><td>

Displays the number of VMs in your infrastructure sorted by class.Virtual Machine Instances \[cmdb\_ci\_vm\_instance\] table is the source table for this chart.

</td></tr><tr><td>

Virtual machines by state

</td><td>

Pie chart

</td><td>

Displays the percent of VMs grouped by the following states: on, off, or other.Virtual Machine Instances \[cmdb\_ci\_vm\_instance\] table is the source table for this chart.

</td></tr></tbody>
</table>**Note:** When you first access the VM Explorer dashboard after installing Discovery Admin Workspace, the Virtual machines with server CI and Virtual Machines with no deep dive discovery indicators might not display scores. For instructions on how to collect data for these scores, see [Run historical data collection for Virtual Machine Explorer](../task/t_RunHistoricalDataCollectVME.md).

## Virtual Machine Instance

This section offers an overview of VM instances discovered, featuring key information such as the Object ID, Class, and Network adapters. You can select an instance from the table to view detailed information about it, or select the **Edit form** icon \(![Edit form icon](../image/workspace-edit-vminstance.png)\) to edit details and view activity. The filter icon \(![filter icon](../image/filter-icon-daw.png)\) enables you to apply fixed filters or create custom filters that can be saved and reused. To export the table, choose the **Export** option and select your preferred format: Excel, CSV, JSON, or PDF.

