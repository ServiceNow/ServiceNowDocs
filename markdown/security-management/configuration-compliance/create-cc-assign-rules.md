---
title: Create or edit Configuration Compliance assignment rules
description: Create rules to automatically assign test results based on filter conditions. These rules assign test results as they are imported.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up, installing, and configuring the Configuration Compliance application, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Create or edit Configuration Compliance assignment rules

Create rules to automatically assign test results based on filter conditions. These rules assign test results as they are imported.

## Before you begin

Role required: sn\_vulc.admin

## About this task

The base system ships with one Configuration Compliance assignment rule, **Assign to CI support group**, which assigns test results to the same assignment group as the CI support group. This rule is inactive by default. You can modify using filter conditions. With assignment rules, you define one or more conditions of assignment and the order of execution. Once a test result matches a rule condition, the assignment lookup stops.

**Note:** New or updated rules are automatically evaluated on the next import or manually using the **Apply Changes** button on the Assignment Rules list.

## Procedure

1.  Navigate to **All** &gt; **Configuration Compliance** &gt; **Administration** &gt; **Assignment Rules**.

2.  Open the **Assign to CI support group** rule or click **New**.

3.  Edit the **Assign to CI support group** rule, or if **New**, fill in the fields on the form, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the group rule.

</td></tr><tr><td>

Execution order

</td><td>

Order in which the rules are evaluated. The lowest number is evaluated first.

 High priority rules, test results that need special handling, where risk is critical, or a test result that should be handled by regulatory compliance, should be run first. Next, run your general rules, where no special handling is required, and you know who should be responsible for them. Finally, create a default rule to assign test results to the group that figures out what assignment group it should belong to. This group could add another rule to cover their decisions. This default rule would run last.

</td></tr><tr><td>

Active

</td><td>

Indicates whether the assignment rule is active.

</td></tr><tr><td colspan="2">

**Condition**

</td></tr><tr><td>

Condition fields

</td><td>

Conditions that must be met.Case sensitivity for the search text you enter in the condition builder is not supported on this record or form.

</td></tr><tr><td>

New Criteria

</td><td>

Adds more condition filter fields to choose from.

</td></tr><tr><td>

Description

</td><td>

Text describing the assignment rule.

</td></tr><tr><td>

Assign using

</td><td>

To automate the assignment of groups created based on this rule, choose one of the options available.

-   User group: Select a user group from the lookup table
-   User group field: Select a user group field from the drop-down menu.
-   Script: Create or edit a script.

**Note:** Creating or edit a script requires ServiceNow expertise.

</td></tr><tr><td>

User group field

</td><td>

Select the user group responsible for remediating tests that match the conditions of the assignment rules.

</td></tr></tbody>
</table>4.  Click **Submit**.


**Parent Topic:**[Setting up, installing, and configuring the Configuration Compliance application](../concept/cc-configuring.md)

