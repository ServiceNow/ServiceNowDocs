---
title: Create a Sidebar discussion for a record
description: Collaborate with others by creating a Sidebar discussion for a task or interaction record. These discussions can be created from a Next Experience page or Core UI record page.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Sidebar, Sidebar, Conversational Interfaces]
---

# Create a Sidebar discussion for a record

Collaborate with others by creating a Sidebar discussion for a task or interaction record. These discussions can be created from a Next Experience page or Core UI record page.

## Before you begin

Role required: users with access to the record associated with the Sidebar discussion

**Note:** To avoid incompatibilities with newer features, use Sidebar only on records that have an associated record number.

## Procedure

1.  Start a Sidebar discussion from a Next Experience page or a Core UI record:

<table id="table_bgq_wvw_n2c"><thead><tr><th>

Next Experience page

</th><th>

Core UI record

</th></tr></thead><tbody><tr><td>

1.  From the top menu, select the Sidebar discussion icon \(![Sidebar icon.](../image/sidebar-chat-icon.png)\) to display the Sidebar discussions window.

![Sidebar discussions menu.](../image/sidebar-discussions-menu-example.png)

2.  To display an existing Sidebar discussion, select it on the Sidebar discussion menu.
3.  Start a new Sidebar discussion by selecting **New discussion** to display the Start a Sidebar discussion window.

![Blank Sidebar discussion window.](../image/sidebar-blank-discussion-window.png)

4.  Select **Link a record** and enter the task or incident number in the Record number field.


</td><td>

1.  In the navigation filter, enter the type of record \(interaction or task\) for which you want to create a Sidebar discussion.
2.  Select **All** to display all records for the type you entered.
3.  On the Incidents or Tasks screen, select the record you want to create the Sidebar discussion for.
4.  On the Incident or Task screen, select **Discuss** to display the Start a Sidebar discussion window:![Start a Sidebar discussion window.](../image/sidebar-another-discussion-window.png)


</td></tr></tbody>
</table>2.  Fill in the fields on the Sidebar discussion window:

<table id="table_kzq_h41_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record number

</td><td>

Record number associated with the Sidebar discussion.

</td></tr><tr><td>

Subject

</td><td>

This field is pre-populated with the record's short description. If the Subject starts with a number in parentheses, that number indicates what number this discussion is for the record. For example, if the subject line has "\(2\) Email issue," the "2" indicates the second discussion for the email issue record. You can edit or add to the Subject field.

</td></tr><tr><td>

Add participants

</td><td>

Select the user or user group to include in the discussion. If an assignment group was entered for this case/interaction/incident, this field is pre-populated with its members. -   If you select individual users, only those users with access to the record can be added as participants.
-   If you select a user group, only those users within the group who have access to the record are added as participants.
For more information, see [Configuring Sidebar member query](configure-sidebar-member-query.md).

</td></tr><tr><td>

Include a brief message for participants

</td><td>

Enter a short message for the participants of the Sidebar discussion.

</td></tr><tr><td>

Private discussion

</td><td>

Select **Private discussion** to limit Sidebar discussion access to only the agent and other discussion participants. These discussions are marked "private" and can't be converted to not private. Participants can invite others to join the private discussion, provided the new participants have access to the record. Private discussions aren’t visible to non-participants in search results.

</td></tr></tbody>
</table>3.  Select one of the following:

    -   Start private discussion - start a private Sidebar discussion.
    -   Start discussion - start a Sidebar discussion.
    -   Cancel - cancel the discussion.
4.  Once you start a discussion, you can edit and delete messages.

<table id="table_b2r_3jb_p2c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Edit a message

</td><td>

Select the More options icon ![More options icon.](../image/ci_more_options_icon.png) next to the message and **Edit message**. The message appears in an Editing window where you can change the text.-   You can only edit messages that you sent.
-   You can only edit one message at a time.
-   If you change the attachment of a message that you sent, both the old and new attachments display.
-   If a message you sent contains a URL, you can delete the message but you can't edit it.


</td></tr><tr><td>

Delete a message

</td><td>

Select the More options icon ![More options icon.](../image/ci_more_options_icon.png) next to the message and **Delete Message**. A dialog displays asking if you’re sure you want to delete your message. Select **Delete** to delete the message or select **Cancel** to leave the message.-   You can only delete messages that you sent.
-   After you delete a message, a notice with the date and time the message was deleted displays.
-   If you delete a message that mentions someone using @mention, then that @mention is also deleted.
-   You can't undo a deletion, after you delete a message it's gone.


</td></tr></tbody>
</table>5.  To mention a user, enter `@user` \(where `user` is the name of the user\) or `@` to display a list of users and select someone from that list.

    -   Only users who have access to the underlying record display in the list.
    -   The list is divided into users who are currently participating in the discussion \(participants\) and users who aren’t \(non-participants\).
    -   The user is notified that they were mentioned in a Sidebar discussion message. The Sidebar discussions chat icon displays a number indicating unread messages or mentions.

        ![Indication of @mention in sidebar discussions.](../image/sidebar-at-mention-indicator.png)

    -   If the user selects the **Mentions** tab, the messages that mention the user with @user display.

        ![Preview of @mention message in sidebar discussions.](../image/sidebar-at-mention-preview.png)

    -   If the user selects the message preview card, the corresponding message displays with the exact message containing the @mention highlighted.
6.  An email notification is sent to the user if:

    -   the user doesn't read the messages within 24 hours. The email is sent as a reminder to view the messages and resume the discussion. See [Sidebar requester mapping](sidebar-requester-mapping.md) for more information about requester mapping for email notifications.
    -   if a requester is added to an existing discussion.
7.  To close the discussion dialog \(but not exit the discussion\), select the Close icon ![Close icon.](../image/sidebar-x-icon.png).


