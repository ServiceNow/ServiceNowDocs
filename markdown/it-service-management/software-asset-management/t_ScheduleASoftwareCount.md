---
title: Schedule a software count for the legacy Software Asset Management plugin
description: How to schedule a software count for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Software license reconciliation counters for the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Schedule a software count for the legacy Software Asset Management plugin

How to schedule a software count for the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## About this task

The SAM License Counters scheduled job scans your instance for software installations. The SAM License Counters job occurs at 2:00am local time every morning. The job queries the Software Installation \[`cmdb_sam_sw_install`\] table and captures any installations that have not been scanned in the past 7 days. The job runs a join query on hardware that has been scanned within the last day and software installations that have not been scanned in the last 7 days.

The SAM License Counters scheduled job runs all software counters at once.

To refresh the cache manually for a specific counter:

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Reconciliation** &gt; **Software Counters**.

2.  Select a counter whose cache you want to refresh.

3.  Right-click in the header bar of the Software Counter record and select **Rebuild SAM Cache** from the context menu.

    ![SAM rebuild cache](../image/SAMRebuildCache.png "SAM rebuild cache")


**Parent Topic:**[Software license reconciliation counters for the legacy Software Asset Management plugin](../concept/c_UseCountersSWLicenseReconcil.md)

