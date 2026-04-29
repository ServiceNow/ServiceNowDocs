---
title: Categorization concepts in Task Mining
description: Categorization rules organize and add context to your data by grouping similar workstation activities with user-friendly category names.
locale: en-US
release: australia
product: Task Mining
classification: task-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Task Mining, Platform Analytics]
---

# Categorization concepts in Task Mining

Categorization rules organize and add context to your data by grouping similar workstation activities with user-friendly category names.

## Purpose of categorization

Task Mining categorization determines how information displays in analyses and provides several benefits.

-   Grouping apps into categories makes dashboards more easily readable and enables you to distinguish between different types of activities.
-   Displaying only categorized apps avoids cluttering the analysis with unwanted information.
-   Anonymization of personal information such as a client name in window names for specific categories with replacement text you specify.
-   Grouping similar activities using categories and application groups making dashboards clearer.

## Categorization workflow

The process to categorize activities is as follows:

1.  A Task Mining analyst mines a sample of data of the applications and windows used in your project. Starting with mined data makes categorization easier as you have the exact values used to categorize activities already available in the data.

    For more information, see [Run a mining job](../task/mine-project-data.md).

2.  The Task Mining power user creates categorization rules with fixed order values that determine how data from apps and windows is shown on dashboards.

    For more information, see [Categorize workstation activities to simplify analysis](../task/define-default-categorization-rules.md).

3.  The Task Mining analyst previews the analysis to see how the collected data is visualized and handles requests.

    For more information, see [Refine the presentation of your data](../task/preview-data-based-on-categorization-rules.md).

4.  The Task Mining power user adjusts categorization rules. Applications and application categories are added and modified to provide more detail.
5.  A Task Mining analyst mines the project data again.
6.  Activities are categorized until uncategorized activities represent no more than approximately 10% of the total data. This level of detail provides a comprehensive view. Further refinement beyond this amount provides diminishing returns.

## Predefined categorization rules

Rules are ordered to define which rule applies first. The following five categorization rules can't be changed. These rules are ordered 1,2,3,4 and MAX. The first four rules apply first by default, and the MAX rule applies last.

1.  **Private**: Defines the activity as non-productive, and is used when the agent is in private mode and used when activities are defined as private.
2.  **Lock**: Defines the activity as a break, and is used when the workstation is locked.
3.  **Off**: Defines the activity as off, and is used when the workstation is turned off.
4.  **Idle**: Defines the activity as idle, and is used on analyses during targeted recordings when the agent is idle.
5.  **MAX**: Applies to uncategorized apps that don’t match any rule and are anonymized by default.

## Category and application names

Organizing your activities with categories and application names adds context to your data by grouping similar workstation activities with user-friendly names. Add sensible category and application names to the list available on the categorization rule form before creating the rule for the activity.

-   **Category**

    Describes the type of work that applications are related to. Don't use the **Other** category as other is used by the Max rule and represents uncategorized apps that don’t match any rule. For example, if you have an app that doesn't fit any category, either use Misc or add a category to the list available on the categorization rule form to describe the type of work that application is related to.

-   **Application**

    Describes the application names available for creating categorization rules. Don't use an application name with more than one category as it corrupts the treemap chart. For example, you could use the user-friendly application name "Teams" with categories Communication or Core Desktop Apps. However, if you create rules for activities in both the native application and accessing the application in a browser, don't use different categories for the two rules.


**Related topics**  


[Categorize workstation activities to simplify analysis](../task/define-default-categorization-rules.md)

[Refine the presentation of your data](../task/preview-data-based-on-categorization-rules.md)

