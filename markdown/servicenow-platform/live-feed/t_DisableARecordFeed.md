---
title: Disable a record feed
description: You can disable Live Feed functionality from the form of any table.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/live-feed/t\_DisableARecordFeed.html
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


**Parent Topic:**[Document feeds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/live-feed/c_DocumentFeeds.md)

**Parent Topic:**[Record feeds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/live-feed/c_RecordFeeds.md)

**Related topics**  


[Add a Live Feed UI action on a table]()

[Configure document feeds]()

[Security configuration for document feeds]()

[Disable a document feed]()

[Business rule installed with Live Feed Document]()

