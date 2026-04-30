---
title: Create events content
description: Using Content Library, you can create content that announce events to your employees.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Content Library, Creating employee communications with Content Publishing, Manage, Employee Center, Employee Service Management]
---

# Create events content

Using Content Library, you can create content that announce events to your employees.

## Before you begin

Role required: sn\_cd.content\_manager, sn\_cd.content\_admin

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select **New** or existing content.

3.  Select **Portal** under the **Select the Platform** column.

4.  Select **Events** under the **Choose a content format** section.

5.  Select **Continue**.

6.  Fill in the fields in the **New content** form.

<table id="table_opy_zsv_hrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content name

</td><td>

The name that describes the content you are creating or editing.

</td></tr><tr><td>

Order

</td><td>

When you have multiple pieces of content that appear in a carousel, you can define the order they appear.Enter a number defining the order the content appears on the service portal or Employee Center. Content appears closer to the beginning of the carousel when assigned a lower number.

**Note:** Use increments of 100 when determining the order. This method makes it easier to edit. For example, you numbered your links 1, 2, 3, 4, 5 and wanted to place a new content after 2. You would have to renumber 3, 4, and 5. If you use 100, 200, and 300 and wanted to place content from 100 through 200, you would simply use any number from 101 through 199.

</td></tr><tr><td>

Active

</td><td>

Indicates the content is active and available for use.

</td></tr><tr><td colspan="2">

Content

</td></tr><tr><td>

Event start

</td><td>

The date and time the event begins.

</td></tr><tr><td>

Event end

</td><td>

The date and time the event ends.

</td></tr><tr><td>

User reference table

</td><td>

Determines the variables you can use to personalize text for the block content.Select **HR Profile** to select variables from the sn\_hr\_core\_profile table.

**Note:** When the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is activated, only **HR Profile** appears.

 Select **User** to select variables from the sys\_user table.

</td></tr><tr><td>

Rich text

</td><td>

Message for your event. Use the editing tools to format your text.Based on the table you select from the **User reference table** drop-down, you can customize your messages using variables from the table. For example, when **User** is selected from the **User reference table** drop-down, a list of variables appears in the **Fields** field. You can place a variable like **First name** so the message displays the user's first name and you don't have to add it manually.

</td></tr><tr><td>

Fields

</td><td>

Variables that customize the rich text of the event.The table you select from the **User reference table** drop-down determines what variables are available.

</td></tr></tbody>
</table>7.  Select **Save** to save the record and remain on the **Design** tab.

8.  Or, select **Save and continue** to save the record and move to the **Publish** tab.

    For information on publishing your content, see [Create a publish plan for your content](ec-content-library-publish2.md).

    To switch languages or translate your content, select the **Language settings** drop-down at the top, right side.

    To switch languages and have the fields on the form appear in a different language, select the **Switch language** button, at the top. This button only appears when the sn\_cd.enable\_language\_switching system property is activated. This is similar to changing your language at login. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    To request your content to be translated into a different language, select the **Translate content** button at the top. This button only appears when the sn\_cd.enable\_localization\_framework\_integration system property is activated. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    -   **Content Governance**

        When portal content is requested from Content Governance, the **Content Request Items** related list tab appears. Select the content request item to view information about the request. For more information, see [Edit a content request item](../concept/ec-content-gov-request.md#).

        When the **Content Request Item** has a state of **Work in Progress**, the **Send for Review** button appears.

        The content is sent to the **Opened by** or content requester person for review.

        **Note:** To edit the content after a review, the content request item state must be changed to **Work in Progress**.


