---
title: Provide access to Live Feed from CMS pages
description: You can provide access to Live Feed from pages built in the Content Management System \(CMS\). For example, allow an end user to access your company feed via the ESS portal.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Provide access to Live Feed from CMS pages

You can provide access to Live Feed from pages built in the Content Management System \(CMS\). For example, allow an end user to access your company feed via the ESS portal.

## Before you begin

Role required: content\_admin or admin

## About this task

The ESS Portal template includes the **Portal - Live page** and **Live Feed** dynamic blocks. To provide access to Live Feed from CMS pages, add the Live Feed dynamic block to a CMS page or include **Portal - Live page** in a site.

## Procedure

1.  Navigate to **Content Management** &gt; **iFrames**.

2.  Click **New**.

3.  Enter the iFrame block details.

<table id="table_xjv_sl1_fr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name such as **Live Frame**.

</td></tr><tr><td>

Frame Name

</td><td>

Enter a frame name, such as **live\_frame**.

</td></tr><tr><td>

URL

</td><td>

https://INSTANCE/live\_feed.do?sysparm\_doctype=true

 where INSTANCE is your instance URL \(example, \[instance name\] .service-now.com\)

</td></tr><tr><td>

Application

</td><td>

Displays scoping information.

</td></tr><tr><td>

Sizing

</td><td>

Select **Fixed Size** and enter height and width pixel dimensions according to the page where you plan to display the feed \(for example, width of 1024 and height of 768\).

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Add the block to a page.


**Parent Topic:**[Administering Live Feed](../concept/c_AdministerLiveFeed.md)

**Related topics**  


[Document feeds](../concept/c_DocumentFeeds.md)

[Record feeds](../concept/c_RecordFeeds.md)

[Live Feed table notifications](../concept/c_SetUpLiveFeedTableNotifications.md)

[Live Feed security and table access](../reference/r_LiveFeedTableAccessRules.md)

[Administering Live Feed](../concept/c_AdministerLiveFeed.md)

[Content Management System](https://www.servicenow.com/docs/access?context=c_ContentManagementSystem&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

