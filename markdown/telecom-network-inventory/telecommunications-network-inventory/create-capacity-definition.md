---
title: Create capacity definition
description: Create a capacity definition in the Telecommunications Network Inventory application. You can use multiple functions in the capacity definition to calculate the capacity of your network assets.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring capacity management, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Create capacity definition

Create a capacity definition in the Telecommunications Network Inventory application. You can use multiple functions in the capacity definition to calculate the capacity of your network assets.

## Before you begin

-   Make sure that the Capacity Management plugin is installed with the Telecommunications Network Inventory application.
-   You create capacity function records.

Role required: sn\_ni\_core.inventory\_admin

## About this task

The capacity definition is an asynchronous way to trigger the capacity functions. You can use multiple functions in the capacity definition to calculate the maximum, occupied, and available capacity of your network assets. When you create a capacity definition, it stores the record in the Capacity Definition \[sn\_cap\_mgmt\_definition\] table.

## Procedure

1.  Navigate to **All** &gt; **Capacity Management** &gt; **Definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

    To learn more about the fields, see [Capacity Definition form](../reference/capacity-definition-form.md).

4.  Select **Submit**.


## Result

The capacity definition record is created.

## What to do next

You can use the definition for capacity calculation. When you run the capacity definition, it creates the metric and the results aggregate to it. You can navigate to **All** &gt; **Capacity Management** &gt; **Metrics** and open the capacity metric record, which you want to see the details.

**Parent Topic:**[Configuring capacity management](../concept/configuring-capacity-management.md)

**Related topics**  


[Capacity management](../concept/capacity-management-reporting.md)

