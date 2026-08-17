---
title: Create announcements
description: Create announcements to highlight important content on the Employee Slate home page, such as new policies, required actions, or featured knowledge articles as a carousel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/eslate-create-employee-slate-announcement.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-05-28"
reading_time_minutes: 4
keywords: [employee communications, announcements, employee slate, content library, content versioning, version history, activate deactivate]
breadcrumb: [Employee communications, Working with Employee Slate capabilities, Employee Slate, Unified Employee Experience, Employee Service Management]
---

# Create announcements

Create announcements to highlight important content on the Employee Slate home page, such as new policies, required actions, or featured knowledge articles as a carousel.

## Before you begin

Role required: content\_manager or content\_admin

## About this task

You can create announcements from scratch or from existing knowledge articles and catalog items in one of the following ways.

-   Manual creation: Create announcements from scratch by entering all content manually in the editor view.
-   Conversational authoring: Prompt, chat, and generate announcements from existing knowledge articles or catalog items. For more information, see [Create an announcement using Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-create-announcement-with-now-assist.md).

## Procedure

1.  Go to your profile menu and select **Communications**.

    **Note:** The Communications link appears only for users with the content manager or content administrator role.

2.  Select **Create announcement** to go to the Editor page and fill in the following fields.

    1.  In the **Headline** field, enter a short title for the announcement.

        The headline appears in the Employee Comms widget and in any chat promotions.

    2.  In the **Body copy** field, specify the optional supporting text.

        This text displays when an employee opens the announcement.

    3.  Add an image by selecting **Choose file** and uploading a thumbnail image.

    4.  After uploading, adjust the focal point of the image by selecting and dragging within the image preview.

        **Note:** The selected target area of the image is visible as the focal point of the image. Verify the focal point positioning to confirm the image render on different widget aspect ratios.

        \[Omitted image "es-focal-point.png"\] Alt text: Set image focal point display

3.  Select the link in one of the following ways:

    1.  Configure the link by selecting an existing link from the reusable links table.

    2.  Create a new link.

        1.  Select **Create new link**.
        2.  Enter the name and select the type: knowledge article, catalog item, or external URL.
        3.  Enter the target URL and specify whether to open in the current tab or a new tab.
        4.  Add a link label for accessibility and promotional contexts.
4.  Determine the **Content priority** order: Critical, High, Medium, or Low.

    Priority combines with content freshness to determine the display order in the carousel. Higher priority values boost an announcement, but newer content with lower priority can still appear ahead of older high-priority content.

5.  Set the start date and time and the end date and time to configure the **Publishing** schedule.

    The announcement is visible only during this schedule.

6.  Configure **Add audience** targeting to target a specific audience beyond the user criteria of the linked content.

    **Note:** When you don't set any audience, the user criteria of the linked knowledge article or catalog item is applicable.

7.  Select **Promote** to boost content in chat and share the announcement through the chat channels such as Microsoft Teams.

    1.  Review and edit the promotional title and body text.

    2.  Set the promotion schedule, which can be independent of the publishing window.

8.  Select **Publish** to make the announcement live.

    The announcement appears in the Employee Comms widget according to the priority and freshness algorithm.

    **Note:** For a list of fields, see [Employee Slate announcement form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-employee-slate-announcement-fields.md).

    **Note:** Publishing creates a version of the announcement and locks the published content from further inline edits.


## Result

The announcement is now visible to employees who match the targeting criteria during the specified publishing window. If the content manager enables the chat promotion, the announcement also appears on the configured chat channels.

**Note:** When you create from existing content, the system inherits user criteria from the original knowledge article or catalog item.

You can also create an announcement from an existing knowledge article or catalog item by selecting **Create from article** or **Create from catalog item**.

## What to do next

After publishing an announcement, you can manage versions and visibility:

-   To change a published announcement, select **Edit** to create a new draft version, make your changes, and select **Publish** again. Publishing locks the announcement content.
-   To review prior versions, select the version history icon next to the editor title. An announcement can have a live version, a draft version awaiting publish, and one or more retired versions. Publishing a draft retires the previous live version.
-   To remove a live announcement from view without deleting it, select **Deactivate**. To restore it, select **Activate**.
-   To locate a specific version, filter announcements by active, inactive, or retired state.
-   To update a linked homepage promotion, edit it separately. Editing and publishing the announcement content doesn't automatically update the promotion.

**Related topics**  


[Create an announcement using Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-create-announcement-with-now-assist.md)

[Conversational authoring for announcements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/eslate-conversational-authoring-announcements.md)

