---
title: Configure a wishlist and cart for your portal header
description: Display a wishlist and cart on your portal header.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure the Portal Polaris Header widget for your portal, Portal Polaris Header widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure a wishlist and cart for your portal header

Display a wishlist and cart on your portal header.

## Before you begin

The Portal Next Experience theme should have been activated.

Role required: sp\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Portal**.

2.  On the Service Portal page, search and select `Customer Support` in the Title column.

3.  On the Customer Support page, in the **Main menu** field, select the Preview this record icon \(![Preview this record](../image/preview-record.png)\).

4.  Select **Open Record** on the Instance with Menu pop-up window.

5.  On the Portal revamp demo menu page, in the **Additional options, JSON format** field, modify the JSON as shown.

    ```
    {
      
      "enable_cart": {
        "displayValue" : "true",
        "value": false
      },
      "enable_wishlist": {
        "displayValue" : "true",
        "value": false
      }
    }
    ```

6.  Select **Update**.


