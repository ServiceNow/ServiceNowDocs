---
title: Create rich text content
description: Using the Content Library, you can create rich text content, which enables you to format your text in a creative and attention-grabbing way.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Portal content, Creating employee communications, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create rich text content

Using the Content Library, you can create rich text content, which enables you to format your text in a creative and attention-grabbing way.

## Before you begin

Role required: sn\_cd.content\_manager

Rich text can be built using reusable block content. For more information, see [Add or modify block content](ecpro-manage-block-content.md).

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select **New** or existing content.

3.  Select **Portal** under the **Select the Platform** column.

4.  Select **Rich text** under the **Choose a content format** section.

5.  Select **Continue**.

6.  Fill in the fields in the **New content** form.

<table id="table_vrw_sql_xrb"><thead><tr><th>

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

</td></tr><tr><td>

Use block content

</td><td>

You can create rich text or use block content for portal content.Select the toggle switch to show the Block content field.

</td></tr><tr><td>

Block content

</td><td>

The block content you want to appear on the Employee Center.Only appears when you select the **Use block content** toggle switch.

 Select the Lookup using list icon \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) to view a list of link content.

</td></tr><tr><td>

User reference table

</td><td>

Determines the variables you can use to personalize text for the **Rich text** field.Appears when the **Use block content** is turned off.

 Select **HR Profile** to select variables from the sn\_hr\_core\_profile table.

**Note:** When the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is activated, only **HR Profile** appears.

 Select **User** to select variables from the sys\_user table.

</td></tr><tr><td>

User column

</td><td>

Together with the HR profile \[sn\_hr\_core\_profile\] table, filters users when evaluating a condition.Only appears when you select the **HR Profile** from the **User reference table** field.

</td></tr><tr><td>

Rich text

</td><td>

Message you want to appear as portal content. Use the editing tools to format your text.**Note:** When translating rich text, the HTML sanitizer can remove HTML formatting to protect against security concerns. For more information, see [HTML sanitizer](https://www.servicenow.com/docs/access?context=c_HTMLSanitizer&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

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


