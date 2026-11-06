---
title: Resume product inventory records
description: Perform the Resume operation on a single product inventory record that results in the creation of an order or quote on the CRM Workspace. By resuming a product inventory, you can restart a product or service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/resume\_product\_inventory\_records.html
release: australia
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Product inventory configurations, Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Resume product inventory records

Perform the **Resume** operation on a single product inventory record that results in the creation of an order or quote on the CRM Workspace. By resuming a product inventory, you can restart a product or service.

## Before you begin

Role required: Order admin \(sn\_ind\_tmt\_orm.order\_admin\) or Order agent \(sn\_ind\_tmt\_orm.order\_agent\)

## About this task

After performing the **Resume** action, a resume order is created and the fulfillment process for the order begins. This fulfillment flow marks the order as **Complete** and updates the product inventory records.

**Note:** For a consumer, you can resume one product inventory record at a time. Sign in as an order agent, open the consumer record, select **Product Inventories**, select a suspended record, and then select **Resume**.

## Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, select **Customer** &gt; **Accounts or Consumers**.

3.  Open the account that the sold product belongs to.

4.  Navigate to the **Product Inventories** related list and select one or more root product inventory records.

    **Note:** You can do a **Resume** action on the root product inventory only if it is in the **Suspended** state.

    The **Resume** option is enabled only if the root product inventory with **Suspended** state is selected and is disabled for any other state.

    The option is disabled if you select a child sold product.

5.  Select **Resume**.

6.  In the Resume window, in the **Start date and time** field, enter when you want to resume the product inventory.

7.  Select **Resume**.


## Result

An order for resuming the product inventory records are created.

