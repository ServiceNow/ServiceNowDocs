---
title: Configure blog publish schedule
description: Configure the publishing interval to ensure blogs are published closer to the scheduled time.
locale: en-US
release: australia
product: Communities
classification: communities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Community content types, Configuring communities, Communities, Customer Service Management]
---

# Configure blog publish schedule

Configure the publishing interval to ensure blogs are published closer to the scheduled time.

## Before you begin

Role required: system\_scheduler\_admin

**Note:** `system_scheduler_admin` is a high‑privilege role which grants broader permissions. Assign this role only after reviewing the permissions and confirming necessity.

## About this task

The default interval for publishing blogs is 30 minutes. You can configure a shorter time so that the blog is published approximately around the scheduled time.

## Procedure

1.  Navigate to **All** &gt; **System definition** &gt; **Scheduled Jobs**.

2.  Search and select `Publish scheduled content` in the name column.

3.  Set the required time in the **Repeat interval** field.

    Keep the time short \(for example, 5 minutes\) to reduce the delay in publishing blogs from the scheduled time.

4.  Click **Update**.


**Parent Topic:**[Community content types](../concept/c_communities-content-types.md)

