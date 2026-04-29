---
title: Stop extraction of unneeded log data in Health Log Analytics
description: If an extracted string of data is not descriptive enough or contains redundant text or information, you can set Health Log Analytics to stop extracting such data from your logs.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, stop extracting, log data, string of data]
breadcrumb: [Log data auto-mapping and mapping, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Stop extraction of unneeded log data in Health Log Analytics

If an extracted string of data is not descriptive enough or contains redundant text or information, you can set Health Log Analytics to stop extracting such data from your logs.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Mapping** &gt; **Excluded values**.

2.  Select **New**.

3.  In the **Value to exclude** field, enter the string that you want Health Log Analytics to stop extracting.

4.  Further specify the values to stop extracting by selecting additional options:

    -   Starts with
    -   Ends with
    -   Contains
    -   Case sensitive
5.  In the **Description** field, add a description of the value.

6.  Select **Submit**.


**Parent Topic:**[Log data auto-mapping and mapping in Health Log Analytics](../concept/hla-data-input-automapping.md)

