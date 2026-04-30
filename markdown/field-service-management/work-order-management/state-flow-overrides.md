---
title: State flow dictionary overrides
description: A dictionary override in a state flow defines the starting state for all new records in a specific table. You set an override in tables that extend a base table only, so that your customizations are applied only to the extended table.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Define state flows, Work orders, Work orders and tasks, Configure, Field Service Management]
---

# State flow dictionary overrides

A dictionary override in a state flow defines the starting state for all new records in a specific table. You set an override in tables that extend a base table only, so that your customizations are applied only to the extended table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **Field Service** then choose one of the following:

    -   **Work Order Flows**
    -   **Work Task Flows**
2.  In a state flow record, select an **Ending state**.

    This is the override value which becomes the starting state for all new records in the table named.

3.  Click **Create Default Value**.

    The system populates the **Dictionary override** field with a value of state, which is the field in the task table affected by the override. The Dictionary override field is read-only. After the override is created, the system hides the **Create Default Value** button on all subsequent state flow forms for that table.


