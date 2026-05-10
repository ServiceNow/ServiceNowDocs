---
title: Create assignment rules and groups
description: Define agent assignment rules and specify groups of agents who are eligible to receive overflow work assignments for a queue.
locale: en-US
release: australia
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Channels, Channels, Workforce Optimization for ITSM, IT Service Management]
---

# Create assignment rules and groups

Define agent assignment rules and specify groups of agents who are eligible to receive overflow work assignments for a queue.

## Before you begin

You must first create a new assignment rule before you create a service channel. For more information, see [create a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md). Use [Exploring Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-overview.md) \(AWA\) to route work items automatically to agents based on an agent's availability, capacity, and skills.

Role required: sn\_channel\_mgmt.admin

## About this task

An eligible assignment group can consist of one or more groups of agents available to work on items in the queue.

## Procedure

1.  Navigate to **All** &gt; **Workforce Optimization for ITSM** &gt; **Channel Management** &gt; **Queues**

2.  Select a queue to define an assignment rule.

3.  In the **Assignment Eligibility** tab, click **New**.

4.  On the form, fill in the fields.

<table id="table_nln_krq_lfb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Agent assignment rule

</td><td>

Name of the rule to assign work items to agents.

</td></tr><tr><td>

Eligible at

</td><td>

The duration that this assignment rule is valid for a set of agents.

</td></tr><tr><td>

Groups

</td><td>

The set of groups eligible for assignment. -   Click the lock icon to unlock it and select the agent groups in the eligible assignment pool.
-   Click the lock icon to lock it.


</td></tr></tbody>
</table>5.  Click **Submit** to create the eligible or **Update** if modifying an eligible assignment pool.

    The Queues \[awa\_queues\] table is updated with the eligible assignment group.

    **Note:** For a new service channel, you must first create a new assignment rule and then [create a service channel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/advanced-work-assignment/awa-create-service-channel.md).


**Parent Topic:**[Setting up Channels in Workforce Optimization for ITSM](../concept/setup-channels-configurable-workforce-optimization-itsm.md)

