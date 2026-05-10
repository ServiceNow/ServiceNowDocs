---
title: Activity stream in Sidebar
description: If Sidebar is integrated with the activity stream, you can create links to discussions and post discussion messages directly to the related record as an activity stream record.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [sidebar, Virtual Agent, activity stream, Polaris, Core UI, discussion, tile]
breadcrumb: [Exploring Sidebar, Sidebar, Conversational Interfaces]
---

# Activity stream in Sidebar

If Sidebar is integrated with the activity stream, you can create links to discussions and post discussion messages directly to the related record as an activity stream record.

**Note:** Sidebar and discussion tiles are available only with Next Experience and not in Core UI.

When a Sidebar discussion is created, a corresponding Sidebar discussion tile is automatically added to the activity stream. Users who have access to the record can also access the discussion from the activity stream. Sidebar users can post messages from discussions into the activity stream as Sidebar posted messages. These messages can be posted to the activity stream as editable entries that can be added and removed as necessary. For generalized information about activity streams, see [Activity streams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_activity-streams.md).

When you start a Sidebar discussion, a tile corresponding to the discussion is automatically added to the activity stream.

![Sidebar tile, indicated by an arrow, within the activity stream.](../image/sidebar-activity-stream-example-1.png)

![Sidebar tile](../image/sidebar-activity-stream-tile-example.png)

| | |
|---|---|
|1|Sidebar discussion name, type of conversation, date/time discussion started.|
|2|Profile pictures of the participants \(if there are more than 5 participants, then a badge displays the number of additional participants whose profile photos can’t be seen.\)|
|3|Name of user who created the Sidebar discussion.|

The primary record card appears as part of the activity stream and displays the following:

-   Record ID
-   Short description
-   Type
-   State
-   Assigned to
-   Link that opens the record
-   Priority \(for task-based record cards\)

![Primary record card.](../image/sidebar-primary-record-card-example.png)

## Starting a discussion

If you select **Open Discussion**, then the Sidebar panel opens and displays the Sidebar discussions. Customers and non-fulfiller roles don’t have access to the record don’t have access to the conversation tile, similar to work notes.

![Start a discussion.](../image/sidebar-start-discussion.png)

## Posting a message

You can select any message in the Sidebar discussion panel and post it to the activity stream. When you post a message from the Sidebar discussion to the primary records activity stream, the most important information is tied directly to the record. This enables you to access collaborative conversations from a record so that you can add yourself to the discussion and view the conversation history.

![Post a message.](../image/sidebar-post-message.png)

If Sidebar messages posted to the activity stream aren’t appearing, ensure **Sidebar discussion** and **Sidebar posted message** are selected in the activity stream filter.

![Check for Sidebar post types.](../image/sidebar-same-post-type.png)

## Pinning a discussion tile

To pin a discussion tile in the activity stream, select the pushpin icon to pin a discussion tile to the activity stream. Pinning a discussion tile ensures that the discussion always stays at the top of the activity stream.

![Pin a discussion tile.](../image/sidebar-pin-example.png)

## Editing or Deleting a message in Sidebar

If you edit a message in a Sidebar discussion that was already posted to the activity stream, then any changes that you made to the message are reflected in the activity stream.

If you posted a message with an attachment in a Sidebar discussion and the message was already posted to the activity stream, any changes made to the attachment will be reflected in the activity stream. For example, if you post a message with an attachment in a Sidebar discussion and it’s posted to the activity stream and you later delete the attachment and replace it with a different one, the activity stream displays the new attachment.

If you delete a message in a Sidebar discussion after the original message was already posted to the activity stream, then the message is removed from the activity stream.

## Deleting a message from the activity stream

To remove a message from the activity stream, select the **More Actions** menu for each chat bubble within a Sidebar discussion and then select **Remove from activity stream**.

![Remove a message.](../image/sidebar-remove-message.png)

