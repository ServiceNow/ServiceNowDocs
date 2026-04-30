---
title: Create capacity function
description: Create a capacity function in the Telecommunications Network Inventory application. You can use this function to calculate the capacity of your network assets.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring capacity management, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create capacity function

Create a capacity function in the Telecommunications Network Inventory application. You can use this function to calculate the capacity of your network assets.

## Before you begin

Make sure that the Capacity Management plugin is installed with the Telecommunications Network Inventory application.

Role required: sn\_ni\_core.inventory\_admin

## About this task

Create a capacity function to calculate the maximum, occupied, and available capacity of your network assets. You can use different strategies to calculate the capacity. When you create a capacity function, it stores the record in the Capacity Function \[sn\_cap\_mgmt\_function\] table.

The system selects the capacity functions based on their priority to calculate the capacity. The following points are considered to set the priority for capacity calculations.

-   If two capacity functions have same Function type and Measurement type, the one with the lowest Order value gets prioritized.
-   If two capacity functions have same Function type, Measurement type, and Order, the one that was most recently updated is given priority.

## Procedure

1.  Navigate to **All** &gt; **Capacity Management** &gt; **Functions**.

2.  Select **New**.

3.  On the form, fill in the fields.

    To learn more about the fields, see [Capacity Function form](../reference/capacity-function-form.md).

4.  Select **Submit**.


## Result

The capacity function record is created.

## What to do next

You can use the function for capacity calculation or use it within the definition record to determine the capacity. To learn more about how to create a capacity definition, see [Create capacity definition](create-capacity-definition.md).

**Parent Topic:**[Configuring capacity management](../concept/configuring-capacity-management.md)

**Related topics**  


[Capacity management](../concept/capacity-management-reporting.md)

