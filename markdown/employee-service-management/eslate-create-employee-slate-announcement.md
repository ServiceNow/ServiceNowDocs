---
title: Create an Employee Slate announcement
description: Create announcements to highlight important content on the Employee Slate home page, such as new policies, required actions, or featured knowledge articles as a carousel.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 3
keywords: [employee communications, announcements, Employee Slate, content library]
breadcrumb: [Employee communications, Working with Employee Slate capabilities, Employee Slate, Employee Service Management]
---

# Create an Employee Slate announcement

Create announcements to highlight important content on the Employee Slate home page, such as new policies, required actions, or featured knowledge articles as a carousel.

## Before you begin

Role required: content\_manager or content\_admin

## About this task

You can create announcements from scratch or from existing knowledge articles and catalog items in one of the following ways.

-   Manual creation: Create announcements from scratch by entering all content manually in the editor view.
-   Conversational authoring: Prompt, chat, and generate announcements from existing knowledge articles or catalog items. For more information, see [Create an announcement using chat](eslate-create-announcement-with-now-assist.md)

## Procedure

1.  Navigate to your profile menu and select **Communications**.

    **Note:** The Communications link appears only for users with the content manager or content administrator role.

2.  Select **Create announcement** to go to the Editor page and fill in the following fields.

    1.  In the **Headline** field, enter a short title for the announcement.

        The headline appears in the Employee Comms widget and in any chat promotions.

    2.  In the **Body copy** field, enter optional supporting text.

        This text displays when an employee opens the announcement.

    3.  Add an image by selecting **Choose file** and uploading a thumbnail image.

    4.  After uploading, set the focal point by clicking and dragging within the image preview.

        **Note:** Verify the focal point positioning to confirm the image renders correctly across different widget aspect ratios.

    **Note:** For a list of fields, see [Employee Slate announcement form](../reference/eslate-employee-slate-announcement-fields.md).

3.  Select the link in one of the following ways:

    1.  Configure the link by selecting an existing link from the reusable links table.

    2.  Create a new link.

        1.  Select **Create new link**.
        2.  Enter the name and select the type: knowledge article, catalog item, or external URL.
        3.  Enter the target URL and specify whether to open in the current tab or a new tab.
        4.  Add a link label for accessibility and promotional contexts.
4.  Set the **Content priority** level: Critical, High, Medium, or Low.

    Priority combines with content freshness to determine display order in the carousel. Higher priority values boost an announcement, but newer content with lower priority can still appear ahead of older high-priority content.

5.  Set the start date and time and end date and to configure the Publishing schedule.

    The announcement is visible only during this time window.

6.  Configure **Add audience** targeting if you need precise control beyond the user criteria from linked content.

    **Note:** When no audience is set, the system uses the user criteria from the linked knowledge article or catalog item.

7.  Select **Promote** to boost content in chat and share the announcement through the chat channels such as Microsoft Teams.

    1.  Review and edit the promotional title and body text.

    2.  Set the promotion schedule, which can be independent of the publishing window.

8.  Select **Publish** to make the announcement live.

    The announcement appears in the Employee Comms widget according to the priority and freshness algorithm.


## Result

The announcement is now visible to employees who match the targeting criteria during the specified publishing window. If the content manager enables the chat promotion, the announcement also appears on the configured chat channels.

**Note:** When creating from existing content, the system inherits user criteria from the original knowledge article or catalog item.

You can also create an announcement from an existing knowledge article or catalog item by selecting Create from article or Create from catalog item.

**Related topics**  


[Create an announcement using chat](eslate-create-announcement-with-now-assist.md)

[Conversational authoring for announcements](../concept/eslate-conversational-authoring-announcements.md)

