---
title: Virtual Machine \(VM\) Explorer dashboard
description: The Discovery Admin Workspace displays information on the activity and capacity of your Virtual Machine instances as revealed by discovery.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Discovery Admin Workspace Insights, Discovery Admin Workspace, Exploring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Virtual Machine \(VM\) Explorer dashboard

The Discovery Admin Workspace displays information on the activity and capacity of your Virtual Machine instances as revealed by discovery.

![VM dashboard](../image/vm_daw.png)

## Required ServiceNow AI Platform roles

-   discovery\_admin
-   admin

## Access the Virtual Machine \(VM\) Explorer dashboard

To open the dashboard, navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Insights** &gt; **Virtual Machine Explorer**.

## Indicators

-   **Virtual Machines with server CI**

    The total number and the trend of the virtual machines that have a server CI discovered since a given date.

-   **Virtual machines with no deep dive discovery**

    The total number and the trend of the virtual machines discovered that have no CI relationships created for them.


## Reports

<table id="table_e2r_zqr_zbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Virtual machines by class

</td><td>

![bar](../../../use/reporting/image/icon-bar-report-p.png)

</td><td>

\[cmdb\_ci\_vm\_instance\]

</td><td>

The number of VMs in your infrastructure sorted by class.

</td></tr><tr><td>

Virtual machines by state

</td><td>

![pie](../../../use/reporting/image/icon-pie-report-p.png)

</td><td>

\[cmdb\_ci\_vm\_instance\]

</td><td>

The percent of VMs grouped by state: on, off, or other.

</td></tr></tbody>
</table>## Filters

<table id="table_g2r_zqr_zbc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Virtual Machine Instance

</td><td>

The filter enables you to select all instances you want to export, by categories such as **State** and **Disk size**.

</td></tr></tbody>
</table>