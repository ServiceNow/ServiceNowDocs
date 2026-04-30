---
title: Add Live Feed to a form header
description: Add the Live Feed button in the form header for a table.
locale: en-US
release: xanadu
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure record feeds, Record feeds, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add Live Feed to a form header

Add the **Live Feed** button in the form header for a table.

## Before you begin

Role required: admin

## Procedure

1.  Type `sys_properties.list` in the Application Navigator.

2.  Open the record for **glide.live\_feed.task\_header\_button**.

3.  In the **Value** field, change the value to `both`.

    **Note:** By default, the value is `collaboration` so that the property is supported in the Collaboration \(com.glide.collaboration\) plugin. Changing the value to `both` allows the system property to be supported in Collaboration and Live Feed.

4.  Click **Update**.

5.  Navigate to **System Definition** &gt; **Tables**.

6.  Open the table record.

7.  If the **Live feed** check box does not appear on the form, [configure the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) to add the **Live feed** field.

8.  On the form, select the **Live feed** check box.

9.  Click **Update**.

    Alternatively, you can add **live\_feed=true** to the **Attributes** field in the dictionary entry for the table.


## Result

The **Live Feed** button appears on the overflow menu of the form header.

![The Live Feed button appears on the overflow menu of the form header.](../image/ShowLiveFeed.png)

**Parent Topic:**[Configure record feeds](../concept/c_ConfigureRecordFeeds.md)

