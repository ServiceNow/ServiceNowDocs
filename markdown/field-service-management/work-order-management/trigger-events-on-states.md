---
title: Trigger events on state changes
description: You can configure a state flow to trigger a registered system event when a task transitions from a starting state to a specified end state. For example, you can use events to trigger email notifications and create script actions.
locale: en-US
release: xanadu
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Customizing State flows, Configuring work orders, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Trigger events on state changes

You can configure a state flow to trigger a registered system event when a task transitions from a starting state to a specified end state. For example, you can use events to trigger email notifications and create script actions.

## Before you begin

Role required: admin

## About this task

When you attach an event to a state flow, the ServiceNow system creates a business rule called **State Flow Events for &lt;table name&gt;** for the table specified in the state flow. If you specify a start and end state, the business rule executes when the record transitions from the start state to the end state. If the state flow only specifies an end state, the business rule executes whenever that end state is reached. The system creates one business rule for all state flows containing events on a single table. When all events or all state flows on a table are deleted, the system deletes the business rule.

To create an event that fires when a work order task moves from a starting state of **Work in Progress** to an end state of **Closed Complete**.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **State Flows** &gt; **Work Task Flows**.

2.  Select the Work Order Task table called Work Order Task \[wm\_task\].

3.  Select **New**.

4.  Open the state flow record named **Close Complete**.

5.  Select `task.closed` in the **Event** field and save your changes.

    The ServiceNow system automatically creates a business rule called **State Flow Events for wm\_task**.


