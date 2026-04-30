---
title: Update more information cards
description: Configure and update the More Information cards in the side panel.
locale: en-US
release: xanadu
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Success Dashboard indicators KPIs, ITSM Success Dashboard Admin console, Configuring ITSM Success Dashboard indicators, ITSM Success Dashboard indicators, IT Service Management]
---

# Update more information cards

Configure and update the **More Information cards** in the side panel.

## Before you begin

Role required: sn\_sd.success\_dashboard\_admin

## Procedure

1.  Navigate to **All &gt; sn\_sd\_m2m\_indicator\_context\_information.list**.

2.  Find the context information record in the table based on the Primary Indicator or the Contributing Indicator Registry that the card is associated with.

3.  Select the **Indicator context information** field to open the context information record.

4.  Modify the content of the record based on your requirement.

5.  Select **Save**.


## What to do next

Associate the new context information card with an indicator. To associate a new context information card to a primary or contributing indicator, perform the following steps:

1.  Navigate to **All &gt;** &gt; **sn\_sd\_indicator\_context\_information.list**.
2.  Select **New**.
3.  On the form, fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Icon|Name of the icon that appears beside the tagline. You can select from any of the icons available in the gallery.|
    |Tagline|Short label of the card.|
    |Heading|Short heading that provides context on what the card explains.|
    |Content|HTML text that describes the card.|
    |Footer|Footer of the card.|

4.  Select **Submit**.
5.  Navigate to **All &gt; sn\_sd\_m2m\_indicator\_context\_information.list**.
6.  Select **New**
7.  On the form, fill in the following fields:

    |Field|Description|
    |-----|-----------|
    |Indicator Context information|The record that is being created.|
    |Contributing Indicator Registry \(if applicable\)|The contributing indicator with which the card is associated with.|
    |Primary Indicator \(if applicable\)|The primary indicator with which the card is associated with.|
    |Order|The order in which the card should appear.|

8.  Select **Submit**.

**Parent Topic:**[Configure Success Dashboard indicators KPIs](config-kpis-sdb.md)

