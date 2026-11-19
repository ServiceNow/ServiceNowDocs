---
title: Configure a wishlist and cart for your portal header
description: Display a wishlist and cart on your portal header.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/customer-self-service-and-omnichannel-engagement/portal-config-header-wishlist.html
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure the Portal Polaris Header widget for your portal, Portal Polaris Header widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Configure a wishlist and cart for your portal header

Display a wishlist and cart on your portal header.

## Before you begin

Role required: sp\_admin or admin

## Procedure

1.  Modify JSON.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Portal**.

    2.  On the Service Portal page, search and select `Customer Support` in the Title column.

    3.  On the Customer Support page, in the **Main menu** field, select the Preview this record icon \(\[Omitted image "preview-record.png"\] Alt text: Preview this record\).

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

2.  Enable wish list.

    1.  Navigate to **Service Catalog** &gt; **Maintain Catalogs**.

    2.  Open **Customer Service** record.

    3.  Select **Enable Wish List** check-box.

    4.  Select **Update**.


