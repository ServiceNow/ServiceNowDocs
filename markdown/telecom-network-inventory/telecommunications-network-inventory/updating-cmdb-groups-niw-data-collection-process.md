---
title: Update CMDB groups for use in the data collection process
description: Add or change the data that you see in a Network Inventory Workspace widget by using the CMDB Groups function. You create CMDB group codes as needed or modify the query conditions for existing ones. By changing the CMDB groups, you affect what data the collection process retrieves for the widgets on the Network Inventory Workspace landing page.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Customizing the content in your Network Inventory Workspace widgets, Reviewing and updating your network inventory with the Network Inventory Workspace, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Update CMDB groups for use in the data collection process

Add or change the data that you see in a Network Inventory Workspace widget by using the CMDB Groups function. You create CMDB group codes as needed or modify the query conditions for existing ones. By changing the CMDB groups, you affect what data the collection process retrieves for the widgets on the Network Inventory Workspace landing page.

## Before you begin

Role required: admin, cmdb\_query\_builder, itil, sn\_cmdb\_editor

## About this task

You must follow the standard CMDB group naming convention that is used for the Network Inventory Workspace widgets. To learn more, see the section called Standard CMDB groups and naming conventions for the Network Inventory Workspace widget data. To learn more about creating, updating, or naming CMDB groups, see [CMDB groups](https://www.servicenow.com/docs/access?context=cmdb-groups&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Groups**.

2.  To view the listings of the CMDB groups that are associated with the Network Inventory Workspace widgets, see the following table.

    |Type of CMDB Group|Description|
    |------------------|-----------|
    |**All CMDB groups created for Network Inventory Workspace widgets**|In the **Description** field, enter `*tni`.|
    |**Only CMDB groups created for the Network equipment by manufacturer widget**|In the **Group Name** field, enter `*manufact`.|

3.  In the Group Naming listing, select a CMDB group for an existing manufacturer in the All domain.

    For example, select **All Ericsson Manufacturer Equipment**. The CMDB Group form appears.

4.  In the **Name** field, overwrite Ericsson with the name of the manufacturer that you want to add.

    For example, change **All Ericsson Manufacturer Equipment** to `All Dell Manufacturer Equipment`.

5.  Click the **CMDB Group Contains Encoded Queries \(n\)** tab, where \(n\) represents the number of encoded queries for the CMDB group.

6.  In the **CMDB Group Contains Encoded Queries \(n\)** tab, in the **Class** field, select **cmdb\_ci\_ni\_telco\_equipment**.

    After you select the CMDB group, the encoded query detail for the selected CMDB group class appears.

7.  In the **Condition** field, overwrite Ericsson with the name of the manufacturer that you want to add.

    For example, overwrite Ericsson with `Dell`.

8.  Click **Update**.

9.  Repeat these steps for each of the remaining network domains for the new manufacturer.

    In the following table, you would create the following CMDB groups for the remaining network domains. These groups are based on the CMDB codes for Ericsson.

    |Existing CMDB Group|Existing CMDB Group|
    |-------------------|-------------------|
    |Core Ericsson Manufacturer Equipment|Core Dell Manufacturer Equipment|
    |Mobility Ericsson Manufacturer Equipment|Mobility Dell Manufacturer Equipment|
    |Telco Ericsson Manufacturer Equipment|Telco Dell Manufacturer Equipment|


## Result

After the data collection process runs for the Network Inventory Workspace, the new network manufacturer appears in the pie chart in the Network Equipment by manufacturer widget. The new CMDB group includes the network equipment records that are assigned to your new manufacturer.

**Parent Topic:**[Customizing the content in your Network Inventory Workspace widgets](../concept/customizing-content-in-your-network-inventory-workspace-widgets.md)

**Related topics**  


[Network Inventory Workspace](../concept/exploring-network-inventory-workspace.md)

