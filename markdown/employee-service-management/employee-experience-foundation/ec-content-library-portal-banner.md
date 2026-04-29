---
title: Create banner content
description: Using the Content Library, you can create banner content that appears on the employee portal.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Portal content, Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create banner content

Using the Content Library, you can create banner content that appears on the employee portal.

## Before you begin

Role required: sn\_cd.content\_manager

## About this task

Banner content appears at the top of the home page to display announcements and redirect users to a portal page or external link. A banner is comprised of a headline, heading, body text, and an optional button.

![Banner content includes headline, heading text, body text, and a button](../images/ec-rich-text-content.png)

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select **New** or existing content.

3.  Select **Portal** under the **Select the Platform** column.

4.  Select **Banner** under the **Choose a content format** section.

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

Active

</td><td>

Indicates the content is active and available for use.

</td></tr><tr><td>

User reference table

</td><td>

Determines which table provides the variables you can use to personalize text for employees. Selecting **User** allows you to insert variables from the sys\_user table to the Headline, Heading text, or Body text. The available variables depend on the user record, which is configured at the platform level.

 Since the banner design form does not display a list of available variables, you can [create a rich text content](ec-content-library-portal-richtext.md) item, to view all available variables from the sys\_user table.

 **Note:** When the Human Resources Scoped App: Core \(com.sn\_hr\_core\) plugin is activated, only **HR Profile** appears. Select **HR Profile** to use variables from the sn\_hr\_core\_profile table.

</td></tr><tr><td>

User column

</td><td>

Together with the HR profile \[sn\_hr\_core\_profile\] table, filters users when evaluating a condition.Only appears when you select the **HR Profile** from the **User reference table** field.

</td></tr><tr><td>

Headline

</td><td>

A title you want to appear for your content. This field is not required if you want your banner to show only a graphic.

</td></tr><tr><td>

Heading text

</td><td>

The headline you want to appear over the banner. Limit is 80 characters.You can use variables to customize the message for the reader. For example, insert `${name}` to display the employee's full name.

</td></tr><tr><td>

Body text

</td><td>

The detailed message you want to appear over the banner.You can use variables to customize the message for the reader.

</td></tr><tr><td>

Primary button

</td><td>

Use to display a button with a link to different content from your banner.Displays the **Button title** and **Button link** fields.

</td></tr><tr><td>

Button title

</td><td>

Text that labels the button or prompts the user to click.Only appears when the **Primary button** is switched to green.

</td></tr><tr><td>

Button link

</td><td>

A link to content that provides access after selecting the button.Only appears when the **Primary button** is switched to green.

 **Note:** Select the Lookup using list icon \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) to view a list of link content. This list matches the content you can select when selecting the down arrow key \(![Down arrow key](../images/down-arrow-icon.png)\). You can also select the Preview this record icon \(![Preview this record icon](../../human-resources/image/view-content-details-icon.png)\) to view the link content record.

</td></tr><tr><td>

Background imageClick to add an image

</td><td>

Link to add a background image to your banner.The recommended size for banners are:

-   Home page banner: 1440 x 400px
-   Topic page: 1258 x 300px


</td></tr></tbody>
</table>7.  Select **Save** to save the record and remain on the **Design** tab.

8.  Or, select **Save and continue** to save the record and move to the **Publish** tab.

    For information on publishing your content, see [Create a publish plan for your content](ec-content-library-publish2.md).

    To switch languages or translate your content, select the **Language settings** drop-down at the top, right side.

    To switch languages and have the fields on the form appear in a different language, select the **Switch language** button, at the top. This button only appears when the sn\_cd.enable\_language\_switching system property is activated. This is similar to changing your language at login. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    To request your content to be translated into a different language, select the **Translate content** button at the top. This button only appears when the sn\_cd.enable\_localization\_framework\_integration system property is activated. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md) and [Configure Localization Framework for Content Publishing](../concept/ec-int-localization-framework.md).

    -   **Content Governance**

        When portal content is requested from Content Governance, the **Content Request Items** related list tab appears. Select the content request item to view information about the request. For more information, see [Edit a content request item](../concept/ec-content-gov-request.md#).

        When the **Content Request Item** has a state of **Work in Progress**, the **Send for Review** button appears.

        The content is sent to the **Opened by** or content requester person for review.

        **Note:** To edit the content after a review, the content request item state must be changed to **Work in Progress**.


