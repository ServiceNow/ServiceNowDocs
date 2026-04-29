---
title: Sidebar and Microsoft Teams
description: Sidebar's integration with Microsoft Teams enables Sidebar users and Microsoft Teams users to communicate with each other from their respective platforms.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Virtual Agent, Microsoft Teams, MSTeams, Sidebar, integration, monetization]
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Sidebar and Microsoft Teams

Sidebar's integration with Microsoft Teams enables Sidebar users and Microsoft Teams users to communicate with each other from their respective platforms.

## Monetization by Microsoft

The Sidebar-Microsoft Teams integration is available as a standard ServiceNow feature, however Microsoft intends to monetize any use of their Microsoft Teams API based on a rate charge per message:

-   The rate charge applies each time the Microsoft Teams API is called. Charges apply for messages sent from your ServiceNow instance to Microsoft Teams and vice versa.
-   The rate charge doesn’t apply to "means to an end" actions such as searching for or adding users to a Microsoft Teams group chat, user presence, or reactions.
-   To minimize the number of API calls to Microsoft Teams, the base system Sidebar-Microsoft Teams integration requires at least one participant is an external only user \(a user that doesn't have a corresponding sys\_user record\). If you want to modify this base system behavior, see [Manage Microsoft Teams permissions](../task/manage-teams-permissions.md) for information on how to add the internal user or group that the internal user is part of.

Microsoft bills ServiceNow customers directly via their Microsoft Azure account. For more information, see [Licensing and payment requirements for the Microsoft Teams API](https://learn.microsoft.com/en-us/graph/teams-licenses).

## Authenticating Sidebar users in Microsoft Teams

A Sidebar user must already have a Microsoft Teams account to communicate with a Microsoft Teams user. Microsoft Teams authenticates each Sidebar user to confirm that they have a Microsoft Teams account. This authentication ensures that Microsoft Teams can create a group chat that includes the Sidebar user's Microsoft Teams account. If the Sidebar user has a Microsoft Teams account but isn’t signed in, they’re prompted to sign in.

## Differentiating between Sidebar and Microsoft Teams users

To differentiate Sidebar users from Microsoft Teams users, a Microsoft Teams icon ![Microsoft Teams icon.](../image/teams-icon.png) displays next to the Microsoft Teams users' names. This icon is visible in discussion windows and search results, but doesn’t appear in the activity stream.

| | |
|---|---|
|Discussion window with Microsoft Teams icon|![Discussion window with Microsoft Teams icon highlighted next to username External One.](../image/discussion-teams-icon.png)|
|All tab on the Discussion window with Microsoft Teams icon|![Discussion window with the All tab selected, and Microsoft Teams icon highlighted.](../image/all-tab-teams-icon.png)|
|Discussion window with Microsoft Teams icon next to search results|![Start a sidebar discussion window with Microsoft Teams icon highlighted next to two search results.](../image/search-teams-icon.png)|
|Discussion info window with Microsoft Teams icon|![Discussion info window, with Microsoft Teams icon highlighted next to username External One.](../image/discussion-info-teams-icon.png)|

## Adding users to a discussion

Sidebar users can enter the partial or full name of a user that they want to add to the discussion. If the user exists in the system, the user's name appears and can be selected to be added to the discussion. Users who have access to Microsoft Teams but not ServiceNow can be identified by the Microsoft Teams logo in their avatar image. Microsoft Teams users can add participants to the discussion by adding them to the group chat on Microsoft Teams. Doing this automatically adds those users to the discussion in Sidebar.

**Note:** A maximum of 250 users can be added to a Microsoft Teams group chat.

## Sending messages between Sidebar and Microsoft Teams

After Sidebar and Microsoft Teams are integrated, you can send these types of messages between the two applications:

-   Messages with plain text
-   Messages with emojis
-   Messages with URLs
-   Messages with attachments

Actions performed in the Sidebar discussion are reflected in Microsoft Teams and actions performed in Microsoft Teams are reflected in Sidebar. If you reply to a message in a Microsoft Teams group chat, the message displays in Sidebar however, it doesn't display as a reply to the original message.

Errors messages appear in these situations:

-   If Sidebar is unable to deliver a message to a Microsoft Teams user, the message "Not delivered in Teams" displays. Depending on how error message notifications in Sidebar are configured, the message displays to just the Sidebar user who sent the message or to all Sidebar users in the discussion.

    ![Message window displaying Not delivered in Teams message](../image/sidebar-not-delivered-message.png)

-   If you delete a message that you previously sent from Sidebar to Microsoft Teams but Microsoft Teams is unable to delete the message, then the message "Not deleted in Teams" displays.

    ![Message window displaying Not deleted in Teams message](../image/sidebar-not-deleted-message.png)

-   If you edit a message that you previously sent from Sidebar to Microsoft Teams but Microsoft Teams is unable to update the message, then the message "Not updated in Teams" displays.

    ![Message window displaying Not updated in Teams message](../image/sidebar-not-updated-message.png)


Replies made to messages in Microsoft Teams are displayed as replies to the corresponding message\(s\) in Sidebar.

## Removing users from a discussion

Sidebar users can remove a Microsoft Teams user from a Sidebar discussion. When a Microsoft Teams user is removed from a discussion, Sidebar and Microsoft Teams users see a message that the user has been removed from the discussion. After a Microsoft Teams user is removed from the discussion, that user can still access the group chat on Microsoft Teams and view older messages, but they can no longer participate in the discussion. If a Microsoft Teams user leaves a discussion on their own, both Sidebar and Microsoft Teams users see a message that the Microsoft Teams user has left the discussion.

## Message history

If the admin enables Microsoft Teams group chats for a user, the message history of any Sidebar discussions that the user is already participating in aren't preloaded in the Microsoft Teams group chat. In the Microsoft Teams group chat, the user will only receive messages that are sent after the admin enables them to receive Microsoft Teams group chats.

## ServiceNow's access to Microsoft Teams messages

ServiceNow's access to Microsoft Teams group chats and messages is restricted to the ones generated as part of the Sidebar and Microsoft Teams integration.

## Synchronizing of participants

The discussion participants aren’t synchronized if the integration between Sidebar and Microsoft Teams is changed multiple times.

Synchronizing example:

1.  A Sidebar group has User A, B, and C, while a Microsoft Teams user has User 1, 2, and 3.
2.  When an admin activates the Microsoft Teams integration, users A, B, and C can communicate with users 1, 2, and 3.
3.  An admin deactivates the integration, and users are removed or added on both sides \(User A is removed from Sidebar, and User 4 is added to Microsoft Teams\).
4.  When the admin reactivates the Microsoft Teams integration, the discussion groups do not update. Instead, they remain as they were before the integration was deactivated: the Sidebar group has User A, B, and C, while a Microsoft Teams user has User 1, 2, and 3.

## Domain separation with Sidebar-Microsoft Teams integration

If Sidebar is integrated with Microsoft Teams, domain separation is not supported on the Microsoft Teams instance. As a result, the **Set up** button for Microsoft Teams is disabled on the Settings page. For example, if you’ve configured two domains on ServiceNow but use only one Microsoft Teams instance, you can't partition the Microsoft Teams instance to have part of it point to one domain and the other part to another domain.

