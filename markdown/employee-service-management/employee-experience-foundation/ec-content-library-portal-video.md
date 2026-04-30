---
title: Create video content
description: Using the Content Library, you can create video content to appear on the employee portal.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Portal content, Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create video content

Using the Content Library, you can create video content to appear on the employee portal.

## Before you begin

Role required: sn\_cd.content\_manager

To add features to your video link like heading text, body text, text color, background color, and background image, use Portal Styled content from the **Content Library**. For more information, see [Create customized media with styled content](ec-content-library-portal-styled.md).

## About this task

The Content Library supports the following types of video:

-   HTML5

    **Note:** Hover text or tooltips are not supported for HTML5 at this time.

-   YouTube
-   Vimeo

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select **New** or existing content.

3.  Select **Portal** under the **Select the Platform** column.

4.  Select **Video** under the **Choose a content format** section.

5.  Select **Continue**.

6.  Fill in the fields in the **New content** form.

<table id="table_nc1_ttv_frb"><thead><tr><th>

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

Video URL

</td><td>

The link to the video you want to appear as content.Only YouTube and Vimeo videos are supported at this time. Ensure you use the embedded video link.

 Select the Lookup using list icon \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) to view a list of link content. This list matches the content you can select when selecting the down arrow key \(![Down arrow key](../images/down-arrow-icon.png)\). You can also select the Preview this record icon \(![Preview this record icon](../../human-resources/image/view-content-details-icon.png)\) to view the link content record.

**Note:** Depending on your configurations or extensions, your link may open in a new window.

</td></tr></tbody>
</table>7.  Select **Save** to save the record and remain on the **Design** tab.

8.  Or, select **Save and continue** to save the record and move to the **Publish** tab.

    To switch languages or translate your content, select the **Language settings** drop-down at the top, right side.

    To switch languages and have the fields on the form appear in a different language, select the **Switch language** button, at the top. This button only appears when the sn\_cd.enable\_language\_switching system property is activated. This is similar to changing your language at login. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    To request your content to be translated into a different language, select the **Translate content** button at the top. This button only appears when the sn\_cd.enable\_localization\_framework\_integration system property is activated. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    For information on publishing your content, see [Create a publish plan for your content](ec-content-library-publish2.md).

    -   **Content Governance**

        When portal content is requested from Content Governance, the **Content Request Items** related list tab appears. Select the content request item to view information about the request. For more information, see [Edit a content request item](../concept/ec-content-gov-request.md#).

        When the **Content Request Item** has a state of **Work in Progress**, the **Send for Review** button appears.

        The content is sent to the **Opened by** or content requester person for review.

        **Note:** To edit the content after a review, the content request item state must be changed to **Work in Progress**.


