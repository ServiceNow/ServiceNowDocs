---
title: Portal Data List widget
description: The Portal Data List widget displays data related to cases from selected case tables in either a list or card format.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Portal Data List widget

The Portal Data List widget displays data related to cases from selected case tables in either a list or card format.

The list view displays a columnar list of cases and their information. You can also display the data list without the category on the left and pin the first column.

![Portal Data List widget displaying different cases and their details in list format.](../image/portal-datalist-widget-list-view.png "Portal Data List widget list view")

The card view displays case information in stacked cards.

![Portal Data List widget displaying different cases and their details in card format.](../image/portal-datalist-widget-card-view.png "Portal Data List widget card view")

![Data List widget displaying list of cases without categories.](../image/data-list-without-categories.png "Portal Data List widget without categories")

Each row in the widget represents a record. You can search, view, sort, and interact with the information presented.

For more information about how to configure the instance options for the Portal Data List widget, see [Add and configure the Portal Data List widget](../task/config-data-list-widget-inst-optns.md).

The Data List portal widget can be used in the following scenarios:

-   Dynamic data list: Enables you to display records dynamically based on the configuration provided in the URL parameters. It avoids the need to create duplicate list pages. You can use a common page to display records from any table by passing the following URL parameters: table, filter, sort order, view, and target view page.
-   Static data list: Ability to display records from one or more tables specified in the widget instance options. It enables you to personalize the data list experience for a particular entity or table, such as cases, products, contacts, and so on.
-   Related data list: Enables you to display records associated with an entity on the record view page. The data list is configured to identify the entity specified in the URL and filters the records accordingly.

