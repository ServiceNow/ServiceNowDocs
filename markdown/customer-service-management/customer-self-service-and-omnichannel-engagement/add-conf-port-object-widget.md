---
title: Add and configure the Portal Object widget
description: Add a Portal Object widget to your portal and modify its data and behavior. You can use the Portal Object widget to display important information and actions related to records from a defined table on your portal homepage.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Portal Object widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Add and configure the Portal Object widget

Add a Portal Object widget to your portal and modify its data and behavior. You can use the Portal Object widget to display important information and actions related to records from a defined table on your portal homepage.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md)

If you haven’t already created the page to which you want to add the widget, see [Create a page for Configurable Portal widgets](create-page-configurable-portal-widget.md).

Role required: sp\_admin

## About this task

The Portal Object widget displays the information based on the sy\_id entered in the widget instance options. If no sys\_id is provided in the instance options, the widget uses the sys\_id parameter provided in the URL.

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, add a set of columns by selecting the plus button \(![Plus button](../image/portal-plus-icon.png)\).

7.  On the Widgets pane, in the **Filter Widget** field, enter `Portal Object`.

8.  Drag the widget onto the container.

9.  In the Edit page, select the Portal Object widget.

10. Enable editing of the widget by selecting the Pencil icon \(![Pencil icon](../image/icon-pencil-ac.png)\).

11. On the Instance form, fill in the fields.

    For a description of the field values, see [Portal Object widget instance options form](../reference/port-object-inst-options.md).

12. Select **Save**.


