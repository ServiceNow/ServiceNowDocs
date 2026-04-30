---
title: Create a cable record by using design and assign
description: Create a cable record using the design and assign function in the Telecommunications Network Inventory application. By creating the cable and related strand records, you can fulfill an order request for a fiber optical cable record.DOC1090321
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a change request from Network Inventory Workspace, Instantiating your network inventory by using design and assign, Using Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create a cable record by using design and assign

Create a cable record using the design and assign function in the Telecommunications Network Inventory application. By creating the cable and related strand records, you can fulfill an order request for a fiber optical cable record.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you instantiate a cable template, it creates the corresponding configuration item \(CI\) records in the Fiber Optical Cable \[cmdb\_ci\_fiber\_optical\_cable\] and Fiber Strand \[cmdb\_ci\_fiber\_strand\] tables. To learn more about the cable data model, see [Data model for Telecommunications Network Inventory](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Add cable**.

5.  Select **Next**.

6.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

7.  Select **Save**.

    A change task is created.

8.  Open the change task.

9.  On the **Task Attribute** tab, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |A end termination|Network site where this cable is starting from.|
    |Z end termination|Network site where the cable is ending.|
    |Inventory template|Name of the inventory template for the card model.|

10. Select **Submit**.


## Result

The cable and related strand records are created.

**Parent Topic:**[Create a change request from Network Inventory Workspace](create_a_change_request_in_tni.md)

