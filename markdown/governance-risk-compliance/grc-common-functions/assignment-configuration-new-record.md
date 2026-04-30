---
title: Assignment Configuration New Record
description: Use the Assignment Configuration new record form to create auto-assignments for regulatory events of the type regulatory alert.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: reference
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Set up an approval configuration record, Use Approver Configurator for setting up approvals for setting up approvals, Common GRC features, Governance, Risk, and Compliance]
---

# Assignment Configuration New Record

Use the Assignment Configuration new record form to create auto-assignments for regulatory events of the type regulatory alert.

## Assignment Configuration New Record

<table id="table_ln3_y5g_3rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the assignment configuration. For example, Assignment configuration 1.

</td></tr><tr><td>

Applies to

</td><td>

Name of the table on which the assignment configuration is being applied.

</td></tr><tr><td>

Order

</td><td>

Value that is used by the assignment configuration engine to pick the assignment configuration for execution. For example, if there are multiple assignment configurations on the same table with different conditions, the one with the lowest value is picked for execution.

</td></tr><tr><td>

Active

</td><td>

Option to mark the assignment configuration record as active.

</td></tr><tr><td class="sub-head" colspan="2">

Conditions

</td></tr><tr><td>

Choose a field

</td><td>

Field on which you want to apply the condition.

</td></tr><tr><td>

Operator

</td><td>

Required operator.

</td></tr><tr><td>

Value

</td><td>

Value of the field on which you’re applying the condition.

</td></tr><tr><td class="sub-head" colspan="2">

Actions

</td></tr><tr><td>

Assign to

</td><td>

-   Individuals influenced by user full name.
-   Individuals referenced in associated context.
-   Individuals based on programmatic logic.

</td></tr><tr><td>

User Influenced by

</td><td>

User category to which you want to assign the configuration.

 -   None.
-   Assigned to.
-   Closed by.
-   Issue manager.
-   Opened by.

</td></tr><tr><td>

Group Influenced by

</td><td>

User group category to which you want to assign the configuration.

 -   Assignment group.
-   Issue manager group.

</td></tr><tr><td>

Assignee \(user\)

</td><td>

User to whom you want to assign the configuration.

</td></tr><tr><td>

Assignee \(group\)

</td><td>

User group to which you want to assign the configuration.

</td></tr></tbody>
</table>**Parent Topic:**[Set up an approval configuration record](../task/set-up-approval-configurator.md)

