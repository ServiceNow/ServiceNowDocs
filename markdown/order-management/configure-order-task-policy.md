---
title: Configure the customer order task policy using Decision Tables
description: Define conditions for automatic generation of order header tasks and top order line item tasks by adding rows to the Customer Order Task Policy in Decision Tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/configure-order-task-policy.html
release: australia
topic_type: task
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [Order management, Configure, Sales Customer Relationship Management]
---

# Configure the customer order task policy using Decision Tables

Define conditions for automatic generation of order header tasks and top order line item tasks by adding rows to the Customer Order Task Policy in Decision Tables.

## Before you begin

Role required: admin or decision\_table\_admin

## About this task

The Customer Order Task Policy decision table determines which order header tasks and top order line item tasks are automatically generated, and at which stage of the order life cycle they are triggered. Each row in the table maps a set of conditions to a subflow that creates the task.

Order header task conditions reference order-level parameters, such as account or order action. Top order line item task conditions reference parameters at the order line item level, such as product offering or order line item action.

For header tasks, specify the stage at which the task is generated:

-   after order submission
-   after order approval
-   after order fulfillment

## Procedure

1.  Navigate to **All** &gt; **Decision Builder**.

2.  Select the **Customer Order Task Policy** decision table.

3.  Select **Add new decision row** to add a condition row.

4.  In the conditions section, set the values for the fields that determine when the task is generated.

    |Field|Description|
    |-----|-----------|
    |Triggered state|Select the order life cycle stage at which the task is generated: **Submitted**, **Post approval**, or **Post fulfillment**.|
    |Order action|Order action that triggers task generation, such as **Add**.|
    |Product offering|Product offering associated with the order line item. Applies to top order line item tasks only.|
    |Account|Customer account associated with the order. Applies to order header tasks.|

5.  In the results section, select the subflow to run when the conditions are met.

    The subflow requires the **Create Order Header Task** flow action for order header tasks, or the **Create Top OLI Task** flow action for top order line item tasks.

6.  Select **Save**.


## Result

The policy row is saved. When an order matches the configured conditions at the specified triggered state, the associated subflow runs and creates the order header task or top order line item task.

## What to do next

To control whether open order header tasks block order state transitions, set **sn\_ind\_tmt\_orm.block\_order\_appro\_complet\_until\_tasks\_complete** system in **All** &gt; **System Properties**.

**Parent Topic:**[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-configuring.md)

**Related topics**  


[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md)

[Using Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/using-order-management.md)

