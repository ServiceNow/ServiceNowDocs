---
title: Add and configure the Portal FAQ widget
description: Add the Portal FAQ widget to your portal and modify its data, presentation, and behavior. You can use the Portal FAQ widget to display a frequently asked questions list \(FAQ\) from a knowledge table on the portal.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/customer-service-management/config-portal-faq-widget-inst-optns.html
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Portal FAQ widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Add and configure the Portal FAQ widget

Add the Portal FAQ widget to your portal and modify its data, presentation, and behavior. You can use the Portal FAQ widget to display a frequently asked questions list \(FAQ\) from a knowledge table on the portal.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/customer-service-management/activate-config-portal-widget.md).

If you have not already created the page to which you want to add the widget, see [Create a page for Configurable Portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/customer-service-management/create-page-configurable-portal-widget.md).

Role required: sp\_admin or admin

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, add a set of columns by selecting the plus button \(\[Omitted image "portal-plus-icon.png"\] Alt text: Plus button\)

7.  On the Widgets pane, in the **Filter Widget** field, enter `Portal FAQ`.

8.  Drag the widget onto the container.

9.  In the Edit page, select the Portal FAQ widget.

10. Select the Pencil icon \(\[Omitted image "icon-pencil-ac.png"\] Alt text: Pencil icon\).

11. On the Instance form, fill in the fields.

    For a description of the fields values, see [Portal FAQ widget instance options form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/customer-service-management/r-port-faq-inst-options.md)

12. Select **Save**.


