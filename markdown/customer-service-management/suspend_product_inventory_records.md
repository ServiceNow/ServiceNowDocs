---
title: Suspend product inventory records
description: Perform the Suspend operation on a single product inventory record that results in the creation of an order or quote on the CRM Workspace. By suspending a product inventory, you can pause your services for a period of time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/suspend\_product\_inventory\_records.html
release: australia
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Suspend product inventory records

Perform the **Suspend** operation on a single product inventory record that results in the creation of an order or quote on the CRM Workspace. By suspending a product inventory, you can pause your services for a period of time.

## Before you begin

Role required: Order admin \(sn\_ind\_tmt\_orm.order\_admin\) or Order agent \(sn\_ind\_tmt\_orm.order\_agent\)

## About this task

After performing the **Suspend** action, a suspend order is created and the fulfillment process for the order begins. This fulfillment flow marks the order as **Complete** and updates the product inventory records.

**Note:** For a consumer, you can suspend one product inventory record at a time. Sign in as an order agent, open the consumer record, select **Product Inventories**, select an active record, and then select **Suspend**.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts or Consumer**.

3.  Open the account that the product inventory belongs to.

4.  Navigate to the **Product Inventories** related list and select one or more root product inventory records.

    **Note:** You can do a **Suspend** action on a single or multiple root sold products only if it is in the **Active** state and is disabled for any other state.

5.  Select **Suspend**.

6.  In the Suspend window, in the **Start date and time** field, enter the start date and time that you want to start the suspension.

    **Note:** If you fill in only the **Start date and time** field, suspend order line items are created. Resume order line items are created within the same order header if the **End date and time** field is also filled in. You can also indefinitely suspend a product inventory without creating a resume order by not entering an end date.

7.  If you know when you want to end the suspension, enter the **End date and time** field.

8.  Add a reason for a suspension in the **Reason for suspension** field.

    For example, a disturbance due to a renovation can be a reason for suspension.

9.  Select **Suspend**.


## Result

An order to suspend the product inventory record is created.

