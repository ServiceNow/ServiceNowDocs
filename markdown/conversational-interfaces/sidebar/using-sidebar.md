---
title: Using Sidebar
description: You can create a Sidebar discussion for a task-based or interaction record from either a configurable workspace or a Next Experience Core UI record page.
locale: en-US
release: xanadu
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2024-11-12"
reading_time_minutes: 3
keywords: [Virtual Agent, using, Sidebar, Polaris, discussions, interaction records]
breadcrumb: [Sidebar, Conversational Interfaces]
---

# Using Sidebar

You can create a Sidebar discussion for a task-based or interaction record from either a configurable workspace or a Next Experience Core UI record page.

## Before you begin

Role required: users with access to the record associated with the Sidebar discussion

**Note:** To avoid incompatibilities with newer features, use Sidebar only on records that have an associated record number.

## Procedure

1.  Navigate to the workspace in which you want to start a Sidebar discussion.

    If you want to initiate a Sidebar discussion in a Customer Service Management \(CSM\) workspace, the CSM plugin for that workspace must be activated.

2.  Select the list icon ![List icon](../image/sidebar-list-icon.png).

3.  From Lists, navigate to and select the record for which you would like to start a Sidebar discussion.

4.  On the Details screen, select **Discuss**.

    -   If the Sidebar discussion exists, the corresponding discussion dialog appears.
    -   If a Sidebar discussion doesn't exist, the Start a Sidebar discussion dialog appears. Fill out the fields and then select **Start discussion**:

        ![Start a Sidebar discussion dialog window.](../image/start-sidebar-discussion.png)

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

</td></tr></tbody>
</table>5.  To return to a previous Sidebar discussion, you can select the Discussion icon ![Discussion icon](../image/sidebar-chat-icon.png) or select one of the tabs in the overflow menu.

6.  After a discussion has been started, you can edit and delete messages.

<table id="choicetable_e3f_lvd_rxb"><thead><tr><th align="left" id="d61130e267">

Option

</th><th align="left" id="d61130e270">

Description

</th></tr></thead><tbody><tr><td id="d61130e276">

**Edit a message**

</td><td>

Select the More options icon ![Discussion icon](../image/ci_more_options_icon.png) next to the message and **Edit message**. The message appears in an Editing window where you can change the text.-   You can only edit messages that you sent.
-   You can only edit one message at a time.
-   If you change the attachment of a message that you sent, both the old and new attachments display.
-   If a message you sent contains a URL, you can delete the message but you can't edit it.


</td></tr><tr><td id="d61130e306">

**Delete a message**

</td><td>

Select the More options icon ![Discussion icon](../image/ci_more_options_icon.png) next to the message and **Delete Message**. A dialog displays asking if you’re sure you want to delete your message. Select **Delete** to delete the message or select **Cancel** to leave the message.-   You can only delete messages that you sent.
-   After you delete a message, a notice with the date and time the message was deleted displays.
-   If you delete a message that mentions someone using @mention, then that @mention is also deleted.
-   You can't undo a deletion, after you delete a message it's gone.


</td></tr></tbody>
</table>7.  To call out a user, enter `@user` \(where `user` is the name of the user\) or `@` to display a list of users and select someone from that list.

    -   Only users who have access to the underlying record display in the list.
    -   The list is divided into users who are currently participating in the discussion \(participants\) and users who aren’t \(non-participants\).
    -   The user is notified that they were mentioned in a Sidebar discussion message. The Sidebar discussions chat icon displays a number indicating unread messages or mentions.

        ![Indication of @mention in sidebar discussions.](../image/sidebar-at-mention-indicator.png)

    -   If the user selects the **Mentions** tab, the messages that mention the user with @user display.

        ![Preview of @mention message in sidebar discussions.](../image/sidebar-at-mention-preview.png)

    -   If the user selects the message preview card, the corresponding message displays with the exact message containing the @mention highlighted.
    -   If Sidebar and Microsoft Teams are integrated, Microsoft Teams users are differentiated from Sidebar users with a Microsoft Teams ![Microsoft teams icon.](../image/teams-icon.png) icon.
8.  When you’re finished, close or exit the discussion.

    -   To close the discussion dialog \(but not exit the discussion\), select ![Close icon.](../image/sidebar-x-icon.png).
    -   To exit the discussion, select **Leave discussion**.

