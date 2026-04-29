---
title: Configure badge counts on navigation bars
description: Configure navigation bar launcher screen tabs and screen tabs to display badge counts. These badge counts indicate how many rows in the Badge Count \[sys\_sg\_badge\_count\] table match a condition that you can configure. For example, how many work orders are waiting for your attention or how many new and unread Sidebar messages have been received.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Navigation bar, Mobile app components, Building mobile apps, Mobile Platform]
---

# Configure badge counts on navigation bars

Configure navigation bar launcher screen tabs and screen tabs to display badge counts. These badge counts indicate how many rows in the Badge Count \[sys\_sg\_badge\_count\] table match a condition that you can configure. For example, how many work orders are waiting for your attention or how many new and unread Sidebar messages have been received.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **sys\_sg\_badge\_count.do**.

2.  On the Badge Count New record form, fill in the fields.

<table id="table_xch_5s4_sbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Application

</td><td>

Application scope.

 To change the application scope, select the globe icon \(![Globe icon](../image/globe-icon.png)\) on the banner and choose the appropriate application scope.

</td></tr><tr><td>

Active

</td><td>

Toggle that sets whether the badge count record is active.

 Inactive badge count records do not appear on the navigation bar launcher screen tabs or screen tabs.

</td></tr><tr><td>

Name

</td><td>

The name of your badge count condition filter.

</td></tr><tr><td>

Location

</td><td>

Location on the mobile screen where badge counts appears. Select **Navigation Tab**.

</td></tr><tr><td>

Mobile Component Table

</td><td>

Table where the navigation tab is located.

 This field auto-populates with **Navigation Tab \[sys\_sg\_navigation\_tab\]** table when you select **Navigation Tab** for **Location**.

</td></tr><tr><td>

Component

</td><td>

The component on which the badge count is displayed. In this case, it is the navigation bar tab on which you want the badge count to appear.

 Select the search icon \(![Magnifying glass search icon](../image/search-icon.png)\) and select a component.

</td></tr><tr><td>

Table

</td><td>

Table to which you want to apply your condition filter.

 Select a table.

</td></tr><tr><td>

Condition

</td><td>

The condition that is used to count the records that match the condition in order to get the badge count. The records that match the condition are displayed as a count on the navigation tab.

</td></tr></tbody>
</table>3.  Select **Submit**.


