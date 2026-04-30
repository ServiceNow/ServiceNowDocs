---
title: To-do content
description: You can assign tasks to your employees that prompts them to take action.You can assign tasks to your employees that prompts your employees to take action. You can also have the to-do as part of a campagin or trigger additional content once a task is completed. To-dos can also be sent via email.Use Content Publishing to create links between a banner or styled content items and to-dos content items.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Content Library, Creating employee communications with Content Publishing, Manage, Employee Center, Employee Service Management]
---

# To-do content

You can assign tasks to your employees that prompts them to take action.

The types of to-do content you can create are:

-   Button Complete
-   E-Signature
-   Play Video
-   View Link

For more information on creating to-do content, see [To-do content form](../reference/to-do-content-form.md).

You can also create to-do content that appears in a banner or styled content. For more information, see [Creating to-do content](ec-to-do-content.md#).

## Create to-do content

You can assign tasks to your employees that prompts your employees to take action. You can also have the to-do as part of a campagin or trigger additional content once a task is completed. To-dos can also be sent via email.

### Before you begin

Role required: sn\_cd.campaign\_manager

### About this task

For example, an Open Enrollment for Benefits campaign can have tasks that appear as to-dos. These tasks prompt employees to sign up for health care.

### Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select **New** or existing content.

3.  Select **To-do** under the **Select the Platform** column.

4.  Select **Button Complete**, **E-Signature**, **Play Video**, or **View Link**.

5.  Fill in the form.

    For more information on each field, see [To-do content form](../reference/to-do-content-form.md).

6.  Select **Submit** or **Save**.

    The Schedule Content related list appears. For more information on scheduling your content, see [Scheduling the delivery of content](../task/ecpro-schedule-content.md).

    If you want your to-do content to be a link you can add to a banner or styled content, see [Add or modify links to other content sources](../task/ecpro-manage-link-content.md).

    To request your content to be translated into a different language, select the **Translate content** button at the top. This button only appears when the sn\_cd.enable\_localization\_framework\_integration system property is activated. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).


## Creating to-do content

Use Content Publishing to create links between a banner or styled content items and to-dos content items.

The two ways of delivering to-do links are:

-   Scheduled Content \(Content Publishing\)
-   Campaigns \(Content Experiences\)

Create to-do links for your banner or styled content items to make it easier to access. Placing to-do links in a banner or styled content makes it highly visible for high priority to-do tasks.

### Process for Content Publishing

To create to-do links for a banner or styled content, do the following:

-   Create to-do content: For more information, see [Create to-do content](ec-to-do-content.md#).
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

### Process for Content Experiences \(campaigns\)

To create to-do links for a banner or styled content within a campaign, you must first have a campaign with stages and content. For more information, see [Creating campaigns with Content Experiences](ecpro-campaigns.md). Use the same steps in Content Publishing, but instead of scheduling your content, add it to a campaign stage.

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


