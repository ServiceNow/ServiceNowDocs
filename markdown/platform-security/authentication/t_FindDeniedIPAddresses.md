---
title: Find denied IP addresses
description: Find Denied IP addresses in the instance's node log files.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [IP range based authentication, Authentication, Access Management]
---

# Find denied IP addresses

Find Denied IP addresses in the instance's node log files.

## Before you begin

Role required: admin.

## About this task

Log entries for blocked IP address appear as follows: `2015-10-21 18:37:43 (175) http-30 WARNING *** WARNING *** Security restricted: Access restricted (xx.xx.xxx.xxx not authorized)`.

**Note:** Denied IP addresses are the viewable instance's node log files, not viewable from the system logs.

## Procedure

1.  Navigate to **All** &gt; **System Logs** &gt; **Utilities** &gt; **Node Log File Browser.**.

2.  Browse the logs by criteria, such as time period and message.

3.  You can also download log files when you know which log you are looking for, by navigating to **System Logs** &gt; **Utilities** &gt; **Node Log File Download**.


