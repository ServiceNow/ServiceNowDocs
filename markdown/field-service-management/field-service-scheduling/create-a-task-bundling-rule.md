---
title: Create a task bundling rule
description: Create a task bundling rule to bundle tasks dynamically according to the selected parameters with Field Service Task Bundling.
locale: en-US
release: zurich
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Dynamic task bundling, Configuring Task Bundling, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Create a task bundling rule

Create a task bundling rule to bundle tasks dynamically according to the selected parameters with Field Service Task Bundling.

## Before you begin

To add rules to any policy other than the default policy, create a policy first. For more information, see [Create a task bundling policy](create-a-task-bundling-policy.md).

[Enable the Field Service territory model](enable-territory-model.md) plugin when bundling tasks by territory.

Role required: admin

## About this task

Task Grouping Rules can be applied on tasks only if the following conditions are met:

-   Is in Draft State
-   Not part of another bundle
-   Not a bundle itself
-   Not a vendor task
-   Shouldn’t have access hours
-   Doesn’t need a crew
-   Doesn’t have a fixed window
-   Doesn’t have dependent tasks

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dynamic Bundling Administration** &gt; **Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_ljv_35d_5xb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the rule.

</td></tr><tr><td>

Policy

</td><td>

Policy that this rule is grouped under.**Note:** To add rules to any policy other than the default policy, create a policy first. For more information, see [Create a task bundling policy](create-a-task-bundling-policy.md).

</td></tr><tr><td>

Order

</td><td>

Order of when this rule is applied relative to other rules within the policy.

</td></tr><tr><td>

Active

</td><td>

Option to make the rule active or inactive.

</td></tr></tbody>
</table>4.  In the Grouping Conditions section, use the condition builder to create task filters that define the tasks that this rule targets.

5.  Toggle **Advanced** to replace the condition builder with a **Script** field.

    Toggling **Advanced** replaces the condition builder with the following template:

    ```
    /**
     * This scripted rule should return an array of sys_ids of tasks joined using comma for each group that should be bundled
     * @param {String} taskType table name that contains the taskIds
     * @param {String} taskIds comma-separated task sys_ids representing a group of tasks
     * @returns {String[]} list of comma-separated task sys_ids shown as below:
     * [
     *	'sys_id_1,sys_id_2,sys_id_3',
     *	'sys_id_4',
     *	'sys_id_5,sys_id_6,sys_id_7,sys_id_8'
     * ]
     */
    (function executeRule(taskType, taskIds) {
    	// your code goes here
    })(taskType, taskIds);
    ```

6.  Select **Preview Tasks** to preview all tasks that are affected by your rule.

7.  Select **Submit**.


