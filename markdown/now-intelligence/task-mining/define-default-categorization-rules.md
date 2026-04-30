---
title: Categorize workstation activities to simplify analysis
description: Organize and add context to your data by grouping similar workstation activities with user-friendly category names.
locale: en-US
release: yokohama
product: Task Mining
classification: task-mining
topic_type: task
last_updated: "2024-08-26"
reading_time_minutes: 2
breadcrumb: [Use, Task Mining, Platform Analytics]
---

# Categorize workstation activities to simplify analysis

Organize and add context to your data by grouping similar workstation activities with user-friendly category names.

## Before you begin

Begin categorizing activities after you mine a sample project to collect workstation activity data. This sample activity data makes categorization easier because you have the exact application and window values used in your organization available.

Role required: sn\_tm\_core.power\_user, sn\_tm\_core.admin

## About this task

Four predefined categorization rules are provided and can't be changed. The first three rules classify inactive time. The MAX rule applies last and represents uncategorized activity that doesn’t match any rule, and is the source for categorizing activities. This uncategorized data is anonymized by default.

For more information, see [Categorization concepts in Task Mining](../concept/configuration-concepts.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Task Mining Workspace**.

2.  Select the Application categorization icon \(![Task Mining Application categorization icon](../image/task-mining-categorization-icon.png)\).

3.  Add categories to the list available on the categorization rule form to describe the type of work that applications are related to.

    For example, if your organization uses many social media applications, you might want to create a category named Social media.

    1.  Select **Categories**.

    2.  Select **Create category**.

    3.  Enter a category name in the **Name** field.

    4.  Select **Save**.

4.  Verify whether all of the applications your organization wants to analyze are listed on the categorization rule form and add any that are missing.

    This list determines the application names available for creating categorization rules. You can provide user-friendly application names, such as "Teams" for "Microsoft Teams."

    1.  Select **Applications**.

    2.  Select **Add application**.

    3.  Enter an application name in the **Name** field.

        For example, you could add the user-friendly name "Teams" for activities in both the native Microsoft Teams application and accessing the application in a browser.

    4.  Select **Save**.

5.  Identify which applications to categorize.

    1.  Select the Preview icon \(![Preview icon](../image/task-mining-preview-icon.png)\) in the **MAX** category.

    2.  Find the largest value in the **Duration \(sec\)** column and select the Create rule icon \(![Create rule icon](../image/task-mining-create-rule-icon.png)\) next to the application's name.

        You could also choose to create an application-based rule, for example, by finding an activity with a Microsoft Teams file name.

    The condition values in the categorization rules form are populated based on the activity record you selected.

6.  On the **Categorization Rule** form, fill in the fields.

    To match the activity record exactly, leave the default conditions as-is. To make a more generalized rule, leave the field empty to allow any value, or use \(.\*\) to replace any value with any number of characters.

    For a description of the field values, see [Categorization rule form in Task Mining](../reference/categorization-rules.md).

7.  Select **Save rule**.

    **Note:** To ensure that more granular rules for an application are applied before more general rules, place more granular rules before more general rules.

8.  Continue recalculating categorizing activities until uncategorized activities represent no more than about 10% of the total duration.


**Related topics**  


[Refine the presentation of your data](preview-data-based-on-categorization-rules.md)

