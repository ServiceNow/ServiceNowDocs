---
title: Set rule-based improvement opportunity
description: Rule-based finding definition is a custom rule that displays improvement opportunities for a use case on the Summary and insights page.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Setting improvement opportunities, Use, Process Mining, Platform Analytics]
---

# Set rule-based improvement opportunity

Rule-based finding definition is a custom rule that displays improvement opportunities for a use case on the Summary and insights page.

## Before you begin

Role required:

-   The sn\_process\_mining\_admin and sn\_process\_mining\_power\_user roles can create an improvement opportunity for a project.
-   The sn\_process\_mining\_analyst role can view an improvement opportunity for a project, but can’t create, edit, or delete an improvement opportunity.

By setting up your own rules, you can focus on specific areas of the process that you'd want to know more about, thus identifying improvement opportunities for a given use case.

For example, you can set up a rule to display records that took more than 7 days from **Awaiting verification** to **Resolved**.

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about Improvement opportunity definition page, see [Set improvement opportunities](improve-opportunities.md).

2.  Select **Create** on the Rule-based card.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form](../reference/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

    ![Configure rule-based finding in Finding Builder](../image/rule-find-config-builder.png)

    The predicates available are:

    -   is
    -   is not
    -   is empty
    -   is not empty
    -   is anything
    -   is one of: When you select "is one of", you can select multiple values at once. Type the first two letters, and select the **Select all** icon to select all matching values.
    -   is not one of: When you select "is not one of", you can select multiple values at once. Type the first two letters, and select the **Select all** icon to select all matching values.
5.  Fill the details on the form.

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
    5.  Select the **Track duration** field.

        This field tracks the time between the specified finding steps to calculate the total duration of the finding process, which is displayed on the improvement opportunity.

    6.  Select **Criteria between steps** to create further filters, and then select**Apply** to set the criteria between steps filter.

        The options available are:

        -   Time between steps
        -   While attribute remained
        -   Touchpoints between steps
    7.  Select an option for **Apply to map view**.

        If you select **With all activities**, it will consider the view of the project. If you select **Matching the rules**, it will consider only the filter that is set. The view of the project will not be considered.

    8.  You can copy or paste a single filter by selecting the **Copy** or **Paste** option from the list.

        ![Copy or paste a filter](../image/copy-process-filter.png)

6.  Select **Create a copy** from the **Actions** list to copy the entire improvement opportunity.

    ![Create a copy of the improvement opportunity](../image/imp-opp-copy.png)

7.  Select **Save and exit**.


**Parent Topic:**[Setting improvement opportunities](../concept/working-with-imp-opp.md)

