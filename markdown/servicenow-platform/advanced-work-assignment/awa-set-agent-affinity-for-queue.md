---
title: Set Agent Affinity rules
description: Specify the Agent Affinity rules to determine the order in which work items in a queue are sorted.
locale: en-US
release: yokohama
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Agent Affinity, Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set Agent Affinity rules

Specify the Agent Affinity rules to determine the order in which work items in a queue are sorted.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the queue settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up queues**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Queues**.
2.  Select the queue.

3.  Select the Agent Affinity related list.

    -   To create a Agent Affinity rule mapping, select **New**.
    -   To change an existing Agent Affinity rule mapping, select the mapping to be updated.
4.  On the form, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Agent Affinity Rule|Agent Affinity rule to be used for the sort.|
    |Order|Value of this rule relative to the other rules in the queue. Rules are ordered from lowest to highest so a rule with an order of 100 is considered before a rule with an order of 200.|

5.  Select **Submit**.

    You can specify a maximum of three Agent Affinity rules per queue.


**Parent Topic:**[Using Agent Affinity](../concept/awa-agent-affinity-concept.md)

