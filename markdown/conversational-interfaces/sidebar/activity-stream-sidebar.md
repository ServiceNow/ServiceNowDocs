---
title: Activity stream in Sidebar
description: Create links to Sidebar discussions in the activity stream and post discussion messages directly to the related record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/conversational-interfaces/sidebar/activity-stream-sidebar.html
release: australia
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [sidebar, Virtual Agent, activity stream, Polaris, Core UI, discussion, tile]
breadcrumb: [Exploring Sidebar, Sidebar, Conversational Interfaces]
---

# Activity stream in Sidebar

Create links to Sidebar discussions in the activity stream and post discussion messages directly to the related record.

**Note:** Sidebar and discussion tiles are available only with Next Experience and not in Core UI.

When someone creates a Sidebar discussion, the system adds a corresponding Sidebar discussion tile to the activity stream. Users who have access to the record can also access the discussion from the activity stream. Sidebar users can post messages from discussions into the activity stream as Sidebar posted messages. You can add and remove these posted messages as necessary. For general information about activity streams, see [Activity streams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_activity-streams.md).

\[Omitted image "sidebar-activity-stream-example-1.png"\] Alt text: Sidebar tile, indicated by an arrow, within the activity stream.

\[Omitted image "sidebar-activity-stream-tile-example.png"\] Alt text: Sidebar tile

| | |
|---|---|
|1|Sidebar discussion name, type of conversation, and date and time the discussion started.|
|2|Profile pictures of the participants. If there are more than five participants, a badge displays the number of additional participants whose profile pictures aren’t shown.|
|3|Name of the user who created the Sidebar discussion.|

The primary record card appears as part of the activity stream and displays the following:

-   Record ID
-   Short description
-   Type
-   State
-   Assigned to
-   Link that opens the record
-   Priority \(for task-based record cards\)

\[Omitted image "sidebar-primary-record-card-example.png"\] Alt text: Primary record card.

## Starting a discussion

If you select **Open Discussion**, then the Sidebar panel opens and displays the Sidebar discussions. Customers and non-fulfiller roles don’t have access to the record, so they don’t see the conversation tile, similar to work notes.

\[Omitted image "sidebar-start-discussion.png"\] Alt text: Start a discussion.

## Posting a message

You can select any message in the Sidebar discussion panel and post it to the activity stream. When you post a message from the Sidebar discussion to the primary record’s activity stream, the most important information is tied directly to the record. You can then open the conversation from the record, add yourself to the discussion, and view the conversation history.

\[Omitted image "sidebar-post-message.png"\] Alt text: Post a message.

If Sidebar messages posted to the activity stream aren’t appearing, ensure **Sidebar discussion** and **Sidebar posted message** are selected in the activity stream filter.

\[Omitted image "sidebar-same-post-type.png"\] Alt text: Check for Sidebar post types.

## Pinning a discussion tile

To pin a discussion tile, select the pushpin icon. A pinned discussion tile stays at the top of the activity stream.

\[Omitted image "sidebar-pin-example.png"\] Alt text: Pin a discussion tile.

## Editing or deleting a message in Sidebar

If you edit a message in a Sidebar discussion that was already posted to the activity stream, then any changes that you made to the message are reflected in the activity stream.

If you posted a message with an attachment in a Sidebar discussion and the message was already posted to the activity stream, any changes made to the attachment are reflected in the activity stream. For example, if you post a message with an attachment in a Sidebar discussion and it’s posted to the activity stream and you later delete the attachment and replace it with a different one, the activity stream displays the new attachment.

If you delete a message in a Sidebar discussion after the original message was already posted to the activity stream, then the system removes the message from the activity stream.

## Deleting a message from the activity stream

To remove a message from the activity stream, select the **More Actions** menu for each chat bubble within a Sidebar discussion and then select **Remove from activity stream**.

\[Omitted image "sidebar-remove-message.png"\] Alt text: Remove a message.

