---
title: Activity streams
description: An activity stream is a list of entries in records and conversations, such as journal fields, comments, and work notes that display in task records and Sidebar conversations. Activity streams are available Core UI.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Activity streams

An activity stream is a list of entries in records and conversations, such as journal fields, comments, and work notes that display in task records and Sidebar conversations. Activity streams are available Core UI.

The three types of activity streams are as follows:

-   **List activity stream**

    Streams live activity information for all records on the current list. For more information, see [Activity streams in list view](../../using-lists/concept/c_DisplayActivityStreams.md). You can click an item to open the record activity stream without opening the record.

-   **Record activity stream**

    Appears in forms that are configured with the activity formatter . You can customize the activities to include in this type of stream.

    When you follow a record to view it in the Connect Chat interface, the conversation contains the same information as the record activity stream. Comments that are entered in the Connect Chat window update the record activity stream.

-   **Visual Task Board**

    Streams live activity information for all task cards in the current task board. You can click an item in the activity stream to [open the task card](../../visual-task-boards/task/t_EditCardDetails.md#) and view the activity stream of the record.


## Attachments and images

You can add and preview attachments and images in the activity stream by doing the following actions:

-   Paste an image into a journal field and enter the inline text.
-   Click an attachment to preview it. Use the download option to download the attachment locally.
-   Use antivirus scanning to protect against virus infections that can be introduced by file attachments. After being uploaded, the system automatically scans all files for viruses. If a file is infected, you can't view or download the file.

## @ Mentions

Get someone's attention on a record by mentioning them with the @ character in an activity stream.

**Note:** Emails sent for @Mention run against the live\_notification table and are not added to the journal field of the parent table.

Any user can use activity stream mentions in the following places:

-   On a form, in the activity formatter \(Core UI only\).
-   In a list, in the [activity stream](../../using-lists/concept/c_DisplayActivityStreams.md) for a record.
-   On a Visual Task Board card, in the [card details](../../visual-task-boards/task/t_EditCardDetails.md#).
-   In a Connect record conversation.

To mention someone, enter the `@` character in a supported activity stream. Next, select a user from the suggestion list to select any user in the instance. You can see which users have access to the record and, if presence is enabled, who is online. Enter any other text and post to the activity stream. The following example shows an \#Mention on a form.

![@mention in an Activity Stream with the user selector menu open.](../image/activity-stream-mention-form.png "Activity stream mention on a form")

By default, you receive an email notification when someone mentions you. You can disable this behavior by unsubscribing from the Activity Stream @Mention Email notification on your notification preferences.

If Connect is enabled, you can receive additional notifications, depending on whether you follow the record in Connect. When someone mentions you in a record that you do not follow in Connect, you receive whichever Connect notifications you enabled globally, as well as the Activity Stream @Mention Email notification. If you do follow the record in Connect, you only receive notifications according to your notification preferences for the record conversation. In this case, you do not receive the Activity Stream @Mention Email notification.

**Note:** The system creates a record on the notification \[live\_notification\] table each time a user is mentioned. The record stores the information required to generate notifications.

You can filter out emails in the activity stream, for example, auto-generated and correspondence emails, by selecting the ![Activity stream filter icon.](../image/activity-stream-filter.png). Select **Post types** to check or clear the boxes of the types of emails and posts that display in your activity stream.

**Note:** The activity stream displays either a user's first and last name or their user name/user id, depending on the system property **glide.ui.activity.displayname**. It is possible that old entries in the activity stream will display a different user name/user id for the same user, if the value has changed. For more information, see [KB1706641](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1706641).

**Parent Topic:**[Common UI elements](../../common-ui-elements/topic/p_CommonUIElements.md)

