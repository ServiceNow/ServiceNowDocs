---
title: Order Management for Telecommunications integration
description: Use a Telecommunications Network Inventory decision table to integrate the Telecommunications Network Inventory and Order Management for Telecommunications applications.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Decision tables, Configure, Telecommunications Network Inventory]
---

# Order Management for Telecommunications integration

Use a Telecommunications Network Inventory decision table to integrate the Telecommunications Network Inventory and Order Management for Telecommunications applications.

## Before you begin

-   Configure the change model and order task variables to enable the Order Management for Telecommunications - Telecommunications Network Inventory integration.
-   Role required: sn\_ni\_core.inventory\_admin

## About this task

You can create, review, update, and remove a decision entry.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**

2.  Select the **TNI Record Producer and Change model policy** decision table.

3.  Create a decision entry in the decision table for an order task.

    For this entry, you must complete the following items:

    -   Order task.
    -   Condition for the order task. In the decision table, search and select an Order Task.Request Type condition for the order task. The **Answer** field is filled based on the condition that you select.
    -   Record Producer.
    -   Change model.
    If all the conditions are met, a change request is created for the order task that needs the inventory actions. In this change request, the order task is assigned as its parent. The new change request is in the related list of the order task. This task redirects you to the change request from the OMT task page.

4.  Transfer the order characteristics to the Telecommunications Network Inventory application by creating an entry in the TNI Record Producer Variable Policy decision table.

    The change tasks are created for the configuration items.


## TNI Design Assign of Fiber Broadband

Let's say that you add a service order with the category broadband service. After you make this addition, the TNI Design Assign of Fiber Broadband flow of the Service Order Fulfillment Policy triggers. As part of this flow, in the TNI Record Producer and Change model policy decision table, an allocate and assign Customer Premises Equipment \(CPE\) order task is created with a Gigabyte Passive Optical Network \(GPON\) broadband record producer for the GPON broadband change model.

To transfer the order characteristics in the TNI Record Producer Variable Policy decision table, the order characteristics map with the record producer.

**Parent Topic:**[Configuring decision tables](../concept/decision_tables.md)

