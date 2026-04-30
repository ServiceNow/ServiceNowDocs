---
title: Add and configure the Portal Banner Carousel widget
description: Add a Portal Banner Carousel widget to the portal and modify its presentation and behavior.
locale: en-US
release: zurich
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Portal Banner Carousel widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Add and configure the Portal Banner Carousel widget

Add a Portal Banner Carousel widget to the portal and modify its presentation and behavior.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md).

If you have not already created the page to which you want to add the widget, see [Create a page for Configurable Portal widgets](create-page-configurable-portal-widget.md).

Role required: sp\_admin or admin

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, select the Pencil icon \(![Pencil icon](../image/icon-pencil-ac.png)\).

7.  In the **Width** field, select **Fluid**.

8.  Select **Save**.

9.  On the container, add a set of columns by selecting the plus button \(![Plus button](../image/portal-plus-icon.png)\).

10. In the column, select the Edit page properties icon \(![Edit page properties icon.](../image/icon-portal-page.png)\) in the Service Portal Designer banner.

    **Note:** Verify that **Column** is selected in the breadcrumbs navigation.![Service Portal Designer banner displaying the Column breadcrumb.](../image/portal-banner-widget-breadcrumbs.jpg)

11. On the Page window, in the **Page Specific CSS** field, paste the following CSS code:

    ```
    .col-md-12{ 
         padding-left: 0;
         padding-right: 0; 
     }
    .padding-top {
         padding-top: 0;
     } 
    ```

    If a message appears about the application scope, select **here** to be able to edit the record.

12. Select **Save**.

13. On the Widgets pane, in the **Filter Widget** field, enter `Portal Banner Carousel`.

14. Drag the widget onto the container.

15. In the Edit page, select the Portal Banner Carousel widget.

16. Select the Pencil icon \(![Pencil icon](../image/icon-pencil-ac.png)\).

17. On the Instance form, fill in the fields.

    For a description of the field values, see [Portal Banner Carousel widget instance options form](../reference/port-banner-carousel-inst-options.md).

18. Select **Save**.


