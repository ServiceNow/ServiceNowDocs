---
title: Jeopardy Management setup overview
description: Learn about how to set up and configure Jeopardy Management for Order Management for Telecommunications.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Jeopardy Management, Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Jeopardy Management setup overview

Learn about how to set up and configure Jeopardy Management for Order Management for Telecommunications.

During design time, fulfillment managers must complete the following Jeopardy Management configuration and setup steps:

-   Define Fulfillment Subflows: Creates an Orchestration plan for each specification. Fulfillment managers can use demo data flow actions to ensure that order task relationships are created.
-   Define Service Level Agreements \(SLA\) Definitions: SLA definitions track how much time each order task takes to complete.
-   Build Decision Tables: Build decision tables that contain information including order task duration, jeopardy level assignment, and jeopardy enablement.

## Define Fulfillment Subflows

To use Jeopardy Management, fulfillment managers must either reconfigure existing fulfillment subflows or create subflows for each specification.

-   Order tasks are created up front: Subflows that are configured for jeopardy management create order tasks up front and in a Draft state.
-   Use Create Order Planned Task flow action: In Decision Builder, use the Create New Order tasks.
-   Create task relationships: After all the order tasks are created, fulfillment managers create order task relationships.
-   Define fulfillment progress: After all order tasks and task relationships are created, define the fulfillment progress.

## Create SLA Definitions

SLA definitions and SLA Processing flows are linked to tasks in a fulfillment plan and track and report on the time jeopardy-enabled tasks take to complete. See  for more information.

-   SLA Definitions: Set start condition, pause condition, cancel condition, and reset conditions according to use case.
-   SLA Durations: Durations are specified so that tracking can be achieved when task SLA is created.
-   SLA Processing flow should be defined: Customer can use demo data flows, which trigger jeopardy level calculation for order tasks at 50%, 75%, 100% task SLA progression.

## Link Jeopardy Management to Product and Service Specifications using Decision Builder

Decision tables are used to link and configure Jeopardy Management to product and service specifications in Order Management for Telecommunications.

-   Order Line Item Jeopardy Level Calculation: Returns Jeopardy Level for order line item based on delayed percentage of tasks.
-   Order Task Jeopardy Level Calculation: Sets a task's jeopardy level based on percentage task completion.
-   Order Task Duration Assignment Policy: Defines the order duration and task SLA definition.
-   Order Jeopardy Enablement Policy: Defines if a specification has jeopardy enabled.

