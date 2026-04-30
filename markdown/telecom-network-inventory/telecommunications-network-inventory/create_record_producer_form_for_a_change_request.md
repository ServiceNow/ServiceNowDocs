---
title: Assign a record producer form to a change model
description: Assign a record producer to a change request by using a decision table in the Telecommunications Network Inventory application.
locale: en-US
release: xanadu
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring decision tables for Telecommunications Network Inventory, Configuring Telecommunications Network Inventory, Telecommunications Network Inventory]
---

# Assign a record producer form to a change model

Assign a record producer to a change request by using a decision table in the Telecommunications Network Inventory application.

## Before you begin

Role required: sn\_ni\_core.inventory\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**.

2.  Select the **TNI Change Model To Record Producer Policy** decision table.

3.  In the conditions section of the decision table, select the **Add new decision row** button.

4.  Select a change model from the **value** field of the **Change model** column.

5.  Select a record producer to assign to the selected change model from **Record Producer** column.


## Result

When you select **Changes** &gt; **All** and the **Next** button for the added change model, the assigned record form is displayed.

**Note:** All record producer form inputs can be seen in the Variables section of the **Details** tab. You can view and update the details as required.

## What to do next

You can also assign a record producer to a change task of a change request. To learn more, see [Assign a record producer form for a request type of a change task](assign_record_producer_form_for_a_change_task_of_a_change_request.md).

**Parent Topic:**[Configuring decision tables for Telecommunications Network Inventory](../concept/decision_tables.md)

