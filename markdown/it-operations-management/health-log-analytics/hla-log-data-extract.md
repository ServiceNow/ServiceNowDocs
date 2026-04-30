---
title: Ensure extraction of specific log data
description: Set Health Log Analytics to extract specified terms from fields and map them to specific components.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [ServiceNow, Health Log Analytics, HLA, extract, log message, mapping, component]
breadcrumb: [Log data auto-mapping and mapping, Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Ensure extraction of specific log data

Set Health Log Analytics to extract specified terms from fields and map them to specific components.

## Before you begin

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **All** &gt; **Health Log Analytics** &gt; **Mapping** &gt; **Extracted values**.

2.  Select **New**.

3.  In the **Value to extract** field, enter the term that you want Health Log Analytics to extract from your logs.

4.  In the **Map to component** field, enter the component that you want the value mapped to.

5.  In the **Property** field, choose a property from the list.

6.  Further specify the value to extract by selecting additional options:

    -   Exact match
    -   Case sensitive
7.  In the **Description** field, add a description of the value.

8.  Select **Submit**.


**Parent Topic:**[Log data auto-mapping and mapping](../concept/hla-data-input-automapping.md)

