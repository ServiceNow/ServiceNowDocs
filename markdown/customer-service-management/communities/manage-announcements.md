---
title: Make an announcement to community members
description: Global announcements appear in the banner and broadcast messages to all community members. Forum announcements appear in the Announcements section on the forum page. You can also send the announcement by email.
locale: en-US
release: yokohama
product: Communities
classification: communities
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Community Service Portal, Configure a community, Communities, Customer Service Management]
---

# Make an announcement to community members

Global announcements appear in the banner and broadcast messages to all community members. Forum announcements appear in the Announcements section on the forum page. You can also send the announcement by email.

## Before you begin

Role required:

-   sn\_communities.admin can manage Global announcements and Forum announcements
-   sn\_communities.forum\_admin can manage Forum announcements for own forums only. The announcement appears only in the forum that the admin owns.

## About this task

This example shows how a community user experiences announcements and how you can configure the appearance and operation of announcements.

![Community announcements page displaying global and forum announcements with options to hide or dismiss the announcements.](../images/announcements_annotated.png "Community User Experience Announcements")

## Procedure

1.  Navigate to **All** &gt; **Community** &gt; **Administration** &gt; **Global Announcements** or **Forum Announcements**, click **New**, and then fill in the form.

<table id="table_zzj_cp4_gbb"><tbody><tr><td>

Announcement type

</td><td>

Read-only. Set to **Global Announcement** or **Forum Announcement**, depending on what you are working on.

</td></tr><tr><td>

Active

</td><td>

Select the check box to publish the announcement to members.

 Clear the check box to cancel the announcement.

</td></tr><tr><td>

Title

</td><td>

Display title of the announcement.-   The text appears above the **Summary** text.
-   In email, the text is the subject of the message.


</td></tr><tr><td>

Summary

</td><td>

Content of the announcement. -   The text appears below the **Title** text.
-   In email, the text is the body of the message.


</td></tr><tr><td>

From / To

</td><td>

-   **From**: Date and time that the announcement should appear.
-   **To**: Date and time that the announcement should no longer appear.


</td></tr><tr><td>

Send email notification

</td><td>

Select the check box to send the announcement to members as an email message in addition to broadcasting the announcement.

</td></tr><tr><td>

Display first

</td><td>

Select the check box to display the announcement as the first announcement in the list.

</td></tr><tr><td>

Public

</td><td>

Select the check box to enable forum members that are not logged in to view the announcement.

</td></tr><tr><td>

Portals

</td><td>

Portals that display the announcement. Default: **Community**.

 **Note:** If no value is specified, the announcement does not appear in any portal.

</td></tr><tr><td>

Click target

</td><td>

The **Click target** setting creates a link for the announcement. -   **None**: No link.
-   **Page**: Opens a Service Portal page in the current browser tab.
-   **URL in current browser tab**: Opens the specified URL in the current browser tab.
-   **URL in new browser tab**: Opens the specified URL in a new browser tab.


</td></tr><tr><td>

Details URL

</td><td>

If you select a URL option for **Click target**, then enter the URL in the **Details URL** field.

</td></tr><tr><td>

Details link text

</td><td>

Appears only if **Click target** is not **None**. -   To display a link under the **Summary** text, enter the text of the link in the **Details link text** field.
-   To use the **Title** text of the announcement as the link, leave **Details link text** blank.


</td></tr><tr><td>

Forums

</td><td>

This setting appears for Forum announcements only. Slushbucket of forums that you are admin for. Move a forum into the **Selected** list to display the announcement on the forum.

</td></tr><tr><td>

Dismiss options

</td><td>

This setting appears for Global announcements only. Determines how the user can dismiss the announcement.

</td></tr></tbody>
</table>
## What to do next

-   To update an announcement, update any setting as needed and then click **Update**. If you specified **Send email notification**, then you are prompted to send the updated email message.
-   To cancel an announcement, clear the **Active** check box.

**Parent Topic:**[Community Service Portal](../concept/community-service-portal.md)

