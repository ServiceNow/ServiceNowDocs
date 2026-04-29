---
title: Create physical connection using design and assign
description: Create an physical connection record using the design and assign function in the Telecommunications Network Inventory application. By creating the physical connection and its related inventory records, you can fulfill an order request for an equipment record.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Design &amp; Assign Network, Use, Telecommunications Network Inventory]
---

# Create physical connection using design and assign

Create an physical connection record using the design and assign function in the Telecommunications Network Inventory application. By creating the physical connection and its related inventory records, you can fulfill an order request for an equipment record.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin, sn\_ni\_core.inventory\_agent

## About this task

When you create a physical connection, it creates the corresponding configuration item \(CI\) records in the Physical Connection \[cmdb\_ci\_ni\_physical\_link\] table. To learn more, see [Data model](../concept/uses-for-network-inventory-data.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the list icon \(![List icon](../image/ni-workspace-list-icon.png)\), and then go to **Changes** &gt; **All**.

3.  Select the **New** button.

4.  Select **Create Physical Connection**.

5.  Select **Next**.

    A change request is created.

6.  On the **Details** tab, fill in the fields.

    For a description of the field values, see [Change request and change task forms](../concept/change_request_forms.md).

7.  Select **Save**.

    A change task is created.

8.  Open the change task.

9.  On the **Task Attributes** tab, fill in the fields.

    To learn more, see [Task attributes in Create physical connection form](../reference/task-attributes-create-physical-connection-form.md).

10. Select **Submit**.


**Parent Topic:**[Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md)

