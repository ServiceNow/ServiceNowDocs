---
title: Create a task bundling policy
description: Create a task bundling policy to apply various rules for dynamically bundling tasks with Field Service Task Bundling.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dynamic task bundling, Configuring Task Bundling, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a task bundling policy

Create a task bundling policy to apply various rules for dynamically bundling tasks with Field Service Task Bundling.

## Before you begin

Role required: admin

## About this task

Task bundling policies are groups of rules that dictate how work order tasks are bundled using dynamic bundling. Policies can be configured to target a minimum and maximum range of records, as well as a maximum duration per bundle. Bundles generated through dynamic bundling can’t exceed 200 work order tasks. Policies must have one or more qualifiers in order to run.

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dynamic Bundling Administration** &gt; **Policies**.

2.  Select **New**.

3.  On the Task Grouping Policy form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Name|Name of the policy.|
    |Task type|Task type table to apply to the rules in this policy.|
    |Order|Order of when this policy is applied to a task relative to other policies.|
    |Active|Option to make the policy active or inactive.|
    |Sort by|Dictates how subtasks are sorted before bundling.|
    |Minimum records|The minimum number of records enabled per bundle.|
    |Maximum records|The maximum number of records enabled per bundle.|
    |Duration field|The duration type that this policy should target.|
    |Maximum duration|The maximum duration per task bundle created by this policy.|

4.  Select **Submit**.


## What to do next

Policies require rules and qualifiers to run. For more information, see [Create a task bundling rule](create-a-task-bundling-rule.md) and [Add qualifiers to a task bundling policy](add-qualifier-bundling-policy.md).

After a policy is complete, you can schedule them or run them manually. For more information, see [Schedule dynamic task bundling](schedule-dynamic-task-bundling.md) or [Run a task bundling policy manually](run-a-task-bundling-policy.md).

