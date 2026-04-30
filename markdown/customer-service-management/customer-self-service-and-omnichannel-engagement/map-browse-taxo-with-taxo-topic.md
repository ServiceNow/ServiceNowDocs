---
title: Configure a Portal Browse Taxonomy widget to work with the Portal Taxonomy Topic widget
description: Enable users to access knowledge articles and catalog items in the Portal Taxonomy widget by selecting a topic on the card in the Topic widget.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Portal Taxonomy Topic widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Configure a Portal Browse Taxonomy widget to work with the Portal Taxonomy Topic widget

Enable users to access knowledge articles and catalog items in the Portal Taxonomy widget by selecting a topic on the card in the Topic widget.

## Before you begin

You must add and configure the Portal Browse Taxonomy widget before accessing taxonomic topic on the Portal Taxonomy Topic widget. Otherwise, an empty page displays on the Portal Taxonomy Topic widget. For more information, see [Add and configure the Portal Browse Taxonomy widget](config-portal-browse-taxo-widget.md).

You must add and configure the Portal Taxonomy Topic widget in your portal. For more information, see [Add and configure the Portal Taxonomy Topic widget](add-conf-port-taxo-topic.md).

Role required: admin or sp\_admin

## Procedure

1.  On your portal home page, in the website URL, copy the page ID.

    ```
    https://<instance-url>/<portal-id>?id=<page-id>&sys_id=<record-id>
    ```

2.  On your portal home page, press Control+right-click on the Portal Taxonomy Topic widget.

3.  Select **Instance Options**.

4.  On the Instance options window, in the Behavior section, paste the page ID into the **Browse taxonomy page** field.

5.  Select **Save**.


## Result

Selecting topics redirects the user to a Portal Browse Taxonomy widget that displays related knowledge articles and catalog items.

