---
title: Categorize workstation activities to simplify analysis
description: Organize and add context to your data by grouping similar workstation activities with user-friendly category names.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/task-mining/define-default-categorization-rules.html
release: australia
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 4
breadcrumb: [Use, Task Mining, Platform Analytics]
---

# Categorize workstation activities to simplify analysis

Organize and add context to your data by grouping similar workstation activities with user-friendly category names.

## Before you begin

Begin categorizing activities after you collect sample workstation activity data. This sample activity data makes categorization easier because you have the exact application and window values used in your organization available.

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

Five predefined categorization rules are provided and can't be changed. The first four rules classify inactive time. The MAX rule applies last and represents uncategorized activity that doesn't match any rule, and is the source for categorizing activities. By default, uncategorized activities don't appear in dashboards and fall into the Other category.

You create categorization rules with a condition builder. Each rule matches activities when the conditions you define evaluate true against an activity's application name, window name, or URL. For more information, see [Categorization concepts in Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/configuration-concepts.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Application categorization icon \[Omitted image "task-mining-categorization-icon.png"\].

3.  Add categories to the list available on the categorization rule form to describe the type of work that applications are related to.

    For example, if your organization uses many social media applications, you might want to create a category named Social media.

    1.  Select **Categories**.

    2.  Select **Create category**.

    3.  Enter a category name in the **Name** field.

    4.  Select **Save**.

    \[Omitted image "tm-cat-3.png"\] Alt text: Screenshot showing the Categories and Applications options.

4.  Verify whether all of the applications your organization wants to analyze are listed on the categorization rule form and add any that are missing.

    This list determines the application names available for creating categorization rules. You can provide user-friendly application names, such as "Teams" for "Microsoft Teams."

    1.  Select **Applications**.

    2.  Select **Add application**.

    3.  Enter an application name in the **Name** field.

        For example, you could add the user-friendly name "Teams" for activities in both the native Microsoft Teams application and accessing the application in a browser.

    4.  Select **Save**.

5.  Identify which applications to categorize in the **MAX** list.

    1.  Select **All other activities** in the Condition column of the **MAX** category to open the **MAX** list of uncategorized activities.

    2.  Select the calendar icon to set the date range for the activities to review.

        **Note:** If the MAX list is empty, check the date range. The range defaults to the last 3 days, so activity collected earlier doesn't appear until you extend it to cover your collection period. You can select a range up to 90 days.

        \[Omitted image "tm-cat-4.png"\] Alt text: Screenshot showing the Open calendar icon.

    3.  Narrow the list to find the activities to categorize.

        -   Select column headers to order the list. Filter the list by **Application Name**, **Window Name**, or **URL**.
        -   Select the search icon to find a text string across the **Application Name**, **Window Name**, and **URL** columns at the same time.
        -   Select **Sort by** or **Group by** to sort and group the candidate list by different values.
    4.  Select the Create rule icon \[Omitted image "create-rule-icon.png"\] next to the application's name.

        You could also choose to create an application-based rule, for example, by finding an activity with a Microsoft Teams file name.

    The **Create rule** panel opens with condition values populated based on the activity record you selected.

6.  In the **Conditions** section of the **Create rule** panel, define the conditions that match the activities to categorize.

    1.  Verify or modify the **Application Name**, **Window Name**, and **URL** conditions.

    2.  Select **and** to match one or more conditions, **or** to match any of several values, or **Add condition set** to add a separate group of conditions.

    \[Omitted image "tm-cat-1.png"\] Alt text: Screenshot showing the Conditions section of the rule builder.

7.  Change the **Rank** value.

8.  In the **Categories** section, set the rule properties.

    1.  Leave **Activity** as Productive for most work.

    2.  Select a **Category** to describe the type of work that the activity is related to.

        **Note:** Don't use the **Other** category. The **Other** category is reserved for the MAX rule and represents uncategorized activities that don't match any rule.

    3.  Select a user-friendly **Application** name.

    4.  Enter a **Window name** to mask or further describe the activity.

    For a description of the field values, see [Categorization rule form in Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/categorization-rules.md).

    \[Omitted image "tm-cat-2.png"\] Alt text: Screenshot showing the Categories section of the rule builder.

9.  Select **Save rule**.

    Activities in the **MAX** list that match the rule are recategorized and removed from the list. Categorization runs automatically when you save the rule.

10. Continue creating rules until uncategorized activities in the **MAX** list represent no more than about 10% of the total duration.


**Related topics**  


[Refine the presentation of your data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/preview-data-based-on-categorization-rules.md)

[Categorization concepts in Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/configuration-concepts.md)

[Categorization rule form in Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining/categorization-rules.md)

