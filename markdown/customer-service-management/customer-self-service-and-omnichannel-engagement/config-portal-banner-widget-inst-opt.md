---
title: Add and configure the Portal Banner widget
description: Add a Portal Banner widget to your portal and modify its appearance and behavior. You can use the Portal Banner widget to display announcements, new product or feature highlights, and important information on the portal page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/config-portal-banner-widget-inst-opt.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Portal Banner widget, Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Add and configure the Portal Banner widget

Add a Portal Banner widget to your portal and modify its appearance and behavior. You can use the Portal Banner widget to display announcements, new product or feature highlights, and important information on the portal page.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/activate-config-portal-widget.md)

If you have not already created the page to which you want to add the widget, see [Create a page for Configurable Portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/create-page-configurable-portal-widget.md).

Role required: sp\_admin

## About this task

Configure portal banner widget 

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Add container.

    1.  Select the **Widgets** tab.

    2.  In the Layouts section, drag the Container layout onto the portal edit page.

    3.  On the container, select the Pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: Pencil icon\).

    4.  In the **Width** field, select **Fluid**.

    5.  Select **Save**.

5.  Add columns to container.

    1.  On the container, add a set of columns by selecting the plus button \(\[Omitted image "portal-plus-icon.png"\] Alt text: Plus button\).

    2.  In the column, select the Edit page properties icon \(\[Omitted image "icon-portal-page.png"\] Alt text: Edit page properties icon.\).

        **Note:** Verify that **Column** is selected in the breadcrumbs navigation.\[Omitted image "portal-banner-widget-breadcrumbs.jpg"\] Alt text: Service Portal Designer banner displaying the Column breadcrumb

    3.  Select the Edit page properties icon \(\[Omitted image "icon-portal-page.png"\] Alt text: Edit page properties icon.\) in the banner in Service Portal Designer.

    4.  On the Page window, in the **Page Specific CSS** field, paste the following CSS code.

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

    5.  Select **Save**.

6.  Add portal banner widget.

    1.  On the Widgets pane, in the **Filter Widget** field, enter `Portal Banner`.

    2.  Drag the widget onto the container.

    3.  In the Edit page, select the Portal Banner widget.

    4.  Select the Pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: Pencil icon\).

    5.  On the Instance form, in the **Presentation** field, paste the following JSON code into the **Search Placeholder Text** field.

        ```
        {
            "title": "enter the title",
            "size": "enter the size of search bar",
            "color": "enter color"
        }
        ```

        For more information about each parameter, see [Script parameters for the search option in the Portal Banner widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/json-param-search-option-banner-widget.md).

    6.  On the Instance form, fill in the fields.

        For a description of the field values, see [Portal Banner widget instance options form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/banner-widget-inst-options.md).

    7.  Select **Save**.


