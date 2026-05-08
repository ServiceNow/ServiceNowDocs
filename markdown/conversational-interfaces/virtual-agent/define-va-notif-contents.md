---
title: Define Virtual Agent notification contents
description: Create the content for a Virtual Agent notification delivered in a chat or messaging channel.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Configuring Virtual Agent notifications, Configure, Virtual Agent, Conversational Interfaces]
---

# Define Virtual Agent notification contents

Create the content for a Virtual Agent notification delivered in a chat or messaging channel.

## Before you begin

-   Images for image cards must be 400 pixels wide or larger and must be in .jpg, .png, .bmp, .gif, .ico, or .svg format.
-   If you're upgrading from an earlier release and want ACLs observed for data displayed in record cards and parameter substitutions in chat notifications, set the **com.glide.cs.notification\_record\_access\_check** system property to true. The default value for this system property is false, which means that data is delivered regardless of the user's access level.

    **Note:** This property does not apply to advanced notifications.

-   Role required: virtual\_agent\_admin or admin

## About this task

You can personalize Virtual Agent notifications by using parameter substitution to add dynamic content to the message header and message. When adding dynamic content to your notifications, you specify the variables that identify the record values to be included in the content. You can add dynamic content to the following types of notifications:

-   Record-based notifications - Use the `${<variable_name>}` format in your content to specify a variable that represents a record value from the table used for the notification. For example, if you want to customize the message heading for a notification that uses the Incident table and you want to include the incident **Priority** in the message, use the **Select variable** column to select the variable for incident priority.
-   Event-based notifications - Use the `${event.parm1}` and `${event.parm2}` format to specify event-specific parameters that pass record information in the notification content. To learn more about event parameters and how they work, see Events.
-   Advanced notifications - Modify a script provided for advanced notifications to specify dynamic content from different data sources and identify third-party services, such as URL shortening for streamlining links in the content.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Provider** &gt; **Notifications** and select the notification for which you're defining or updating content.

2.  Do one of the following:

    -   If you're defining new content, navigate to the **Notification Contents** related list, select **New Provider Content**, and go to step 3.
    -   If you're updating content, navigate to the **Notification Contents** related list, select the content to be updated, and go to step 4.
3.  Select the Virtual Agent content type:

    -   **Virtual Agent Content - Chat**: The notification is for chat channels.
    -   **Virtual Agent Content - Messaging**: The notification is for a messaging channel, such as SMS.
    ![The Notification Content page displaying the notification content types that user can choose and create. The available options are Chat Channel, Messaging Channel, and Workspace.](../images/va-notif-content-prompt.png "Notification content")

4.  Provide or update the notification content:

    1.  On the form, fill in the fields for the chat or messaging notification:

<table id="table_chk_33w_znb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the notification content.

</td></tr><tr><td>

Notification

</td><td>

Notification that is associated with the content. This field is populated automatically with the notification that you created.

</td></tr><tr><td>

Type

</td><td>

Notification layout:-   **Simple**: A message-only notification, that contains information for review.
-   **Record card**: A notification that contains information about a particular record in a table.
-   **Image card**: A notification that contains images.


</td></tr><tr><td>

Table

</td><td>

\(For Record Cards\) Table to receive notifications about. This field is populated automatically with the table defined in the notification.

</td></tr><tr><td>

Fields

</td><td>

\(For Record Cards\) Fields to be displayed in the notification. For example, if you select **Comments and Work notes**, the notification includes the comments and work notes that users have added to the record.

</td></tr><tr><td>

Application

</td><td>

Application scope of the notification content.

</td></tr><tr><td>

Active

</td><td>

Option to activate the notification content.

</td></tr><tr><td>

Enable link

</td><td>

\(For Record Cards\) Option to add a link to the record.

</td></tr><tr><td>

Advanced

</td><td>

Option that opens the script editor for entering a script that returns dynamic content for notification heading and message content pulled from multiple data sources.

</td></tr><tr><td>

Script

</td><td>

\(For advanced notification content\) Script that you can edit to specify dynamic content from various data sources, including third-party services \(such as URL shortening\), to be used in the message heading and message content.

</td></tr><tr><td>

Message heading

</td><td>

Text that appears at the top of the message. The default message heading is: `A notification has arrived. You can continue the conversation after viewing the notification.` If you want to create a custom heading with dynamic content, enter the heading text and specify the variables used in the text:

-   For record-based notifications: Expand the **Select variables** column and choose the variables for the record values to be included in the heading. The variables map to records in the table used for the notification. For example: `An incident has been assigned to you with Priority:${priority}`
-   For event-based notifications: Specify the `${event.parm1}` and `${event.parm2}` variables to identify event-specific parameters that pass record information in the notification content.


</td></tr><tr><td>

Message

</td><td>

Content of the message with rich text format.If you want to create a custom message with dynamic content, enter the message text and specify the variables used in the text:

-   For record-based notifications: Expand the **Select variables** column and choose the variables for the record values to be included in the message. The variables map to records in the table used for the notification. For example: `Here's a brief description of your assigned incident:${short_description}`
-   For event-based notifications: Specify the `${event.parm1}` and `${event.parm2}` variables to identify event-specific parameters that pass record information in the notification content.
A notification message defined with rich text format is displayed in bold, italics, link \(url\), and unordered list.![A notification message contains italicized text and a bulleted list. It also includes a hyperlink to a Knowledge article for more information.](../images/rich-text-notif-message.png)

 When users click the URL in the message, they are redirected to the destination as per the portal configuration.

</td></tr><tr><td>

Image Source

</td><td>

\(For Image Cards\) Option for selecting the image to be displayed in the notification:-   **Upload image**: Add the image by uploading.
-   **URL**: Specify the URL for the image.


</td></tr><tr><td>

Image

</td><td>

\(For Image Cards\) Image displayed in the card.-   To add the image, select **Click to add**. From the file finder, choose your image file and select **OK**.
-   To change the image, select **Update**. From the file finder, select the new image file and select **OK**.
-   To remove the image, select **Delete**. The file is immediately deleted.


</td></tr><tr><td>

Image alt text

</td><td>

\(For Image Cards\) Alternative text for the image to be displayed in the card.

</td></tr></tbody>
</table>        **Note:** To create or update the messaging notification details, navigate to the **Delivery Channel** related list and complete the form. For more information, see [Configure a delivery channel for Virtual Agent notification](configure-delivery-channel.md).

    2.  Select **Submit** or **Update**.


## What to do next

-   To configure a delivery channel, see [Configure a delivery channel for Virtual Agent notification](configure-delivery-channel.md).
-   If you're creating an actionable notification, see [Define the actions](define-va-notif-actions.md).

**Parent Topic:**[Configuring Virtual Agent notifications](../concept/configuring-va-notifications.md)

