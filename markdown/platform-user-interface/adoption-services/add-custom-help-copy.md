---
title: Add custom Embedded Help from a copy
description: To customize embedded help for your organization, you can edit a topic in the base system and save it as a copy.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Add custom Embedded Help from a copy

To customize embedded help for your organization, you can edit a topic in the base system and save it as a copy.

## Before you begin

Role required: embedded\_help\_admin or admin

## About this task

In base system topics, the read-only **ServiceNow Help** check box is selected. When you create a copy, the **ServiceNow Help** check box is cleared, allowing you to modify the content.

When a user navigates to a UI page for which custom content exists, the custom content displays instead of the base system content.

**Note:** Embedded help records are also used to create content for the Help Center within a configurable workspace. For more information, see [Create Help Center content for configurable workspaces](../../adoption-services/task/create-help-center-content.md).

## Procedure

1.  Navigate to **All** &gt; **Embedded Help** &gt; **Help Content**.

2.  Open the embedded help topic to copy.

    You can also open an embedded help topic by selecting **Edit Help Article** from the menu in the embedded help pane.

3.  Update the fields as appropriate.

<table id="table_osr_qms_5y"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The embedded help topic name.

</td></tr><tr><td>

Page

</td><td>

The UI page this topic corresponds to. Typically, you do not change the page name.**Note:** If you are using the embedded help record to display in the Help Center, as described in [Create Help Center content for configurable workspaces](../../adoption-services/task/create-help-center-content.md), enter the same value in the Name and Page fields, replacing spaces with underscores in the Page field.

</td></tr><tr><td>

Mode

</td><td>

-   **Normal** content appears for any user with the appropriate role who navigates to the page.
-   **Setup** content appears when the page is accessed from a link in Guided Setup.


</td></tr><tr><td>

Role

</td><td>

The role that the topic is written to assist. Users assigned to the role see the content when they navigate to the associated UI page.All roles that contain the role also see the content, unless another topic targeted to their role exists for the same page. For more information, see [Embedded Help roles](../concept/embedded-help-roles.md)

</td></tr><tr><td>

Active

</td><td>

Specifies whether this content displays for the UI page. Clear the check box to prevent the content from being available.

</td></tr><tr><td>

Product

</td><td>

**Enterprise** is the default, and should not be changed.

</td></tr><tr><td>

Qualifier

</td><td>

The qualifier that provides custom embedded help for a common UI page.For example, the `home.do` page is opened for every Homepage module and for many Dashboard modules. Create the qualifier before you enter it into this embedded help record.

</td></tr><tr><td>

Version

</td><td>

The version this topic is appropriate for. If you are editing the content for a custom application or to provide information relevant to your organization business process, select **All**.

</td></tr><tr><td>

Last sync

</td><td>

The last date and time that the CDN was checked for updated content. When a user accesses this UI page, the platform determines whether the last sync date and time are more than 15 days ago. If it is, the CDN is checked for updated content and the date is refreshed.**Note:** The administrator can change the last sync duration in system properties.

</td></tr><tr><td>

Order

</td><td>

The order defaults based on the role, and determines what content to display when the user has an assigned role. For more information, see [Embedded Help roles](../concept/embedded-help-roles.md).

</td></tr><tr><td>

Domain

</td><td>

Specify the domain this content is used for, if applicable.This field appears in the form if the administrator configured the form to display it.

</td></tr></tbody>
</table>4.  In the **Content** field, update the text using the HTML formatting tools as needed.

    If you add a link, enter the full URL to the web page. A good practice is to select **New window \(\_blank\)** as the **Target**.

    **Note:** Do not add images in an embedded help topic. Images are removed from the content section when the record is saved.

    To add an embedded video, see [Embed video content in help topics](embed-video-help-content.md).

5.  To add another line below tables, videos, or related links, click the newline icon \(**⏎**\).

6.  Click **Copy** in the form header.

    The edited topic is saved and the list redisplays. The **ServiceNow Help** check box is cleared in the saved topic.


**Parent Topic:**[Configuring Embedded Help](../concept/configuring-embedded-help.md)

