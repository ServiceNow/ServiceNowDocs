---
title: Create a child log policy
description: Refine an existing log policy to focus on a subset of CIs or services by creating a child policy.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector log policies, Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# Create a child log policy

Refine an existing log policy to focus on a subset of CIs or services by creating a child policy.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

A published log policy \(the parent policy\) can be used as a template for creating a new log policy \(the child policy\). You can customize the parameters that the child policy inherits from the parent to focus on a subgroup of its CIs or services.

The child policy inherits parameters from its parent policy that are modified after the child policy's creation, unless you disable this option in the child policy. You can choose to review these modified parameters in draft mode in each child policy before accepting them.

**Note:** The child policy is inherently more specific than its parent policy. When Agent Client Collector matches a condition defined in the child policy, it will not try to match the parent policy.

## Procedure

1.  Navigate to **All** &gt; **ACC Log Analytics** &gt; **ACC Log Policies**.

2.  On the **Policies** page, select a published policy with a Hierarchy value of either **None** or **Parent**.

3.  Select **Create Child**.

    A new policy opens with the same parameters as the published policy. The name of the new policy is **&lt;Policy name&gt;&lt;date and time created&gt;**.

    For example, MySQL DB on Linux Logs 2022-02-13 04:44:12.

    The following fields are read-only:

    |Field|Value|
    |-----|-----|
    |Publish status|Draft|
    |Hierarchy|Child|
    |Parent|&lt;Name of the parent policy&gt;|

    The **Order** field value indicates the priority by which the agent attaches itself to the child policy in relation to its sibling policies. A lower number indicates a relatively higher priority for this child policy. By default, each new child policy takes on a higher value \(and hence, a lower priority\) than the one preceding it. You can modify the order value as needed.

4.  Customize the child policy's parameters.

    For a description of the parameters, see [Create an Agent Client Collector log policy](../../health-log-analytics-admin/task/hla-acc-log-policies.md).

5.  Select **Save** to create the child policy.

6.  Select **Disable inherit option** to disable automatically inheriting modified parameters from the parent policy.

7.  Select **Publish** to publish the child policy.


## Result

The child policy is published and appears on the **Child Policies** tab of the parent policy.

