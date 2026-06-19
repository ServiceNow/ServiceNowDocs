---
title: Add and configure the Portal Banner Carousel widget
description: Add a Portal Banner Carousel widget to the portal and modify its presentation and behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/config-portal-banner-carousel-widget.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Portal Banner Carousel widget, Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Add and configure the Portal Banner Carousel widget

Add a Portal Banner Carousel widget to the portal and modify its presentation and behavior.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/activate-config-portal-widget.md).

If you have not already created the page to which you want to add the widget, see [Create a page for Configurable Portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/create-page-configurable-portal-widget.md).

Role required: sp\_admin

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, select the Pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: Pencil icon\).

7.  In the **Width** field, select **Fluid**.

8.  Select **Save**.

9.  On the container, add a set of columns by selecting the plus button \(\[Omitted image "portal-plus-icon.png"\] Alt text: Plus button\).

10. In the column, select the Edit page properties icon \(\[Omitted image "icon-portal-page.png"\] Alt text: Edit page properties icon.\) in the Service Portal Designer banner.

    **Note:** Verify that **Column** is selected in the breadcrumbs navigation.\[Omitted image "portal-banner-widget-breadcrumbs.jpg"\] Alt text: Service Portal Designer banner displaying the Column breadcrumb.

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

16. Select the Pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: Pencil icon\).

17. On the Instance form, fill in the fields.

    For a description of the field values, see [Portal Banner Carousel widget instance options form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/port-banner-carousel-inst-options.md).

18. Select **Save**.


