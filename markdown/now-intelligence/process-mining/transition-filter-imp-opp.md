---
title: Set improvement opportunities from Analyst workbench
description: Set a process step filter as a rule-based improvement opportunity for your process table or your project.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [For projects, Setting improvement opportunities, Use, Process Mining, Platform Analytics]
---

# Set improvement opportunities from Analyst workbench

Set a process step filter as a rule-based improvement opportunity for your process table or your project.

## Before you begin

Role required:

-   The sn\_process\_mining\_admin and sn\_process\_mining\_power\_user roles can create an improvement opportunity for a project.
-   The sn\_process\_mining\_analyst role can view an improvement opportunity for a project, but can’t create, edit, or delete an improvement opportunity.

## Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  Select a project.

3.  Select **Process steps** on the Analyst workbench.

    The Process step filter window is displayed.

    ![Process step filter](../image/process-step-filter.png)

4.  Set the filters.

    To create an improvement opportunity from a transition filter, you need a minimum of two steps in your filter.

    1.  Define an activity by adding conditions that contain a field, operator, and values.

        Use the **Occurrence** field to define whether the filter applies to the first, last, or all occurrences of this condition.

    2.  Use the **Add step criteria** button to include and set threshold across the steps.

        Step criteria are conditions that apply to more than one step allowing to narrow results beyond single-step criteria. Some examples are time spent to complete a task, or any event that happened before or after the task, and so on.

    3.  Select **Add next step** to define another activity within this sequence.

        After creating a filter, a relationship section appears between the two filters. This section defines the relationship between the activities immediately above and below it.

    4.  Select a relationship between your activities.

        -   Directly followed by
        -   At some point followed by
        -   Not directly followed by
        -   Never followed by
    5.  Select **Criteria between steps** to create further filters, and then select**Apply** to set the criteria between steps filter.

        The options available are:

        -   Time between steps
        -   While attribute remained
        -   Touchpoints between steps
    6.  Select an option for **Apply map to view**.

        If you select **Current**, it will consider the view of the project. If you select **Matching the filter**, it will consider only the filter that is set. The view of the project will not be considered.

    7.  You can copy or paste a process step filter by selecting the **Copy** or **Paste** option from the list.

        ![Copy or paste a filter](../image/copy-process-filter.png)

5.  Select **Save as improvement opportunity** from the Actions list.

    ![Save as improvement opportunity from Actions list](../image/action-save-as-impopp.png)

    The Save as improvement opportunity definition dialog box is displayed.

6.  Fill the details on the Save as improvement opportunity definition dialog box.

    ![Save as improvement opportunity dialog box](../image/save-impopp.png)

    **Note:** You can add this improvement opportunity either to the project, process configuration, or both. The **Apply to** field provides the options.

    You can add it to the process configuration only if you have the sn\_process\_mining\_power\_user role.

7.  Select **Save**.

    The improvement opportunity is created and added to your process configuration, project, or both according to your preference.


**Parent Topic:**[Setting improvement opportunity for projects](../concept/project-imp-opp.md)

