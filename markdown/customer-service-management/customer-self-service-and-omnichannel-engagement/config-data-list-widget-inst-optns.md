---
title: Add and configure the Portal Data List widget
description: Add a Portal Data List widget to your portal and modify its data, appearance, and behavior. You can use the Portal Data List widget to display different case-related data in a card or list format on your portal.
locale: en-US
release: yokohama
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Portal Data List widget, Set up Configurable Portal widgets, Set up self-service, Configuring Customer Service Management, Customer Service Management]
---

# Add and configure the Portal Data List widget

Add a Portal Data List widget to your portal and modify its data, appearance, and behavior. You can use the Portal Data List widget to display different case-related data in a card or list format on your portal.

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

6.  On the container, add a set of columns by selecting the plus button \(![Plus button](../image/portal-plus-icon.png)\).

7.  On the Widgets pane, in the **Filter Widget** field, enter `Portal Data List`.

8.  Drag the widget onto the container.

9.  In the Edit page, select the Portal Data List widget.

10. Select the Pencil icon \(![Pencil icon](../image/icon-pencil-ac.png)\).

11. On the instance options page, in the **Data** field, paste and update the following JSON code to configure the lists.

    ```
    [
      {
        "category": "All Cases",
        "table": "sn_customerservice_case",
        "list_view": "Case",
        "card_view_primary_column": "number",
        "card_view_secondary_column": "short_description",
        "card_view_additional_columns": "product|priority|state|contact",
        "glyph": "th-list",
        "target_page_id": "csm_ticket",
        "sub_categories": [
          {
            "sub_category": "Open",
            "sub_category_query": "active=true"
          },
          {
            "sub_category": "Closed",
            "sub_category_query": "active=false"
          }
        ],
        "run_time_filters": [
          {
            "column": "priority",
            "selection_type": "single_select",
            "values": [
              {
                "label": "1-Critical",
                "value": 1
              },
              {
                "label": "2-High",
                "value": 2
              },
              {
                "label": "3-Moderate",
                "value": 3
              },
              {
                "label": "4-Low",
                "value": 4
              }
            ]
          },
          {
            "column": "state",
            "selection_type": "multi_select"
          },
          {
            "column": "contact",
            "selection_type": "multi_select"
          },
          {
            "column": "sys_updated_on",
            "selection_type": "single_select",
            "ranges": [
              {
                "label": "Last month",
                "query": "sys_updated_on>javascript:gs.endOfLastMonth()"
              },
              {
                "label": "Last 3 months",
                "query": "sys_updated_on>javascript:gs.beginningOfLast3Months()"
              },
              {
                "label": "Last 6 months",
                "query": "sys_updated_on>javascript:gs.beginningOfLast6Months()"
              }
            ]
          }
        ]
      },
      {
        "category": "Actions Needed",
        "table": "sn_customerservice_case",
        "view": "Case",
        "card_view_primary_column": "number",
        "card_view_secondary_column": "short_description",
        "card_view_additional_columns": "product|priority|state|contact",
        "filter": "stateIN6,18",
        "glyph": "check",
        "target_page_id": "csm_ticket"
      },
      {
        "category": "Work Orders",
        "table": "wm_order",
        "card_view_primary_column": "number",
        "card_view_secondary_column": "short_description",
        "card_view_additional_columns": "priority|state",
        "glyph": "briefcase"
      }
    ]
    ```

    For more information, see [Portal Data List widget JSON parameters](../reference/portal-datalist-widget-data-json.md).

    Each category in the widget displays a list of filtered records from a selected table. The default table is the Case \[sn\_customerservice\_case\] table. In a category, you can further filter the records and display them in tabs using the **pre\_defined\_filters** parameter. You can also configure the filter options displayed in the filter icon using the **run\_time\_filters** parameter.

12. On the Instance form, fill in the fields.

    For a description of the field values, see [Portal Data List widget instance options form](../reference/r-port-data-list-inst-options.md).

13. Select **Save**.


