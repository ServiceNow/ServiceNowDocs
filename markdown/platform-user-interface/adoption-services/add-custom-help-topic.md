---
title: Add custom Embedded Help content
description: You can add a custom Embedded Help topic, for example, if you have a custom application and you want to provide help to users.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Add custom Embedded Help content

You can add a custom Embedded Help topic, for example, if you have a custom application and you want to provide help to users.

## Before you begin

Role required: embedded\_help\_admin or admin

## About this task

When you write content for your users, keep the following limitations in mind.

-   You cannot include images in embedded help content.
-   To embed video, you must code the video information in the source code &lt;**&lt;&gt;**&gt; view. Video content from YouTube and Vimeo are supported.
-   To add a related information link, you must use a full URL, not a relative URL.
-   Best practice is not to use the highlight text tool, as the color may make text unreadable depending on the theme the user has selected.
-   Any changes you make to embedded help are not automatically deployed to another instance.
-   Changes to the embedded help table are not captured in update sets, update\_sync=false is set intentionally.

**Note:** Embedded help records are also used to create content for the Help Center within a configurable workspace. For more information, see [Create Help Center content for configurable workspace](../../adoption-services/task/create-help-center-content.md).

## Procedure

1.  Navigate to **All** &gt; **Embedded Help** &gt; **Help Content**.

2.  Select **New**.

3.  Complete the form.

<table id="table_osr_qms_5y"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter the Embedded Help topic name. A typical name is the title of the page to which it applies.

</td></tr><tr><td>

Page

</td><td>

Enter the UI page this content provides help for, without the .do file extension.![Page name in the URL](../image/embedded-help-url-page.png)

**Note:** If you're using the embedded help record to display in the Help Center, as described in [Create Help Center content for configurable workspace](../../adoption-services/task/create-help-center-content.md), enter the same value in the **Name** and **Page** fields, replacing spaces with underscores in the **Page** field.

</td></tr><tr><td>

Modifier

</td><td>

Select the modifier, typically **Normal**.-   **Normal** content appears for any user with the appropriate role who navigates to the page.
-   **Setup** content appears when the page is accessed from a link in Guided Setup.


</td></tr><tr><td>

Role

</td><td>

Select the role that the topic is written for. All roles that contain the role also see the content, unless another topic targeted to their role exists for the same page. For more information, see [Embedded Help roles](../concept/embedded-help-roles.md)

</td></tr><tr><td>

Active

</td><td>

Select the check box to make this content appear. Clear the check box to hide the content from being available, for example, to have someone review it before it is accessed on the UI page.

</td></tr><tr><td>

Product

</td><td>

**Enterprise** is the default, and should not be changed.

</td></tr><tr><td>

Qualifier

</td><td>

The qualifier that provides custom embedded help for a common UI page.For example, the `home.do` page is opened for every Homepage module and for many Dashboard modules. Create the qualifier before you enter it into this embedded help record.

**Note:** Dynamic IDs are supported in Embedded Help Qualifier route parameters. For example, adding `$dynamic_value$` in the fragment field makes your content available for the same URL, even when the value changes. This can happen when selecting different languages for the same page.

</td></tr><tr><td>

Version

</td><td>

Select a version, if different from the current version of your instance. To provide content for a custom application or information relevant to your organization business process, select **All**.

</td></tr><tr><td>

Order

</td><td>

Change the default role, if needed. The order defaults based on the selected role. For more information about default order priority numbers, see [Embedded Help roles](../concept/embedded-help-roles.md).

</td></tr><tr><td>

Domain

</td><td>

Specify the domain this content is used for, if applicable.This field appears in the form if the administrator configured the form to display it.

</td></tr></tbody>
</table>4.  In the **Content** field, enter the text using the HTML formatting tools as needed.

    If you add a link, enter the full URL to the web page. A good practice is to select **New window \(\_blank\)** as the **Target**.

    **Note:** Do not add images in an embedded help topic. Images are removed from the content section when the record is saved.

    To add an embedded video, see [Embed video content in help topics](embed-video-help-content.md).

5.  To add another line below tables, videos, or related links, select the newline icon \(**⏎**\).

6.  Select **Submit**.


**Parent Topic:**[Configure Embedded Help](../concept/configuring-embedded-help.md)

