---
title: Create or modify Map Related Items
description: The Map Related Items module relates referenced CIs to one another, which allows them to be displayed in a Dependency Views map.
locale: en-US
release: australia
product: Dependency Views
classification: dependency-views
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Administer, Dependency Views, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or modify Map Related Items

The Map Related Items module relates referenced CIs to one another, which allows them to be displayed in a Dependency Views map.

## Before you begin

Role required: sn\_cmdb\_admin or admin

## About this task

The base system configuration includes the following tables and relates them to items in the Computer \[cmdb\_ci\_computer\] and Server \[cmdb\_ci\_server\] tables.

-   Disk \[cmdb\_ci\_disk\]
-   Network Adapter \[cmdb\_ci\_network\_adapter\]
-   Database \[cmdb\_ci\_database\]

Some additional referenced CIs that can be related in this manner are file systems and running processes.

In the following example, computer nodes in the map are related to network adapter nodes if the **Configuration Item** field of the adapter records reference the specific CI node. Access or create a network adapter record from the Network Adapter related list in the cmdb\_ci\_computer record.

![CIs related by depencency.](../image/NGBSMRelatedItems2.png "Dependency Views Configuration Item field")

The Dependency Views map for the \*JEMPLOYEE-IBM computer shows the network adapter attached to the computer.

![Dependency Views map displaying related CIs.](../image/DepViewsExample01.png "Dependency Views map Related Items example")

You can configure Dependency Views to display CIs that have no relationship record, but are related to other CIs by reference fields.

## Procedure

1.  Navigate to **All** &gt; **Dependency Views** &gt; **Map Related Items**.

2.  Click **New** to create a new related item, or click in the row of an existing CI to modify an existing map related item.

3.  On the form, fill in the fields.

    See the Related Items form table.

4.  Click **Submit** to enter a new map related item or click **Update** to modify an existing map related item.

    |Control|Description|
    |-------|-----------|
    |Configuration item|CI that represents the base node or a CI in a table that extends the base node table. In the base system, the configuration item that represents the base node is Computer \[cmdb\_ci\_computer\], which includes all types of workstations and servers.|
    |Related item|Table name of the related item. Only the cmdb\_ci table and tables that extend it are displayed in the choice list.|
    |Related field|Field that links this related item to the configuration item. In many cases, the appropriate value is automatically populated in the field after the first two fields are selected. Select the drop-down menu for additional options.|
    |Active|Check box to enable or disable this record.|


**Parent Topic:**[Administer Dependency Views](../topic/p_AdministerNGBSM.md)

**Related topics**  


[Create or modify map indicators](t_CreateModifyNGBSMMapIndicators.md)

[Create or modify map icons](t_CreateModifyNGBSMMapIcons.md)

[Create a predefined filter](create-predefined-filter.md)

[Set a predefined filter as default](set-predefined-filter-default.md)

[Create or modify Dependency Views menu actions](t_CreateModifyNGBSMMenuActions.md)

[Condition and script parameters for menu actions](../reference/condition-script-parameters.md)

[Create or edit a dependency type](t_CreateMapScript.md)

