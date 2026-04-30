---
title: Set work item sort order
description: Specify the order in which work items in a queue are sorted.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Set work item sort order

Specify the order in which work items in a queue are sorted.

## Before you begin

Role required: awa\_admin or admin

## About this task

The **Work Item Sort Order** field only determines the order that AWA assigns the work item and doesn’t affect the order of work items in the agent's inbox card. Work items in the inbox card are displayed based on the time that they arrive. The **Work Item Sort Order** field assigns a set of pending work items to agents designed by the defined work item sort order. For example, if two work items are pending when an agent becomes available, the **Work Item Sort Order** decides which work item is assigned first to an agent via AWA.

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select the queue.

3.  Select the **Work Item Sort Order** related list and select **New**.

4.  In the Work Item Sort Order form, select:

    -   **Field**: The field to be used for the sort. The fields are from the table for the associated channel. For example, the fields available for the chat service channel are from the Interaction table.
    -   **Sort Direction**: The order in which work items are sorted. Select either Ascending \(smallest to largest or oldest to newest\) or Descending \(largest to smallest or newest to oldest\).
    -   **Order**: The value of the **Order** value relative to other items in the queue.
5.  Select **Submit**.


**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

