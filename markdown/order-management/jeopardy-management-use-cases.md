---
title: Jeopardy Management use cases
description: Jeopardy Management use cases help you explore and understand how Jeopardy Management works in different scenarios in Order Management.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Jeopardy Management, Order management, Configure, Sales Customer Relationship Management]
---

# Jeopardy Management use cases

Jeopardy Management use cases help you explore and understand how Jeopardy Management works in different scenarios in Order Management.

## Design-time use cases

Design-time use cases explain some of the scenarios around configuring and setting up Jeopardy Management for Order Management.

**Use case: Configure business logic and workflows**

System admins want to configure and define fulfillment subflows with Jeopardy Management actions and logic.

Define jeopardy logic using Workflow Studio to links product specifications and a fulfillment workflow.

-   Create planned order tasks in Draft state.
-   Set task relationships.
-   Create placeholder for domain orders.
-   Create relationships for order tasks in a domain order.
-   Set order task state.
-   Configure jeopardy decision tables.

## Run-time use cases

Run-time use cases explain some of the scenarios around running and monitoring Jeopardy Management for Order Management.

**Use Case: Support predictive jeopardy that monitors customer orders**

Fulfillment agents and managers use jeopardy management workflows to monitor the potential risk of an order missing a customer due date.

-   Calculate planned task completion dates and estimated dates.
-   Monitor order tasks against service level agreements \(SLA\)s.
-   Trigger SLA thresholds for order task and order line items.
-   Update jeopardy levels as needed in the order entry forms.
-   Roll up planned dates for order tasks that complete.

**Use Case: Support staggered order decomposition and Jeopardy Management**

Fulfillment managers and agents expect that when a staggered order decomposition occurs, each occurrence of a staggered order line item causes the Jeopardy Management workflow logic to restart.

-   Completed decomposed order line items, the Jeopardy Management workflow restarts when additional planned tasks are added.
-   New planned tasks get a task SLA assigned, which is benchmarked for all tasks repeated, and includes the date roll ups.

**Use Case: Support inflight orders and Jeopardy Management**

Fulfillment managers and agent want Jeopardy Management to pause orders. When the order revision is approved, the jeopardy monitoring restarts.

-   Revision in progress and all tasks are on hold: jeopardy monitoring halts.​
-   Order revisions approved: task states go from on hold to their previous state and upcoming tasks move to a scheduled state​.
-   Jeopardy logic recalculates dates: planned dates and estimated or expected dates​.
-   Dates are benchmarked​.
-   Date roll up logic run and reflects the new start and end dates for planned and estimated dates.

