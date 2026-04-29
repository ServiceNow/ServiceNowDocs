---
title: Delete a log source in Health Log Analytics
description: Delete a log source with or without its associated log data in Health Log Analytics.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, log source, delete, log data]
breadcrumb: [Additional data input setup tasks, Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Delete a log source in Health Log Analytics

Delete a log source with or without its associated log data in Health Log Analytics.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

When you delete a log source, Health Log Analytics automatically deletes its related log data. You can also delete a source while keeping the log data. The associated data will then be deleted according to the log retention policy. For more information, see [Storage space for log retention in Health Log Analytics](../concept/hla-log-retention-space.md).

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Log Sources**.

2.  Open a source record.

3.  Delete the log source in one of the following ways:

    -   Delete the source and its related data by selecting **Delete**.
    -   Delete the source without its related data by selecting the **Delete without logs** related link.

**Parent Topic:**[Additional data input setup tasks in Health Log Analytics](../concept/hla-data-input-setup-extra.md)

