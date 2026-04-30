---
title: Configure My Requests to track open records
description: Specify which records that you want your users to see under My Requests so that they can track their work assignments. For example, you can add a filter to display records that are opened by the user from the Problem table. By default, the app displays records that are opened by the user from the Incident and Requested Item tables.
locale: en-US
release: yokohama
product: Now Mobile - Employee Experience
classification: now-mobile-employee-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure, Now Mobile app, Unified Employee Experience, Employee Service Management]
---

# Configure My Requests to track open records

Specify which records that you want your users to see under **My Requests** so that they can track their work assignments. For example, you can add a filter to display records that are opened by the user from the Problem table. By default, the app displays records that are opened by the user from the Incident and Requested Item tables.

## Before you begin

Role required: admin

## About this task

Demonstrates configuring service catalogs, knowledge bases, and My Requests in the Now Mobile App.

## Procedure

1.  Navigate to **All** &gt; **Now Mobile App** &gt; **My Request Filters**.

2.  In the My Request Filters \[request\_filter\] table, create a filter to display records from a specific table:

    1.  Click **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Title|Name for the filter.|
        |Table|Table that extends the Task table. The app displays records from this table under **My Requests**.|
        |Filter|Filter for the table. For example, you can set the filter to **\[Opened by\]** **\[is \(dynamic\)\]** **\[Me\]** to enable users to view their own requests.|
        |Active|Option that you can select to make the filter active.|
        |Applies to|Option that you can select to apply to **Mobile** apps.|

    3.  Click **Submit**.

    Records from the defined filter are displayed in the app under **My Requests** in the **For Me** tab.


