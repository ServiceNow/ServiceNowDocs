---
title: Viewing Live Feed from records
description: Interact with the record feed in any form that has Live Feed enabled.
locale: en-US
release: australia
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Live Feed to work on records, Using Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Viewing Live Feed from records

Interact with the record feed in any form that has Live Feed enabled.

The record feed appears in a pop-up window. The record feed also appears on the record form's activity formatter if the administrator enables the record feed system property \(`glide.ui.show_live_feed_activity`\).

To access a record feed from the form, do one of the following:

-   Click the **Show Live Feed** button ![Show Live Feed icon](../image/LiveCompanyFeed.png) in the form header. This displays the Live Feed pop-up.
-   Right-click the form header and select **Show Live Feed**. This also displays the Live Feed pop-up.
-   Scroll down to the activity formatter area on the form. Click one of the following tabs:
    -   **Live Feed**: click to show a text box to type in the feed.
    -   **Activity**: click to show the activity summary. The activity filter determines the content in the activity summary.

If the activity formatter or the **Live Feed** and **Activity** tabs are not visible, administrators can do the following:

-   Configure the form layout and add **Activities \(filtered\)** to the form. This adds the activity formatter.
-   Personalize the form layout and add **Activities \(filtered\)** to the form. This adds the activity formatter.
-   Go to **System Definition** &gt; **Tables**, access the table associated with the record, and verify that the live\_feed dictionary attribute is set to true on the form. This adds Live Feed to the activity formatter.
-   Go to **Live Feed** &gt; **Feed Administration** &gt; **Properties** and enable the following property:**Toggle the display of the Live Feed tab in the activity formatter**

