---
title: Disconnect product inventory records
description: Perform the Disconnect operation on single or multiple product inventory records that result in the creation of orders or quotes on the CSM Configurable Workspace so that you can permanently disconnect a product and its services.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Disconnect product inventory records

Perform the **Disconnect** operation on single or multiple product inventory records that result in the creation of orders or quotes on the CSM Configurable Workspace so that you can permanently disconnect a product and its services.

## Before you begin

Role required: Order admin \(sn\_ind\_tmt\_orm.order\_admin\) or Order agent \(sn\_ind\_tmt\_orm.order\_agent\)

## About this task

After performing the **Disconnect** action, a disconnect order is created and the fulfillment process for the order begins. This fulfillment flow marks the order as **Complete** and updates the product inventory records.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the product inventory belongs to.

4.  Navigate to the **Product Inventories** related list and select one or more root product inventory records.

    **Note:** You can do the **Disconnect** action only on one root sold product whose state is **Active** or **Suspended**, and the option is enabled only if the root product inventory with **Active** or **Suspended** states are selected and is disabled for any other state.

5.  Select **Disconnect**.

6.  In the Disconnect window, enter when you want the disconnection to start in the **Start date and time** field.

7.  Add a reason for a disconnection in the **Reason for disconnection** field.

8.  Select **Disconnect**.


## Result

An order to disconnect the product inventory record is created.

