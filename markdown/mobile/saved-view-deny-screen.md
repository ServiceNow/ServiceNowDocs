---
title: Make saved views unavailable on specific pages
description: You might want to remove the option for users to save specific views and screens for security or privacy reasons.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Bookmark screens &amp; web pages, Configuring the Mobile Platform, Mobile Platform]
---

# Make saved views unavailable on specific pages

You might want to remove the option for users to save specific views and screens for security or privacy reasons.

## Before you begin

Role required: admin

## Procedure

1.  In the web-based UI, enter `sys_sg_favorite_deny_list.list` in the filter navigator to open the list of search configurations.

2.  Select **New** in the Saved Items Deny List form.

3.  In the **Source Table** field, select `Screen [sys_sg_screen]`.

4.  Select the reference lookup icon \(![Reference lookup icon.](../image/reference-lookup-icon.png)\) from the **Source** field.

5.  In the **Select the document** screen, select the reference lookup icon \(![Reference lookup icon.](../image/reference-lookup-icon.png)\) within the **Document** field.

6.  Select the screen on which you want the saved views icon not to display.

7.  Select **OK**.

8.  Make sure that the **Active** option is selected.

9.  Select **Submit**.


## Result

The specified screen no longer displays the saved views icon in the screen header.

