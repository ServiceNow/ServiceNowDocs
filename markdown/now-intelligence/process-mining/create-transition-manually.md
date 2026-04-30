---
title: Create a transition filter manually
description: Create a transition filter to meet your needs and apply it to view the result on the process graph.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Apply a transition filter on an activity, Filtering project data, Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Create a transition filter manually

Create a transition filter to meet your needs and apply it to view the result on the process graph.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  Open a project for which you want to set the transition filter.

3.  Go to the **Analyst Workbench** tab.

4.  Select **Transitions** from the Advanced filters area.

    ![Transitions from Advanced filters area](../image/transition-location-1.png)

    The transition filter form is displayed.

5.  Fill the transition filter form with the required conditions.

    ![Transition filter conditions](../image/transition-filter.png)

    1.  Define an activity by adding conditions that contain a field, operator, and values.

        Use the **Occurrence is** field to define whether the filter applies to the first, last, or all occurrences of this condition.

    2.  Use the **Add contextual condition** button to define additional contextual conditions for this activity.

        Use the **and** and **or** buttons to create as many contextual conditions as needed.

    3.  Select **Add next activity** to define another activity within this chain.

        After creating a new activity, a **Relationship** section appears between the two activities. This section defines the relationship between the activities immediately above and below it.

    4.  Select a relationship between your activities.

        -   Directly followed by
        -   Eventually followed by
        -   Not directly followed by
        -   Not eventually followed by
    5.  Select \(![Add activity conditions using the Transitions filter](../image/show-constraint.png)\) next to **No constraints added** text to edit constraints for this relationship.

        After creating a constraint, you can select \(![Add activity conditions using the Transitions filter](../image/hide-constraint.png)\) to minimize the constraint editor.

    6.  Select **+ Add Chain** \(on the top right\) to create an additional chain of activities.

        A chain is a set of linked activities. Create a new chain to define separate set of related activities that must also evaluate to true, but does not have a relationship with the activities in another chain. Once you create a new chain you can navigate between chains using the **Chain &lt;number&gt;** tabs at the top of the window.

    7.  When you have finished creating your filter, select **Apply** to save and return to the **Analyst Workbench**.

    8.  When you have finished creating your filter, select **Apply** to save and return to the **Analyst Workbench**.

        The task runs in the background.

6.  When the task completes, select **View result** in the Scheduled tasks panel of the Analyst Workbench.


**Parent Topic:**[Apply a transition filter on an activity](../concept/node-to-node-conditions.md)

