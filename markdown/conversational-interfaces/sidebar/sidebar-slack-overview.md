---
title: Sidebar and Slack
description: Sidebar's integration with Slack enables Sidebar users and Slack users to communicate with each other from their respective platforms.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Sidebar and Slack

Sidebar's integration with Slack enables Sidebar users and Slack users to communicate with each other from their respective platforms.

The base system Sidebar-Slack integration requires at least one participant is an external only user \(a user that doesn't have a corresponding sys\_user record\).

## Authenticating Sidebar users in Slack

A Sidebar user must already have a Slack account to communicate with a Slack user. Slack authenticates each Sidebar user to confirm that they have a Slack account. This authentication verifies that Slack can create a private channel chat that includes the Sidebar user's Slack account. If the Sidebar user has a Slack account but isn’t signed in, they’re prompted to sign in.

## Differentiating between Sidebar and Slack users

To differentiate Sidebar users from Slack users, a Slack icon \(![Slack icon.](../image/slack-icon.png)\) displays next to the Slack users' names. This icon is visible in discussion windows and search results, but does not appear in the activity stream.

| | |
|---|---|
|Discussion window with Slack icon|![Discussion window with Slack icon next to user name External One.](../image/discussion-slack-icon.png)|
|All tab on the Discussion window with Slack icon|![Discussion window with the All tab selected and Slack icon highlighted.](../image/all-tab-slack-icon.png)|
|Discussion window with Slack icon next to search results|![Start a Sidebar discussion window with Slack icon highlighted next to two search results.](../image/search-slack-icon.png)|
|Discussion info window with Slack icon|![Discussion info window, with Slack icon highlighted next to username External One.](../image/discussion-info-slack-icon.png)|

## Adding users to a discussion

Sidebar users can enter the partial or full name of a user that they want to add to the discussion. If the user exists in the system, the user's name appears and can be selected to be added to the discussion. Users who have access to Slack but not ServiceNow can be identified by the Slack logo in their avatar image. Slack users can add participants to the discussion by adding them to the group chat on Slack. Doing this automatically adds those users to the discussion in Sidebar.

**Note:** A maximum of 250 users can be added to a Slack private channel.

## Synchronizing Sidebar and Slack users

If Sidebar and Slack are integrated, a job runs every 30 minutes to synchronize the Sidebar and Slack users. If a Slack user's email matches a Sidebar user's email, the Slack user is mapped to the Sidebar user.

## Validating messages

Messages that are sent from Slack to Sidebar are verified using Slack's signing secret.

## Sending messages between Sidebar and Slack

After Sidebar and Slack are integrated, you can send these types of messages between the two applications:

-   Messages with plain text
-   Messages with images
-   Messages with emojis
-   Messages with URLs
-   Messages with attachments
-   Messages with links to ServiceNow records

Replies made to messages in Slack are displayed as replies to the corresponding message\(s\) in Sidebar.

## Removing users from a discussion

Sidebar users can remove a Slack user from a Sidebar discussion. When a Slack user is removed from a discussion, Sidebar and Slack users see a message that the user has been removed from the discussion. After a Slack user is removed from the discussion, they can still access the group chat on Slack and view past messages, but they can no longer participate in the discussion. If a Slack user leaves a discussion on their own, both Sidebar and Slack users see a message that the Slack user has left the discussion.

## Message history

If the admin enables Slack group chats for a user, the message history of any Sidebar discussions that the user is already participating in aren't preloaded in the Slack group chat. In the Slack group chat, the user will only receive messages that are sent after the admin enables them to receive Slack group chats.

## ServiceNow's access to Slack messages

ServiceNow's access to Slack group chats and messages is restricted to the ones generated as part of the Sidebar and Slack integration.

## Synchronizing of participants

The discussion participants aren’t synchronized if the integration between Sidebar and Slack is changed multiple times.

![What happens if you turn the Sidebar-Slack configuration off and on.](../image/sidebar-slack-on-off.png "Synchronizing example")

## Domain separation with Sidebar and Slack integration

If Sidebar is integrated with Slack, domain separation is not supported on the Slack instance. As a result, the **Set up** button for Slack is inactive on the Settings page. For example, if you’ve configured two domains on ServiceNow but use only one Microsoft Teams instance, you can't partition the Microsoft Teams instance to have part of it point to one domain and the other part to another domain.

