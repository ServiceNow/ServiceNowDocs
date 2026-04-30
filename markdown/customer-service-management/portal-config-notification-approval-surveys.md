---
title: Configure notification, approval, and survey for your portal header
description: Display menu items like notification, approval, and survey on your portal header.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure the Portal Polaris Header widget for your portal, Portal Polaris Header widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure notification, approval, and survey for your portal header

Display menu items like notification, approval, and survey on your portal header.

## Before you begin

The Portal Next Experience theme should have been activated.

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portal**.

2.  On the Service Portal page, search and select `Customer Support` in the Title column.

3.  On the Customer Support page, in the **Main menu** field, select the Preview this record icon \(![Preview this record](../image/preview-record.png)\).

4.  Select **Open Record** on the Instance with Menu pop-up window.

5.  On the Portal revamp demo menu page, select **New** in the related list and create notifications, approvals, and surveys.

6.  Create a notification item on the header.

    1.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Label|Name that appears for the item on the header. The default text is `Notification`.|
        |Parent Menu|This field should already contain the name of the menu you’re adding items to.|
        |Order|Value that determines where the item appears in the menu in relation to other menu items.|
        |Type|The type of page the item links to. You must select **Scripted List** from the list.|
        |Application|Application for the menu item|
        |Condition|Determines what conditions are required for menu items to show on the header.|
        |Glyph|Icon that appears next to the item.|

    2.  Select **Submit**.

7.  Create an approval item on the header.

    1.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |Label|Name that appears for the item on the header. The default text is `Approval`.|
        |Parent Menu|This field should already contain the name of the menu you’re adding items to.|
        |Order|Value that determines where the item appears in the menu in relation to other menu items.|
        |Type|The type of page the item links to. You must select **Scripted List** from the list.|
        |Application|Application for the menu item|
        |Condition|Determines what conditions are required for menu items to show on the header.|
        |Glyph|Icon that appears next to the item.|

    2.  Select **Submit**.

8.  Create a survey item on the header.

    1.  On the form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |Label|Name that appears for the item on the header. The default text is `Survey`.|
        |Parent Menu|This field should already contain the name of the menu you’re adding items to.|
        |Order|Value that determines where the item appears in the menu in relation to other menu items.|
        |Type|The type of page the item links to. You must select **Scripted List** from the list.|
        |Application|Application for the menu item|
        |Condition|Determines what conditions are required for menu items to show on the header.|
        |Glyph|Icon that appears next to the item.|

    2.  Select **Submit**.


