---
title: Assign a record producer form for a request type of a change task
description: Assign a record producer to a change task of a change request with the help of a decision table in Telecommunications Network Inventory application.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring decision tables for Telecommunications Network Inventory, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Assign a record producer form for a request type of a change task

Assign a record producer to a change task of a change request with the help of a decision table in Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin

## About this task

**Note:** By default, the Telecommunications Network Inventory application added request types for create equipment, create physical connection, create logical connection, and add interface card in this decision table.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Select the **TNI Request type to Record Producer Policy** decision table.

3.  In the Conditions section of the decision table, select the **Add new decision row** button.

    On the **Change Tasks** tab of the added change model, when you select a change task, the assigned record producer form is displayed on the **Task attributes** tab.

4.  Select a change task from the **value** field of the **Request Type** column.

5.  Select a record producer to assign to the selected change task from **Record Producer** column.


## What to do next

Create a network instance instantiation. For information, see [Instantiating your network inventory by using design and assign](../concept/instantiate-asset-using-template-relationship-model.md).

**Parent Topic:**[Configuring decision tables for Telecommunications Network Inventory](../concept/decision_tables.md)

