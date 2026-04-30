---
title: Enable user criteria for topics
description: Enable user criteria to configure topic-level access and visibility settings for topics in navigation and popular topics widget.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Unified Taxonomy for Employee Center, Setup Employee Center browse experience features, Configure, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Enable user criteria for topics

Enable user criteria to configure topic-level access and visibility settings for topics in navigation and popular topics widget.

## Before you begin

Role required: taxonomy\_admin

User criteria required: Taxonomy Manager, Taxonomy Contributor, Topic Manager, Topic Contributor.

**Important:** The Topic-based access control is available from the Yokohama family release.

When you have many topics, setting up user criteria for your topics can help with navigational ease and optimal performance.

## About this task

Organizations can define who the topic page is **Available for** and **Not Available for** at each topic level, avoiding the need to evaluate content-level access to determine topic visibility. Organizations can make subtopics automatically inherit the same access levels as the parent topic or define their own criteria.

**Note:** Remember that the topic visibility on the Mega menu and Popular topics, is driven by the Enable user criteria check option.

Before you configure topic-level visibility, understand the following user criteria basics:

-   Add topic-level hierarchy controls on each topic page overriding the default content-based security for megamenu.
-   Enable this option on the parent topics and the subtopics inherit the same user criteria automatically.
-   Remember that when you disable the topic user criteria toggle, the content security model is applicable.
-   Simplify the user criteria and improve the page load time.

## Procedure

1.  Navigate to **All** &gt; **Content Taxonomy** &gt; **Topics**.

2.  Click **New**.

3.  Configure the topic form, see [Topic form](../reference/topic-form.md).

4.  Select **Enable user criteria check** to set user criteria at topic-level.

    ![Associating topic to the related tabs](../images/associate-topics-tabs.png "User criteria and related tabs")

    Understand how it works from the note and proceed to add criteria for the following options:

    **Note:** Enable user criteria check to determine visibility of the current topic and its child topics in navigation and popular topics widget. The criteria set also applies to child topics. Criteria in connected content still govern content visibility on topic pages.

    -   **Available for**: Users or user group for whom the topic is visible.
    -   **Not available for**: Users or user group for whom the topic isn't visible.
    After you enable this option, the user criteria fields are available for the entire hierarchy that is root-topic and all its child-topics.

    **Note:** When you turn this **Enable user criteria check** option ON the first time, the default values for Available for and Not available for are empty, which means that the topic isn’t accessible by any user. Ensure you define the user criteria for the topic to be visible. When you don’t specify any values, the topic isn’t visible on the mega menu.

5.  Specify the user criteria **Available for** and **Not available for** options based on your business needs.

    Understand how the user criterion works in the following use cases:

    |Scenario|How user criteria works|
    |--------|-----------------------|
    |When a new topic is created with no parent|User criteria and visibility remain same as defined at the time of creation.|
    |When a new topic is created with parent|User criteria and visibility of parent is applied to the new topic.|
    |When a topic is moved to a new parent|User criteria and visibility of new parent are applied and old parent criteria are removed. Manual edits remain intact.|
    |When a topic is moved out of a hierarchy and made root topic \(new hierarchy\).|User criteria and visibility remain same as defined at the time of creation.|
    |When a topic is cloned to a new parent with empty user criteria.|User criteria and visibility of the topic are empty.|
    |When a topic is cloned to a new parent with non-empty user criteria.|User criteria and visibility of the new parent override the cloned topic.|
    |When user criteria and visibility of parent change|The revised user criteria and visibility are applied to its children.|
    |When user criteria is enabled for favorites|Employee \(for whom the topic isn’t available for\) isn’t able to view the favorited topic. The following message appears `You don't have access to <count> of your favorited items`. For more information, see [Configure favorites option](web-configure-favorites-admin.md).|
    |When a new topic is cloned and made root topic|The cloned topic user criteria and visibility are empty.|

    **Note:** When the user criteria applies on the favorited topic, where the topic isn't visible under **My Favorites**.

6.  Click **Submit** or **Save**.

    **Note:** Topics are visible based on the user criteria associated. For more information, see the **Favorites card and access** illustration on [Configure favorites option](web-configure-favorites-admin.md).


## Result

User criteria changes are available only after relogging. Proceed to check the topics visibility from the Employee Center portal.

## What to do next

Create child topics for the parent topic. For more information, see [Create a child topic](create-child-topics-for-parent.md). Go to the tabs to associate the topic appropriately. Child topics inherit the user criteria of the parent topic however admin can update the child-topic criteria separately as per business needs.

**Note:** When you clone or move a topic, the associated guided self-service also is cloned or moved accordingly.

