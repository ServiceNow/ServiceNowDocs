---
title: Add a widget in the Portal Banner widget
description: Add a widget for additional functionality to the Portal Banner widget and configure it. For example, you could add the Portal Quick Links widget to enable users to access knowledge articles, external URLs, catalog items, or custom pages from the Portal Banner widget.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Portal Banner widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Add a widget in the Portal Banner widget

Add a widget for additional functionality to the Portal Banner widget and configure it. For example, you could add the Portal Quick Links widget to enable users to access knowledge articles, external URLs, catalog items, or custom pages from the Portal Banner widget.

## Before you begin

The UI Components for Customer Portals plugin must be installed. For more information, see [Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md).

Role required: admin or sp\_admin

## Procedure

1.  Navigate to your portal home page.

2.  On the widget you want to add, press Control+right-click.

3.  In the context menu, select **Instance in Page Editor**.

4.  In the Edit section, select the Portal Quick Links widget from the flowchart.

    The Portal Quick Links widget has been considered as an example.

5.  Select the **Instance 2**.

6.  Copy the JSON code from the **Additional options, JSON format** field.

7.  On your portal home page, press Control+right-click on the Portal Banner widget..

8.  Select **Instance Options**.

9.  In the **Behavior** section, paste the JSON code into the **Widget Option Schema** field.

10. In the **Widget Option Schema** field, modify the JSON code to update the configuration of the widget that you've added.

    For more information on each JSON parameters of the Portal Quick Links widget, see [Portal Banner widget JSON parameters](../reference/r-port-banner-widget-json-schema.md).

11. Select **Save**.


