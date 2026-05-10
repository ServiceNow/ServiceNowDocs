---
title: Disable a record feed
description: You can disable Live Feed functionality from the form of any table.
locale: en-US
release: australia
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Document feeds, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Disable a record feed

You can disable Live Feed functionality from the form of any table.

## Before you begin

Role required: personalize\_dictionary or admin

## Procedure

1.  Navigate to **System Definition** &gt; **Dictionary**.

2.  Open the dictionary entry for the table.

3.  Add `live_feed=false` in the **Attributes** field.

4.  Click **Update**.

    **Note:** If the Collaboration feature is activated, you can remove the show Live Feed icon from all form headers. Set the **glide.live\_feed.task\_header\_button** property to **collaboration**.


**Parent Topic:**[Document feeds](../concept/c_DocumentFeeds.md)

**Parent Topic:**[Record feeds](../concept/c_RecordFeeds.md)

**Related topics**  


[Add a Live Feed UI action on a table](t_AddALiveFeedUIActionOnATable.md)

[Configure document feeds](t_ConfigureDocumentFeeds.md)

[Security configuration for document feeds](../concept/c_ConfigureFeedSecurity.md)

[Disable a document feed](t_DisableADocumentFeed.md)

[Business rule installed with Live Feed Document](../reference/r_InstalledComponents.md)

