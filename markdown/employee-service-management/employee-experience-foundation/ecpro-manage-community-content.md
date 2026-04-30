---
title: Add or modify forum content
description: Provide content to your employees through employee forums.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Employee Forums, Creating employee communications, Manage, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Add or modify forum content

Provide content to your employees through employee forums.

## Before you begin

Role required: sn\_cd.content\_manager

## About this task

Creating forum content also requires the following to post to a community or forum:

-   A forum to post community content. For information on creating forums, see [Configure community forums](https://www.servicenow.com/docs/access?context=configure-forums-topics&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).
-   The `Content Publishing: Post to Forums` scheduled job runs every hour by default to process posts. For more information on scheduled jobs, see [Components installed with Content Publishing](../reference/installed-with-content-delivery.md).

**Note:** The Communities \(com.sn\_communities\) plugin must be activated in order to use this feature.

## Procedure

1.  Navigate to **All** &gt; **Content Publishing** &gt; **Content Library** &gt; **Community**.

2.  On the form, fill in the fields.

<table id="table_j5v_qvp_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title or name that identifies the community post.

</td></tr><tr><td>

Content type

</td><td>

Classification of the community post. Fields used to define the post change based on the content type selection.-   Community Blog
-   Community Event
-   Community Video
-   Forums Post List \(lists posts from a specific forum\)
 **Note:** For more information on community content types, see [Community content types](https://www.servicenow.com/docs/access?context=c_communities-content-types&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US).

</td></tr><tr><td>

Active

</td><td>

Indicates that the community post is active and available to post.

</td></tr></tbody>
</table>    Fields change depending on which content type you select.

    **Community Blog**

<table id="table_bsk_fbx_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Use block content

</td><td>

Indicates that you are using block content and not rich text. For information on creating block content, see [Add or modify block content](ecpro-manage-block-content.md).

</td></tr><tr><td>

Block content

</td><td>

Appears when you check the **Use block content** box. Click to access existing block content or to create content for your community blog.

</td></tr><tr><td>

Description

</td><td>

Appears when the **Use block content** box is unchecked.Enter rich text for your community blog.

</td></tr></tbody>
</table>    Community Event if you select **Virtual event**, the fields are different.

<table id="table_eh2_3bx_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show attendee list

</td><td>

Indicates that attendees can view a list of other attendees.

</td></tr><tr><td>

Attendee limit

</td><td>

Determines the maximum number of attendees that can attend the event.

</td></tr><tr><td>

Virtual event

</td><td>

Indicates that event is online. When checked, the Event URL, Start time, and End time fields appear.

</td></tr><tr><td>

Event URL

</td><td>

The URL link to the virtual meeting.

</td></tr><tr><td>

Start time

</td><td>

The date and time the virtual event begins.

</td></tr><tr><td>

End time

</td><td>

The date and time the virtual event ends.

</td></tr><tr><td>

Location name

</td><td>

The name or description of the event location.

</td></tr><tr><td>

Street

</td><td>

The street address of the event location.

</td></tr><tr><td>

City

</td><td>

The city of the event location.

</td></tr><tr><td>

Zip / postal code

</td><td>

The zip or postal code of the event location.

</td></tr><tr><td>

Time zone

</td><td>

The time zone of the event location.Used to determine the event scheduling and reminder.

</td></tr><tr><td>

Event reminder

</td><td>

Indicates when you want an event reminder sent.

</td></tr><tr><td>

State / province

</td><td>

The state or province of the event location.

</td></tr><tr><td>

Country

</td><td>

The country of the event location.

</td></tr><tr><td>

Description

</td><td>

A description of the event.

</td></tr></tbody>
</table>    **Community Video**

<table id="table_utw_sbx_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Video

</td><td>

Link to the video you want to post to your community, use as part of a campaign, or post to the Employee Center. Videos appear as web URLs that link to popular video sites. Supported video link hosts are:

 -   dailymotion.com
-   facebook.com
-   vimeo.com
-   youtube.com
 For more information on video content, see [Add or modify links to other content sources](ecpro-manage-link-content.md).

</td></tr><tr><td>

Description

</td><td>

Description of the video.

</td></tr></tbody>
</table>    **Forums Post List**

<table id="table_qlr_wbx_cfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

List type

</td><td>

How you want the posts from a forum to appear on the Employee Center.-   Manual List: You decide the order and content links to appear.
-   Dynamic List: Automatically generated list.


</td></tr><tr><td>

Forum links

</td><td>

Determines what forum links you want to appear on the Employee Center.Appears when you select **Manual List** from **List type**.

 Click the **Unlock forum links** icon and select the links you want to appear.

 **Note:** The first forum link you select appears first on the Employee Center.

</td></tr><tr><td>

Dynamic list type

</td><td>

The method your posts appear in the forum list.-   Recently Added: The most recently added forum posts appear.
-   Most Popular: Forum posts that
 Appears when you select **Dynamic** in **List type**.

</td></tr><tr><td>

Number of list items

</td><td>

The number of forum posts you want to appear.Only appears when you select **Most Popular** from **Dynamic list type**.

</td></tr></tbody>
</table>    **Community Blog**

3.  Click **Save** to save and remain on the form, or click **Update** to save and return to the Community Content list.


## What to do next

-   Go to Schedule Content to define the audience, date, and time your content is available. For more information, see [Scheduling the delivery of content](ecpro-schedule-content.md).

    **Note:** If you edit published forum content, you must create a new Schedule content record to publish the updates.

-   Or, go to Campaign Content to add your content to a campaign bundle. For more information, see [Create campaign bundles/stages](ecpro-manage-campaign-bundles.md).

