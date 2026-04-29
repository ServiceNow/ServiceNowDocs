---
title: Jeopardy Management
description: Jeopardy Management is a risk assessment tool that monitors fulfillment tasks, assesses the risk level, and alerts fulfillment managers when the assigned task time is in jeopardy.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-26"
reading_time_minutes: 3
breadcrumb: [Order management, Explore, Sales and Order Management]
---

# Jeopardy Management

Jeopardy Management is a risk assessment tool that monitors fulfillment tasks, assesses the risk level, and alerts fulfillment managers when the assigned task time is in jeopardy.

## Overview of Jeopardy Management

Jeopardy Management consists of multiple components in the Order Management application that work together to monitor and report on task completion time in a fulfillment plan.

If a task is taking longer than expected, the system assesses the percentage of delay and assigns a risk level.

In Order Management, some customer orders are expected to be fulfilled in a committed time frame. The time commitment may be part of a contract that the customer and customer service provider \(CSP\) have signed to ensure delivery and assurance of products and services. To fulfill an order in the target date and time, a CSP depends on order management systems to monitor the fulfillment progress. Jeopardy Management proactively identities any delays and shares alerts, which can be addressed by fulfillment managers.

Jeopardy Management provides proactive risk management for the order fulfillment process through the following steps:

1.  Monitor order fulfillment progress.
2.  Predict jeopardy and risk for domain orders and order tasks.
3.  Make jeopardy information available to users.
4.  Fulfillment managers resolve tasks in jeopardy.

## How Jeopardy Management works

Jeopardy Management works by tracking tasks in an order fulfillment process. Order task relationships are created and task durations are set. Planned tasks are set in the Draft state and have a start time and an end time. As an order task is being fulfilled, any delays in the task's assigned amount of time triggers a jeopardy alert.

Jeopardy Management uses the following components to monitor and manage risk in order fulfillment:

-   **Define subflows and decision tables**
    -   Define subflows that create order tasks upfront and define task relationships.
    -   Configure jeopardy policy decision tables.
-   **Monitor order fulfillment progress**
    -   Define and launch SLA for order tasks.
    -   Monitor fulfillment progress and closure of domain orders and order tasks.
-   **Predict jeopardy and risk**
    -   Leverage planned task date fields and date roll-up logic to produce timelines for order task fulfillment progression.
    -   Monitor the progress of each order task and produce jeopardy information.
    -   Roll up jeopardy date changes for all order entities.
-   **Share jeopardy information**

    Use the order forms, list, and orchestration UI forms to show jeopardy details for orders, domain orders, and order tasks to prioritize tasks to take action.

-   **Resolve tasks in jeopardy**

    Based on jeopardy condition, customers can implement notifications or other logic as required based on the jeopardy level flag on each entity jeopardy.


## Jeopardy Management alert levels

In Jeopardy Management, the fulfillment manager can set different levels of alerts for each task. As the system monitors task duration, any delay triggers adjustments to the jeopardy level of predecessor and successor tasks in the fulfillment plan.

The following table compares how Jeopardy Management assesses risk levels across tasks in a fulfillment workflow for three scenarios: expected, on-time, and delayed.

|Scenario|Product order|Task A|Task B|Task C|Task D|
|--------|-------------|------|------|------|------|
|Expected|Duration: 48 hours|12 hours|12 hours|12 hours|12 hours|
|Scenario 1: On-time|Duration: 34 hours|10 hours|10 hours|8 hours|6 hours|
|Scenario 2: Delayed|Duration: uncertain|10 hours|18 hours \(in jeopardy, task delayed\)|Uncertain fulfillment time|Uncertain fulfillment time|

The following table shows how Jeopardy Management assesses risk levels for tasks in a fulfillment workflow and the impact on the successor tasks.

|Scenario|Task status|Risk level|Impact on successor tasks|
|--------|-----------|----------|-------------------------|
|Task completed within the expected time|On time|None|No adjustment to successor task risk levels|
|Task slightly delayed but within the acceptable threshold|At risk|Low|Successor tasks flagged as low risk|
|Task significantly delayed, exceeding the acceptable threshold|Delayed|High|Successor tasks escalated to high risk; jeopardy alert triggered|

Jeopardy Management assesses all tasks in a workflow and adjusts the risk level for tasks that occur later in the workflow. In the delayed scenario, a delay in Task B causes the fulfillment time for all successor tasks to become uncertain, and the product order duration can no longer be determined.

## What to do next

For information on configuring and using Jeopardy Management, see:

-   [Configuring Jeopardy Management](configuring-jeopardy-management.md)
-   [Monitoring order jeopardy](../task/monitoring-jeopardy-management.md)

