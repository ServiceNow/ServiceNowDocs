---
title: Creating to-do content
description: Use Content Publishing to create links between a banner or styled content items and to-dos content items.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [To-do content, Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Creating to-do content

Use Content Publishing to create links between a banner or styled content items and to-dos content items.

The two ways of delivering to-do links are:

-   Scheduled Content \(Content Publishing\)
-   Campaigns \(Content Experiences\)

Create to-do links for your banner or styled content items to make it easier to access. Placing to-do links in a banner or styled content makes it highly visible for high priority to-do tasks.

## Process for Content Publishing

To create to-do links for a banner or styled content, do the following:

-   Create to-do content: For more information, see [Create to-do content](../task/ecpro-manage-content-to-do.md).
-   Create link content referencing your to-do content: For details, see [Add or modify links to other content sources](../task/ecpro-manage-link-content.md)

    **Note:** Select **To-do** in the **Type** field. And, select the to-do content you created previously from the **To-do content** list.

    .

-   Create portal content that references your link content.
-   Schedule your content using Content Publishing.
    -   Schedule the portal content \(banner or styled content\).

        **Note:** Your to-do content automatically schedules when you schedule your portal content \(banner or styled content\).

    -   The to-do scheduled content appears in the **To-do scheduled content** field after you select **Save**. Your to-do content also aligns with the schedule of your portal content.
    -   The to-do content is automatically scheduled separately when the link content is scheduled.
    -   For more information, see [Scheduling the delivery of content](../task/ecpro-schedule-content.md).
    -   The Content Publishing: Create To-dos scheduled job must run before the content becomes available.

## Process for Content Experiences \(campaigns\)

To create to-do links for a banner or styled content within a campaign, you must first have a campaign with stages and content. For more information, see [Creating campaigns](ecpro-campaigns.md). Use the same steps in Content Publishing, but instead of scheduling your content, add it to a campaign stage.

-   Create to-do content.
-   Create link content referencing your to-do link content.
-   Create portal content that references your link content.
-   Add your portal content to a stage/bundle as an activity in your campaign.
    -   You can use the legacy lists and forms or the campaign builder UI to add your portal content.
    -   For more information, see [Create a campaign](../task/ecpro-manage-campaigns.md).
-   If you use the campaign builder UI, you will see the banner and link content.

    ![Schedule of content view: Portal content and linked content](../images/content-exps-to-do-link.png)

-   Use Portal preview to view your content. For details, see [Campaign preview](ecpro-campaign-preview.md).
-   After verifying your content, publish it.

    **Note:** You cannot delete the link content without deleting the banner \(parent\) content. You also cannot move the link content to another stage \(bundle\) without moving the banner \(parent\) content.


