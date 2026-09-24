---
title: Create filter manually
description: Create filters manually after selecting the Start from scratch option from Process steps in Analyst workbench.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/process-mining/filter-manual.html
release: brazil
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Create filter, Applying a process step filter on an activity, Filtering project data, Analyzing and getting process insights, Use, Process Mining, Platform Analytics]
---

# Create filter manually

Create filters manually after selecting the Start from scratch option from Process steps in Analyst workbench.

## Before you begin

Role required: sn\_process\_mining\_analyst, sn\_process\_mining\_power\_user, or sn\_process\_mining\_admin

## Procedure

1.  Follow steps 1 through 3 on [Create a process step filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/create-transition-manually.md) section.

2.  Select **Start from scratch** option from the **Process steps** list.

    \[Omitted image "quick-start.png"\] Alt text: Start from scratch

    The Process steps filter page is displayed.

    \[Omitted image "transition-filter.png"\] Alt text: Process step filter conditions

    The predicates available are:

    -   is
    -   is not
    -   is empty
    -   is not empty
    -   is anything
    -   is one of: When you select "is one of", you can select multiple values at once. Type the first two letters, and select the **Select all** icon to select all matching values.
    -   is not one of: When you select "is not one of", you can select multiple values at once. Type the first two letters, and select the **Select all** icon to select all matching values.
    **Note:** OR condition can be used only for conditions within the same entity. \(State \(incident\) is Work in progress OR Assignment group \(incident\) is database\).

3.  Provide the details on the form.

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

        If you select **Current**, it will consider the view of the project. If you select **Matching the filter**, it will consider only the filter set. The view of the project will not be considered.

    7.  You can copy or paste a process step filter by selecting the **Copy** or **Paste** option from the list.

        \[Omitted image "copy-process-filter.png"\] Alt text: Copy or paste a filter

4.  When you have finished creating your filter, select **Apply** to save and return to **Analyst workbench**.

    The task runs in the background.

5.  When the task completes, select **View result** in the Scheduled tasks panel of Analyst workbench.


**Parent Topic:**[Create a process step filter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/process-mining/create-transition-manually.md)

