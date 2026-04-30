---
title: Create internationalized embedded help
description: Translate provided English embedded help content into other languages or create custom embedded help content in the language of your choice.
locale: en-US
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Embedded Help internationalization, Embedded Help planning, Configuring Embedded Help, Embedded Help, In-product help, Adoption services, Configure user experiences]
---

# Create internationalized embedded help

Translate provided English embedded help content into other languages or create custom embedded help content in the language of your choice.

## Before you begin

Role required: embedded\_help\_admin or admin

## About this task

All embedded help content records are in English by default. To create a non-English embedded help content record, there must first be an English content record in the Embedded Help \[sys\_embedded\_help\_content\] table. The English embedded help content record is parent to all other language embedded help content records. Once you create a non-English embedded help content record, it resides in the Translated Texts \[sys\_translated\_text\] table.

To translate provided English content into another language, create a copy of the English content record and save the edited, non-English, copy record. The new record is saved to the Translated Texts \[sys\_translated\_text\] table. Refer to [Add custom embedded help from a copy](add-custom-help-copy.md) to translate available embedded help content.

To create a non-English custom embedded help content record, your working instance must be configured to the same language you intend to write in. You create custom non-English embedded help content when English embedded help content is not available to copy.

After creating a non-English embedded help content record, you must create the same content record in English and store it in the Embedded Help \[sys\_embedded\_help\_content\] table. The English embedded help content record is parent to all other languages.

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

The UI page this topic corresponds to. Typically, you do not change the page name.

</td></tr><tr><td>

Modifier

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


**Parent Topic:**[Embedded Help internationalization](../concept/embedded-help-internationalization.md)

