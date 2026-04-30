---
title: Scan software installations with the system scheduler
description: The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds a scheduled job for scanning software installations named SAM License Counters in System Scheduler Scheduled Jobs .
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Determine where software is installed using the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Scan software installations with the system scheduler

The legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin adds a scheduled job for scanning software installations named **SAM License Counters** in **System Scheduler** &gt; **Scheduled Jobs**.

The **SAM License Counters** job occurs at 2:00am \(local time\) every morning. The job queries the Software Installation \[cmdb\_sam\_sw\_install\] table and captures any installations that have not been scanned in the past 7 days.

**Parent Topic:**[Determine where software is installed using the legacy Software Asset Management plugin](c_DeterminWhereSWInstalled.md)

