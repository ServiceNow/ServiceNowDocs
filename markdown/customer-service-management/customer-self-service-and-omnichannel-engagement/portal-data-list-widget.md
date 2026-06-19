---
title: Portal Data List widget
description: The Portal Data List widget displays data related to cases from selected case tables in either a list or card format.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/portal-data-list-widget.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Portal Data List widget

The Portal Data List widget displays data related to cases from selected case tables in either a list or card format.

The list view displays a columnar list of cases and their information. You can also display the data list without the category on the left and pin the first column.

\[Omitted image "portal-datalist-widget-list-view.png"\] Alt text: Portal Data List widget displaying different cases and their details in list format.

The card view displays case information in stacked cards.

\[Omitted image "portal-datalist-widget-card-view.png"\] Alt text: Portal Data List widget displaying different cases and their details in card format.

\[Omitted image "data-list-without-categories.png"\] Alt text: Data List widget displaying list of cases without categories.

Each row in the widget represents a record. You can search, view, sort, and interact with the information presented.

For more information about how to configure the instance options for the Portal Data List widget, see [Add and configure the Portal Data List widget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/config-data-list-widget-inst-optns.md).

The Data List portal widget can be used in the following scenarios:

-   Dynamic data list: Enables you to display records dynamically based on the configuration provided in the URL parameters. It avoids the need to create duplicate list pages. You can use a common page to display records from any table by passing the following URL parameters: table, filter, sort order, view, and target view page.
-   Static data list: Ability to display records from one or more tables specified in the widget instance options. It enables you to personalize the data list experience for a particular entity or table, such as cases, products, contacts, and so on.
-   Related data list: Enables you to display records associated with an entity on the record view page. The data list is configured to identify the entity specified in the URL and filters the records accordingly.

