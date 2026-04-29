---
title: Configure email notifications for watch lists
description: Watch lists \(glide\_list field type\) allow multiple users to subscribe to notifications of a task. You can specify conditions in an email notification to send email notifications to the members when the conditions are met.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add users to a watch list, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Configure email notifications for watch lists

Watch lists \(glide\_list field type\) allow multiple users to subscribe to notifications of a task. You can specify conditions in an email notification to send email notifications to the members when the conditions are met.

## Before you begin

Role required: admin

## About this task

To receive these notifications, users must define an email address in their user record or enter an email address into the watch list email field.

**Important:** Administrators configure email notifications for watch lists.

An advanced configuration using watch lists involves placing two watch lists on a form, one for the general comments on a task and another for work notes or non-public comments. By configuring separate email notifications, separate users on each watch list can be notified about different information.

If users on a watch list are getting more than one email for each update to an incident, it can be because other recipients are replying all to an email notification. Recipients may be receiving email through their email system \(Outlook, Groupwise, and so on\) and through the base system. To stop this duplication, remove the names of other users from the email or the watch list.

## Procedure

1.  Open the notification to configure.

2.  In the Who will receive section, select the icon beside **Users/groups in fields**.

3.  Double-click **Watch list** in the **Available** column to move it to the **Selected** column.

4.  Click **Update**.


-   **[Hide email addresses in a watch list](t_HideEmailAddressesInAWatchList.md)**  
You can remove the email address text entry element from a watch list by modifying the dictionary.
-   **[Configure order buttons on the watch list slushbucket](watchlist-slushbucket-order.md)**  
When you add multiple users to a glide\_list, such as a watch list, the slushbucket does not display the order buttons for the list of selected members. You can set a dictionary attribute to display the order buttons.

**Parent Topic:**[Add users to a watch list](../../../use/using-forms/task/t_UseAWatchList.md)

**Related topics**  


[Configure email notifications for watch lists](t_ConfigNotifications4WatchLists.md)

[Email and SMS notifications](https://www.servicenow.com/docs/access?context=c_EmailNotifications&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

