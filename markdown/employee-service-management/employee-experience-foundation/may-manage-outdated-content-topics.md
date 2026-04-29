---
title: Manage outdated connected content
description: Improve performance by tracking and removing outdated content from connected content from a dedicated tab. .
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Taxonomy and connected content, Setup Employee Center browse experience features, Configuring Employee Center, Employee Center, Unified Employee Experience, Employee Service Management]
---

# Manage outdated connected content

Improve performance by tracking and removing outdated content from connected content from a dedicated tab. .

## Before you begin

**Important:** The outdated connected content management is available from the Zurich family release.

Role required: taxonomy\_admin.

User criteria required: Taxonomy Manager, Taxonomy Contributor, Topic Manager, Topic Contributor.

## About this task

Outdated content refers to obsolete, invalid, or stale content that is no longed aligned to user needs or organizational priorities.

-   Use one-click and bulk actions to remove all outdated content associations while preserving source content​.
-   Manage content integrity and improve system performance.
-   Gain visibility and optimize content operations.

![See how the outdated connected content tab and interface looks](../images/outdated-connected-content-ui.png "Outdated connected content tab and interface")

## Procedure

1.  Go to **All** &gt; **Content Taxonomy** &gt; **Content Configuration**.

2.  Click one of the following records.

    -   **Knowledge**
    -   **Catalog**
    -   **Quick links**
    Taxonomy content configuration information appears along with the related list.

3.  Select one of the following tabs:

    |Field|Value|
    |-----|-----|
    |Connected Content|Connected content table, reference information, and display filter of the selected record.|
    |Connected Category|Category linked to the topic pages based on the content type.|
    |Outdated Connected Content|The number of outadated content records detected on the linked category.|

4.  Go to the **Outdated Connected Content** tab to use the default conditions.

    ![Outdated connected content count and default filters](../images/outdated-connected-content.png "Outdated Connected Content conditions")

5.  Customize the filter conditions to suit your requirements.

6.  Click **No. of records matching the condition** to see the outdated content.

    When appropriate conditions are selected, all the outdated content appears in the matching records for you to manage.


## Result

Based on the filter conditions, the outdated, retired knowledge, and inactive catalog items appear under the **Outdated Connected Content** related list.

**Note:** When a category has outdated content, then the same isn't associated to the topic. Ensure you mark the connected catalog item as active to be able to associate.

## What to do next

To see a full list, go to **All** &gt; **Content Taxonomy** &gt; **Outdated Content Configuration**View **Connected Content View:Outdated Connected Content** to see the list.

You can proceed to manage the outdated content manually or automatically. Here's what you can do:

-   \(For topic-level outdated content\) Go to **All** &gt; **Content Taxonomy** &gt; **Topics**, click **Outdated Connected Content** tab, and select the outdated content to delete.
-   \(For a full-list of outdated content across topics and taxonomies\) Go to **All** &gt; **Content Taxonomy** &gt; **Outdated Content Configuration**, and select the outdated content to delete.

Review and delete outdated content across all topics and taxonomies with an automated option through a scheduled job.

**Note:** When you delete, only the association with the topic and taxonomies is removed. The actual catalog item or the knowledge article is not deleted.

For more information, see [Run the scheduled job for outdated content](may-scheduled-job-content-outdated.md).

-   **[Run the scheduled job for outdated content](may-scheduled-job-content-outdated.md)**  
Auto-delete the outdated content by marking the schedule job active. Once the schedule job is active, all the outdated content is removed automatically.

**Parent Topic:**[Taxonomy and connected content](../concept/track-new-content.md)

