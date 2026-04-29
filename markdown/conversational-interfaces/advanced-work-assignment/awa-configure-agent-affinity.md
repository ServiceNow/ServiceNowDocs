---
title: Configure Agent Affinity rules
description: Create or change the Agent Affinity rules that route work items in Advanced Work Assignment.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Configure Agent Affinity rules

Create or change the Agent Affinity rules that route work items in Advanced Work Assignment.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the agent affinity settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Advanced settings section, select **Set up Agent Affinity**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Agent Affinity Rules**.
2.  Choose a situation.

    -   To create an affinity rule, select **New**.
    -   To update an existing affinity rule, select the affinity rule.
3.  On the form, fill in the fields.

<table id="table_m12_pyk_t2b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the affinity rule.

</td></tr><tr><td>

Service channel

</td><td>

Service channel that the rule applies to.

</td></tr><tr><td>

Application

</td><td>

Name of the application.

</td></tr><tr><td>

Affinity based on

</td><td>

Type of affinity. Only affinity types corresponding to your selection appear. -   History
-   Related Tasks
-   Account Team Responsibility


</td></tr><tr><td>

Agent's affinity to

</td><td>

Account level or contact level. This field appears when you select **History** in the **Affinity based on** field.

</td></tr><tr><td>

Number of days

</td><td>

Past number of days during which the agent has worked with the customer. The maximum number of days is 30. This field appears when you select **History** in the **Affinity based on** field.

</td></tr><tr><td>

Responsibility

</td><td>

Agent who is part of the account team. This field appears when you select **Account Team Responsibility** in the **Affinity based on** field.

</td></tr></tbody>
</table>4.  Click **Submit** for a new affinity rule or **Update** to modify an existing affinity rule.


