---
title: Create an assignment workbench configuration
description: Use a matching rule to create a configuration for the assignment workbench.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure assignment workbench, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create an assignment workbench configuration

Use a matching rule to create a configuration for the assignment workbench.

## Before you begin

Role required: admin

## About this task

The assignment workbench configuration is stored in a matching rule that is based on the **Selection criteria** matching type. The default configuration uses the **Recommendation for Case Assignment** matching rule, which includes three of the four default matching criteria:

-   Availability today
-   Matching skills
-   Assigned cases

You can modify or create matching criteria and then modify the **Recommendation for Case Assignment** matching rule as needed or you can create your own configuration.

## Procedure

1.  Navigate to **All** &gt; **Routing and Assignment** &gt; **Matching Rules** to access the Matching Rules list.

2.  Select **New**.

3.  Enter a **Name** for the matching rule.

4.  If desired, enter an **Execution Order** for the matching rule.

    This execution order is the order in which the matching rule is to be executed. Similar to business rules, matching rules are processed based on execution order, from the lowest to the highest.

5.  In the **Applies To** tab, select the **Table** that stores the task for which the matching rule is being created.

6.  Use the **Conditions** field to build one or more conditions on the selected table.

    A condition is made up of a selected field, an operator, and a value. Add conditions using the **AND** and **OR** buttons. Delete conditions by selecting the **X** icon on the right-side of a condition.

7.  In the **Resource** tab, select **Selection Criteria** in the **Matching** field.

8.  Select **Submit**.

9.  From the Matching Rules list, open the matching rule that you created .

10. In the **Select Criteria** related list, select **New**.

    The select Criterion form is displayed.

11. Select a **Criterion** from the Matching Criteria list.

12. Select how the criterion is to be used in the **Use for** field.

<table id="choicetable_njl_kph_xx"><tbody><tr><td id="d213948e231">

**Ranking and Display**

</td><td>

Uses the criterion to determine agent ranking and displays it in a column on the workbench.

</td></tr><tr><td id="d213948e240">

**Display Only**

</td><td>

Displays the criterion in a column on the workbench but does not use it to determine agent ranking.

</td></tr><tr><td id="d213948e249">

**Ranking and No Display**

</td><td>

Uses the criterion to determine agent ranking but does not display it on the workbench.

</td></tr></tbody>
</table>13. Select a **Ranking Method**.

<table id="choicetable_mth_1qh_xx"><tbody><tr><td id="d213948e270">

**More is better**

</td><td>

A higher value is better. For example, more availability is better when determining the agent ranking.

</td></tr><tr><td id="d213948e279">

**Less is better**

</td><td>

A lower value is better. For example, fewer cases are better when determining the agent ranking.

</td></tr></tbody>
</table>14. Select **Submit**.

15. Repeat steps 10 through 14 for each criterion to add to the matching rule.

16. If desired, change the weight of a criterion by double-clicking the **Weight** field in the **Select Criteria** related list and entering a new weight.

    Each matching criterion has an assigned weight. By default, the matching criteria in the Recommendation for Case Assignment matching rule have an assigned weight of 10. You can assign a higher weight to the criteria that are more important.

17. If desired, set the threshold for a criterion by double-clicking the **Threshold** field in the **Select Criteria** related list and entering a threshold number.

    A threshold sets a minimum requirement for a criterion. It may be necessary to personalize the list and add the **Threshold** column.

18. If desired, set a criterion active or inactive by double-clicking the **Active** field in the **Select Criteria** related list and selecting **true** or **false**.

    Changing this setting has an immediate impact on the agent ranking. It may be necessary to personalize the list and add the **Active** column.


