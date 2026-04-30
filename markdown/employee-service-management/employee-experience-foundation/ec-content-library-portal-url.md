---
title: Create URL content
description: Using the Content Library, you can create URL content containing a link to information.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Portal content, Creating employee communications, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create URL content

Using the Content Library, you can create URL content containing a link to information.

## Before you begin

Role required: sn\_cd.content\_manager

Define the link: [Add or modify links to other content sources](ecpro-manage-link-content.md)

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library** &gt; **New**.

2.  Select **Portal** under the **Select the Platform** column.

3.  Select **URL** under the **Choose a content format** section.

4.  Select **Continue**.

5.  Fill in the fields in the **New content** form.

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

Link

</td><td>

The URL link to content you want to appear for your employees.Select the Lookup using list icon \(![Lookup using list icon](../../human-resources/image/magnify-glass-outline-icon.png)\) to view a list of link content. This list matches the content you can select when selecting the down arrow key \(![Down arrow key](../images/down-arrow-icon.png)\).

**Note:** Depending on your configurations or extensions, your link may open in a new window.

</td></tr></tbody>
</table>6.  Select **Save** to save the record and remain on the **Design** tab.

7.  Or, select **Save and continue** to save the record and move to the **Publish** tab.

    For information on publishing your content, see [Create a publish plan for your content](ec-content-library-publish2.md).

    To switch languages or translate your content, select the **Language settings** drop-down at the top, right side.

    To switch languages and have the fields on the form appear in a different language, select the **Switch language** button, at the top. This button only appears when the sn\_cd.enable\_language\_switching system property is activated. This is similar to changing your language at login. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    To request your content to be translated into a different language, select the **Translate content** button at the top. This button only appears when the sn\_cd.enable\_localization\_framework\_integration system property is activated. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    -   **Content Governance**

        When portal content is requested from Content Governance, the **Content Request Items** related list tab appears. Select the content request item to view information about the request. For more information, see [Edit a content request item](../concept/ec-content-gov-request.md#).

        When the **Content Request Item** has a state of **Work in Progress**, the **Send for Review** button appears.

        The content is sent to the **Opened by** or content requester person for review.

        **Note:** To edit the content after a review, the content request item state must be changed to **Work in Progress**.


