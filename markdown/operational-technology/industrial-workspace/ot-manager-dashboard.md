---
title: Operational Technology Visibility dashboard
description: The Operational Technology \(OT\) Visibility dashboard helps you manage your OT device in a centralized location. The OT Visibility dashboard lets you the access your OT device data.
locale: en-US
release: yokohama
product: Industrial Workspace
classification: industrial-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Dashboard Library in the Industrial Workspace, Explore, Industrial Workspace, Operational Technology]
---

# Operational Technology Visibility dashboard

The Operational Technology \(OT\) Visibility dashboard helps you manage your OT device in a centralized location. The OT Visibility dashboard lets you the access your OT device data.

## OT Visibility dashboard overview

The OT Visibility dashboard is a centralized location in the Industrial Workspace. You can use this dashboard to review your Operational Technology Manager and Industrial Process Manager data. You can also use it to review or edit the detailed information for the OT devices and equipment model entities in your OT network.

With the OT Visibility dashboard, you can achieve the following:

-   Understand what OT device information changed in your OT network in the past week.
-   View the progress of an OT device inventory through an industrial facility.
-   Analyze your OT devices in meaningful ways. For example, you can gain insights into how many of your production devices map to your production processes.

**Dashboard contents**

To access the OT device data in the OT Visibility dashboard, navigate to **All** &gt; **Industrial Workspace**, select the Dashboard Library \(![Dashboards icon](../../mftg-manufacturing-ot-vulnerability-response/image/dashboards-icon.png)\) icon, and then select the **Operational Technology Visibility**. To access the key performance indicators \(KPI\) graph for any tile that is described in the following table, select the number count or chart component in the tile.

The following table describes the OT device data that you can see on the different tiles on the dashboard.

<table id="table_odg_jht_xpb"><thead><tr><th>

Tile

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Updates from the past 7 days

</td></tr><tr><td>

New OT devices discovered

</td><td>

Number of the new OT devices that were discovered by Discovery for Operational Technology and other automated processes in your OT network during the last seven calendar days.

</td></tr><tr><td>

Inactive OT devices

</td><td>

Number of the OT devices that haven't appeared in your OT network during the last seven calendar days. These devices are considered inactive.

</td></tr><tr><td colspan="2">

OT devices overview

</td></tr><tr><td>

Total CMDB OT devices

</td><td>

 

</td></tr><tr><td>

Unclassed OT devices

</td><td>

Number of the OT devices in your OT network that aren't assigned with an OT device type category.

</td></tr><tr><td>

Unassigned OT devices

</td><td>

Number of the OT devices in your OT network that aren't assigned to a user.

</td></tr><tr><td>

Unmapped OT devices

</td><td>

Number of the OT devices in your OT network that are not mapped to any equipment model entity for your assigned site.**Note:** This tile is only available when the Industrial Process Manager is installed because it requires that your organization has an equipment model for mapping OT devices to a production process.

</td></tr><tr><td colspan="2">

OT devices by category

</td></tr><tr><td>

Supervisory systems

</td><td>

Number of the OT devices in your OT network that are assigned to a Supervisory systems category.

</td></tr><tr><td>

Control systems

</td><td>

Number of the OT devices in your OT network that are assigned to the Control systems category.**Note:** Control modules aren’t included in this number.

</td></tr><tr><td>

Field devices

</td><td>

Number of the OT devices in your OT network that are assigned to the Field devices category.

</td></tr><tr><td>

Computers and servers

</td><td>

Number of the OT devices in your OT network that are assigned to the Computers and servers category.

</td></tr><tr><td>

Network Gear

</td><td>

Number of the OT devices in your OT network that are assigned to the Network Gear category.

</td></tr><tr><td>

Industrial IoT

</td><td>

Number of the OT devices in your OT network that are assigned to the Industrial Internet of Things \(IoT\) category.

</td></tr><tr><td>

OT devices by Purdue level

</td><td>

Bar chart that indicates the number of OT devices in your OT network by their assigned Purdue level.**Note:** To learn more about the Purdue levels in the OT systems, see [https://subscription.packtpub.com/book/networking\_and\_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems](https://subscription.packtpub.com/book/networking_and_servers/9781788395151/1/ch01lvl1sec10/the-purdue-model-for-industrial-control-systems).

</td></tr><tr><td>

OT devices by type \(Top Level\)

</td><td>

Bar chart that categorizes the OT device data by the OT device types.

</td></tr><tr><td>

OT devices by manufacturer \(Top Level\)

</td><td>

Pie chart that indicates the number of OT devices in your OT network by their assigned manufacturer.

</td></tr><tr><td>

OT devices by criticality

</td><td>

Pie chart that indicates the number of OT devices in your OT network by their assigned criticality.

</td></tr></tbody>
</table>## Required roles to view the dashboard

To access the OT Visibility dashboard, you must have the **cmdb\_ot\_viewer** and **cmdb\_ot\_isa\_viewer** roles.

## Site filter

You can use the **Site** filter to search for and select the site that you want to view on the dashboard. To access and use the site filter, you must have the **cmdb\_ot\_isa\_viewer** role with access to the site you want to view.

For more information, see [Use the site filter](../../mftg-manufacturing-process-mgr/task/use-business-unit-and-site-filters.md).

**Parent Topic:**[Dashboard Library in the Industrial Workspace](../../operational-technology-management/concept/dashboard-library-industrial-workspace.md)

