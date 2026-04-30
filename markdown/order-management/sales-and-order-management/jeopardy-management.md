---
title: Jeopardy Management
description: Jeopardy Management is a risk assessment tool that monitors fulfillment tasks, assesses the risk level, and alerts fulfillment managers when the assigned task time is in jeopardy.
locale: en-US
release: yokohama
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Order Management, Exploring Sales Customer Relationship Management, Sales Customer Relationship Management]
---

# Jeopardy Management

Jeopardy Management is a risk assessment tool that monitors fulfillment tasks, assesses the risk level, and alerts fulfillment managers when the assigned task time is in jeopardy.

Jeopardy Management consists of multiple components in the Order Management application that work together to monitor and report on task completion time in a fulfillment plan.

If a task is taking longer than expected, the system assesses the percentage of delay and assigns a risk level.

In Order Management, some customer orders are expected to be fulfilled within a committed time frame. The time commitment may be part of a contract that the customer and customer service provider \(CSP\) have signed to ensure delivery and assurance of products and services. To fulfill an order within the target date and time, a CSP depends on order management systems to monitor the fulfillment progress. Jeopardy Management proactively identities any delays and shares alerts, which can be addressed by fulfillment managers.

![Infographic that shows how Jeopardy Management works to track tasks in the fulfillment process and alert managers if tasks are taking too much time.](../image/jm-workflow-concept.png "Overview of Jeopardy Management")

## How Jeopardy Management works

Jeopardy Management works by tracking tasks in an order fulfillment process. Order task relationships are created and task durations are set. Planned tasks are set in the Draft state and have a start time and an end time. As an order task is being fulfilled, any delays within the task's assigned amount of time triggers a jeopardy alert.

![Infographic that shows five boxes that list how Jeopardy Management components work together to assess risk.](../image/jm-how-jm-works.png "Jeopardy Management components")

## Jeopardy Management alert levels

In Jeopardy Management, the fulfillment manager can set different levels of alerts for each task. As the system monitors task duration, any delay triggers adjustments to the jeopardy level of predecessor and successor tasks in the fulfillment plan.

The following image shows several Jeopardy Management configuration examples.



![Infographic that shows several scenarios that convey how Jeopardy Management assesses and manages risk to workflow completion.](../image/jm-use-case-image.png)

The Jeopardy Management scenarios image compares some scenarios for tasks at certain risk levels: expected, on-time, and delayed. Jeopardy Management assesses all the tasks in a workflow and adjusts the risk level for tasks that occur later in the workflow.

## What to do next

Use the following links to learn more about how to configure and use Jeopardy Management.

-   
-   [Monitoring Jeopardy Management](../task/monitoring-jeopardy-management.md)

