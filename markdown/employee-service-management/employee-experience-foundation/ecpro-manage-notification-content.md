---
title: Create email, SMS, or push notification content
description: Use Notification Content to send an information blast directly to your employees via email, SMS, or push to their mobile devices. Notifications can be used to direct users to the portal for detailed information.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Notification content, Creating employee communications, Managing employee communications, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Create email, SMS, or push notification content

Use Notification Content to send an information blast directly to your employees via email, SMS, or push to their mobile devices. Notifications can be used to direct users to the portal for detailed information.

## Before you begin

Role required: sn\_cd.content\_manager

## Procedure

1.  Navigate to **Content Publishing** &gt; **Content Library**.

2.  Select **New** or existing content.

3.  Select **Notification** under the **Select the Platform** column.

4.  Select **Email** or **Push** under **Choose a content format**.

5.  Fill out the new notification content form:

<table id="table_rkb_p1z_vfb"><thead><tr><th>

Field

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

Title

</td><td>

A descriptive title of the notification. The title is not the subject of the notification, although they can be identical.

</td></tr><tr><td colspan="2">

If you select the **Email** content type, provide the following information:**Note:** You will configure recipients as part of a publish plan or in a campaign. The email will be individually addressed to the first listed user, while the remaining users will be blind copied \(BCC\).

</td></tr><tr><td>

From

</td><td>

The email address of the person or organization you want the notification to come from. Use the format `admin@example.com`. **Note:** The system does not support string-type inputs, such as `Administrator<admin@example.com>`.

</td></tr><tr><td>

Reply to

</td><td>

The email address that can accept a reply when you want your audience to be able to respond to the notification. Use the format `admin@example.com`. **Note:** The system does not support string-type inputs, such as `Administrator<admin@example.com>`.

</td></tr><tr><td>

Subject

</td><td>

The subject of the notification, similar to the subject line in an email.

</td></tr><tr><td>

Use block content

</td><td>

You can select reusable block content for your notification message. For more information, see [Add or modify block content](ecpro-manage-block-content.md).

</td></tr><tr><td>

Block content

</td><td>

Click the **Lookup using list** icon to select the block content you want for your notification message.Only appears when you select the **Use block content** check box.

</td></tr><tr><td>

Active

</td><td>

Indicates that the notification is active and available.**Note:** Your content must be active in order to publish it.

</td></tr><tr><td>

Body

</td><td>

The body or message of the notification.When you insert an image, use 1440 x 600 pixels \(px\) and a file size of 100–500 kilobytes \(KB\). A file size of 100 KB is optimal.

 This field only appears when Content type is email.

**Note:** Optimize your image. It improves performance on the service portal. Also, use SVG files for optimal quality.

</td></tr><tr><td colspan="2">

If you select the **Push** content type, provide the following information:

</td></tr><tr><td>

Description

</td><td>

The message you want to send via push. You are limited to 1600 characters.

</td></tr></tbody>
</table>6.  Select **Submit** or **Update** to save and return to the Notification Content list.

    Go to Schedule Content to define the audience, date, and time your content is available. For more information, see [Scheduling the delivery of content](ecpro-schedule-content.md). Or, go to Manage Content to add your content to a campaign bundle. For more information, see [Create campaign bundles/stages](ecpro-manage-campaign-bundles.md).

    To request your content to be translated into a different language, select the **Translate content** button at the top. This button only appears when the sn\_cd.enable\_localization\_framework\_integration system property is activated. For more information, see [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md).

    **Note:** Integration with Localization Framework is not available for Push or SMS content.


