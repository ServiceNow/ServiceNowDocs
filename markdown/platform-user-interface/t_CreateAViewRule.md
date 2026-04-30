---
title: Create a view rule
description: When a user switches views, the selected view is saved as a user preference so the user sees the same view by default when the form opens. With a view rule, you can override this functionality to force a specified view to be used.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [View management, User interface configuration, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create a view rule

When a user switches views, the selected view is saved as a user preference so the user sees the same view by default when the form opens. With a view rule, you can override this functionality to force a specified view to be used.

## Before you begin

Role required: admin

## About this task

View rules do not always apply if there are existing user preference entries on the instance. Delete the user preference entry and clear the system cache to make sure the respective view rule applies. You can clear the system cache by appending `cache.do` to the instance URL. For example, `instance_name.service-now.com/cache.do`.

**Important:** Clearing the system cache can affect overall performance, and degrade system response times. Do not run cache flushes during business hours, and do not trigger cache flushes automatically.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **View Rules**.

2.  Click **New**.

3.  Complete the form, using the fields in the table.

    |Field|Input value|
    |-----|-----------|
    |Name|Specify an identifying name for the rule.|
    |Active|Select this option to apply the view rule according to the conditions you specified. If unchecked, the view rule is not be applied.|
    |Advanced|Select this option to specify a code-based condition instead of using the condition builder. Selecting this option displays the **Script** field and hides the **Match conditions**, **Conditions**, and **View** fields.|
    |Match Conditions|Select whether **Any** or **All** of the conditions need to be met. The system hides this field when you create an advanced View Rule.|
    |Conditions|Use the condition builder to determine when the view is applied. The system hides this field when you create an advanced View Rule.|
    |Application|Displays the application to which the View Rule record belongs.|
    |Table|Select the table on which this view rule will be applied. The list shows only tables and database views that are in the same scope as the view rule|
    |Device type|Select which interface this view rule applies to.|
    |View|Enter the name of the View you are creating a rule for. The system hides this field when you create an advanced View Rule. This field is case-sensitive and must match exactly the view name.|
    |Script|Enter a script to determine when to display a particular view. The system only displays this field when you create an advanced View Rule.|

4.  Click **Submit**.


**Parent Topic:**[View management](../concept/view-management-overview.md)

