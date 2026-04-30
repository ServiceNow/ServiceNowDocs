---
title: Create a recommendation with the decision tree as an action type
description: Create a recommendation to select Troubleshoot credit card transaction failure decision tree as an action type.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Example: Troubleshoot a failed credit card transaction, Example configurations of recommended actions, Recommended Actions configuration, Implement Intelligence, Configuring Customer Service Management, Customer Service Management]
---

# Create a recommendation with the decision tree as an action type

Create a recommendation to select Troubleshoot credit card transaction failure decision tree as an action type.

## Before you begin

Role required: sn\_nb\_action.next\_best\_action\_author, admin

## About this task

New recommendations can only be created inside the rules.

## Procedure

1.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.

2.  Select the Case context.

3.  Select Active rule from the Rules related list.

4.  In the Recommendations related list, select **New**.

5.  In the New Recommendation screen, select **A guided flow to follow** to create a recommendation of type decision tree.

    A new Recommendation form is displayed with the **Rule**, **Context**, and **Action type** fields auto populated.

6.  In the **Name** field, enter `Troubleshoot credit card transaction failure`.

7.  In the **Action** field, select the action.

    The available actions are determined by the selection in the **Action type** field.

    1.  In the **Action** field, select the lookup icon.

        In the resulting pop-up window, the **Table name** field is auto populated with the table that stores the available actions for the selected action type.

    2.  In the **Document** field, select the Troubleshoot credit card transaction failure decision tree by clicking the lookup icon.

        For more information about how to create this decision tree, see [Create Troubleshoot credit card transaction failure decision tree](../concept/preparation-for-creating-a-decision-tree.md).

    3.  Select **OK**.

8.  In the **Recommendation hint** field, enter `Troubleshoot credit card transaction failure`.

    The hint explains to agents why a recommendation is being suggested.

9.  Select **Update**.


