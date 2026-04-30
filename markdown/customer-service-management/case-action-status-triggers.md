---
title: Actionable case flows
description: Actionable case flows contain predefined user actions that automatically create and resolve blocking tasks for customer service cases.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Administering case action status, Administer, Customer Service Management]
---

# Actionable case flows

Actionable case flows contain predefined user actions that automatically create and resolve blocking tasks for customer service cases.

The Case Action Status plugin provides several actionable case flows that create and resolve blocking tasks for different case-related actions. These flows are enabled by default. If you don't want to create blocking tasks for a specific action, disable the associated flow.

To view these flows, navigate to **Customer Service** &gt; **Administration** &gt; **Actionable Case Flows**.

## Flow Designer actions

Case flows use the following predefined Flow Designer actions:

-   Add Blocking Task
-   Inactivate Blocking Task
-   Set Needs Attention Flag

## Flows for customer service cases

The case action status feature provides the following flows for customer service cases.

-   Create blocked by record if case needs customer information
-   Create blocked by record if Case Task is associated with case
-   Create blocked by record if Change Request is associated with case
-   Create blocked by record if SC Request is associated with case
-   Create blocked by record if Work Order is associated with case
-   Create blocked by record if Incident is associated with case
-   Create blocked by record if Problem is associated with case
-   Resolve blocked by record if Case Task is closed
-   Resolve blocked by record if Change Request is closed
-   Resolve blocked by record if Incident is closed
-   Resolve blocked by record if Problem is closed or Fix is communicated
-   Resolve blocked by record if Problem is closed or Fix/Workaround is communicated
-   Resolve blocked by record if SC Request is closed
-   Resolve blocked by record if user information is provided for case
-   Resolve blocked by record if Work Order is closed or cancelled
-   Set Needs Attention if additional comments are added by others
-   Update case when blocked by record is created
-   Update case when Needs attention field is toggled

## Flows for customer service orders

The case action status feature provides the following flows for customer service orders.

-   Create blocked by record if order case needs customer information
-   Resolve blocked by record if user information is provided for order case
-   Set Needs Attention if additional comments are added by others on order case
-   Update order case when Needs attention field is toggled

## Flows for problem records associated with a case

If a problem is associated with a case with the **Need task resolution** blocking reason, a case flow is provided to resolve the blocking task when a fix is communicated or the problem record is closed or cancelled.

If a problem is associated with a case with the **Need PRB workaround** blocking reason, a case flow is provided to resolve the blocking task when a workaround is provided or the problem record is closed or cancelled.

**Parent Topic:**[Administering case action status](../concept/customer-service-case-action-status.md)

