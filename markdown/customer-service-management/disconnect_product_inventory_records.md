---
title: Disconnect product inventory records
description: Perform the Disconnect operation on a single product inventory record that results in the creation of an order or quote on the CRM Workspace so that you can permanently disconnect a product and its services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/disconnect\_product\_inventory\_records.html
release: australia
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Disconnect product inventory records

Perform the **Disconnect** operation on a single product inventory record that results in the creation of an order or quote on the CRM Workspace so that you can permanently disconnect a product and its services.

## Before you begin

Role required: Order admin \(sn\_ind\_tmt\_orm.order\_admin\) or Order agent \(sn\_ind\_tmt\_orm.order\_agent\)

## About this task

After performing the **Disconnect** action, a disconnect order is created and the fulfillment process for the order begins. This fulfillment flow marks the order as **Complete** and updates the product inventory records.

**Note:** For a consumer, you can disconnect one product inventory record at a time. Sign in as an order agent, open the consumer record, select **Product Inventories**, select an active or suspended record, and then select **Disconnect**.

The disconnect order includes the product's pricing values. This includes the pricing method, periodicity, price list, unit net price, one-time price, monthly and annual recurring prices, and the cumulative prices. The order reflects the pricing based on the selected price list and configuration.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts or Consumer**.

3.  Open the account that the product inventory belongs to.

4.  Navigate to the **Product Inventories** related list and select one or more root product inventory records.

    **Note:** You can do the **Disconnect** action only on one root sold product whose state is **Active** or **Suspended**, and the option is enabled only if the root product inventory with **Active** or **Suspended** states are selected and is disabled for any other state.

5.  Select **Disconnect**.

6.  In the Disconnect window, enter when you want the disconnection to start in the **Start date and time** field.

7.  Add a reason for a disconnection in the **Reason for disconnection** field.

8.  Select **Disconnect**.


## Result

An order to disconnect the product inventory record is created.

