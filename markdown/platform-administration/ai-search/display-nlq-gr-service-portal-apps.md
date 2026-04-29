---
title: Display NLQ Genius Result answers in Service Portal search applications
description: Configure the system to display search result preview lists for NLQ Genius Result answers in Service Portal search applications.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [NLQ Genius Results, Genius Result configurations in the base system, Genius Results, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Display NLQ Genius Result answers in Service Portal search applications

Configure the system to display search result preview lists for NLQ Genius Result answers in Service Portal search applications.

## Before you begin

You only need to perform this task if you want to use NLQ Genius Results in your Service Portal search applications. If you only use NLQ Genius Results in Next Experience search applications, you don't need to perform this task.

Role required: admin

## About this task

The **glide.service\_portal.ais\_nlq\_enabled** system property determines whether the system displays search result preview lists for NLQ Genius Result answers in Service Portal search applications.

Administrators should set this system property's value to **true** if the NLQ Genius Result configuration is active in any Service Portal application.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Select **New**.

3.  On the System Property form, enter these values.

    |Field|Value|
    |-----|-----|
    |Name|glide.service\_portal.ais\_nlq\_enabled|
    |Type|true \| false|
    |Value|true|

    For details on this system property's values, see the [System properties for NLQ Genius Results](../reference/sys-properties-nlq-gr.md) section.

4.  Press **Submit**.

    The new **glide.service\_portal.ais\_nlq\_enabled** record appears in the System Property \[sys\_properties\] table list view.


**Parent Topic:**[NLQ Genius Results](../concept/genius-result-nlq-ais.md)

