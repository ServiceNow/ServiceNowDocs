---
title: Installed with Vendor Management Workspace
description: Vendor Management Workspace provides a single destination for you to view and manage your vendors.
locale: en-US
release: xanadu
product: Vendor Management Workspace
classification: vendor-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Vendor Management Workspace reference, Vendor Management Workspace, IT Service Management]
---

# Installed with Vendor Management Workspace

Vendor Management Workspace provides a single destination for you to view and manage your vendors.

## Vendor Management Workspace

When you activate the Vendor Management Workspace \(sn\_itsm\_vendor\) plugin, the following components are installed.

<table id="table_rd3_4gw_5hb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Vendor admin\[sn\_vlm.vendor\_admin\]

</td><td>

Can create, edit, or delete vendor types and KPI groups in Vendor Management Workspace

</td><td>

sn\_vlm.vendor\_manager

</td></tr><tr><td>

Vendor Manager\[sn\_vlm.vendor\_manager\]

</td><td>

Views and manages vendors using Vendor Management Workspace.

 Configures vendor performance metrics for use in Vendor Management Workspace.

</td><td>

-   pa\_viewer
-   service\_viewer
-   service\_credit\_mgr

</td></tr></tbody>
</table><table id="table_m3c_j4y_jjb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

KPI Vendors\[sn\_itsm\_vendor\_kpi\_group\_m2m\_vendor\]

</td><td>

Store the relationship between KPIs and vendors.

</td></tr></tbody>
</table><table id="table_qgw_pvf_qxb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Process Mining - VM Remine Projects**

</td><td>

-   Automatically runs once a day.
-   Automatically updates the project when vendors are added or removed.
-   Fetches all projects that haven’t been mined from the time-period specified in the **sn\_itsm\_vendor.po\_mining.run\_frequency** system property; for example, the last 7 days.

</td></tr></tbody>
</table>Navigate to **Vendor Management** &gt; **Configuration** &gt; **Vendor Properties** to set the properties for Vendor Management Workspace.

<table id="table_ojw_fby_llb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_itsm\_vendor.enable.po.vm

</td><td>

Enables the integration of Process Mining with Vendor Management Workspace. When enabled, you can initiate process mining and mine Process Mining projects and analyze process analysis in Vendor Management Workspace.

-   **Type:** true \| false
-   **Default value:** false

</td></tr><tr><td>

sn\_itsm\_vendor.po\_mining.run\_frequency

</td><td>

Fetches all projects that haven’t been mined for the specified time-period. The **Process Mining - VM Remine Projects** job fetches the data based on the time specified in this property.

-   **Type:** Integer
-   **Default value:** 7

</td></tr></tbody>
</table>**Parent Topic:**[Vendor Management Workspace reference](vendor-manager-workspace-reference.md)

