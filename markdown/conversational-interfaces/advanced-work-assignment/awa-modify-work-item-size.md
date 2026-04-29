---
title: Create or change a work item size override
description: Create a work item size override if you want Agent Affinity to calculate an agent's workload using a work item size other than the default.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create or change a work item size override

Create a work item size override if you want Agent Affinity to calculate an agent's workload using a work item size other than the default.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Select the service channel.

3.  On the form, select the **Work Item Size Override** list.

    -   To create an override, select **New**.
    -   To change an existing override, select the override that you want to update.
4.  On the form, fill in the fields.

<table id="table_fdy_rhq_gfb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the override.

</td></tr><tr><td>

Service Channel

</td><td>

Service channel that is assigned to the override.

</td></tr><tr><td>

Override Size

</td><td>

Size to use instead of the default.

</td></tr><tr><td>

Order

</td><td>

Order in which Advanced Work Assignment considers this size override.

</td></tr><tr><td>

Condition mode

</td><td>

Type of condition for routing work items using this size override:

-   Simple: Specify a routine condition using the condition builder.
-   Advanced: Specify a JavaScript scripted condition.


</td></tr><tr><td>

Conditions

</td><td>

Condition that applies to the override work item sizes. This field appears when you select **Simple** in the **Condition mode** field.

</td></tr><tr><td>

Script

</td><td>

JavaScript condition statement that specifies the override work item size. The condition must evaluate to true. This field appears when you select **Advanced** in the **Condition mode** field.

</td></tr></tbody>
</table>5.  Select **Submit** to create the override or **Update** to change the override.


