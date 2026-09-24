---
title: Filter and sort instances
description: Filter and sort the instance list to find specific instances and customize the display format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/filter-and-sort-instances.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Manage Multi-Instance View, Manage, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Filter and sort instances

Filter and sort the instance list to find specific instances and customize the display format.

## Before you begin

Role required: clone\_admin. [Multi-Instance view is enabled.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/setup-multi-instance-view.md)

## Procedure

1.  Filter instances by source using the **Origin Instance** list.

    Use the **Origin Instance** drop-down to view instances by their clone source.

2.  Filter instances by status using the filter icon.

    Use the **filter** icon to view instances by their status.

3.  Sort the instance list by selecting any column header.

    Default sort is Most Recent to show most recently cloned instances first.

4.  Change the instance display format using the view icons.

    -   Select the **grid** icon to view the instance list as a grid.
    -   Select the **list** icon to view the instance list as a list. The list view allows customizing the columns displayed. Select the **gear** icon to configure the columns.

## Result

The Instance List shows each instance with the following information:

|Column|Description|
|------|-----------|
|CHG Number|Change request associated with the clone request|
|Source Instance|Which instance serves as source for the clone operation|
|Target Instance|Which instance is cloned to|
|State|The current status of the clone activity|
|Scheduled Date/Time|The scheduled timestamp of the clone activity|
|Clone start time|The starting timestamp of the clone activity|
|Estimated End Time|The estimated end timestamp for completing the clone activity|
|Duration \(for completed actions\)|The duration taken for the clone activity|

