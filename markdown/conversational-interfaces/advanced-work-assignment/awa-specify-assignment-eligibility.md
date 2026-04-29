---
title: Define agent pools eligible for assignment
description: Specify pools of agents eligible to receive overflow work assignments for a queue. An eligible assignment pool can consist of one or more groups of agents available to work on items in the queue. This feature enables Advanced Work Assignment to find a qualified agent from a wider pool of agents.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Define agent pools eligible for assignment

Specify pools of agents eligible to receive overflow work assignments for a queue. An eligible assignment pool can consist of one or more groups of agents available to work on items in the queue. This feature enables Advanced Work Assignment to find a qualified agent from a wider pool of agents.

## Before you begin

Role required: admin

## About this task

Use the **Assignment Eligibility** related link to expand the pool of agents eligible to work on items in the queue when other agents are busy or unavailable. For each agent pool, select the assignment rule that determines the assignment eligibility. If you don’t define an eligible assignment pool for a queue, work items are routed to the queue but AWA doesn't assign them.

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select the queue.

3.  To create an assignment pool, go to the **Assignment Eligibility** related link.

    -   To create a new eligible assignment pool, select **New**.
    -   To change the assignment eligibility for a pool of agents, select the pool to be updated.
4.  On the form, fill in the fields.

<table id="table_nln_krq_lfb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Agent assignment rule

</td><td>

The name of the rule that determines how work items are to be assigned. Select an assignment rule from the list.

</td></tr><tr><td>

Eligible at

</td><td>

The length of time in seconds before AWA considers the next set of agents for assignment.

</td></tr><tr><td>

Groups

</td><td>

The set of groups eligible for assignment. -   Click the lock icon to unlock it and select the agent groups in the eligible assignment pool.
-   Click the lock icon to lock it.


</td></tr></tbody>
</table>5.  Select **Submit** to create the eligible or **Update** if modifying an eligible assignment pool.

    The Queues \[awa\_queues\] table is updated with the eligible assignment pool.


