---
title: Add and configure the Portal Case Cards widget
description: Add a Portal Case Cards widget to your portal and modify its data, presentation, and behavior. You can use the Portal Case Cards widget to display status, priority, and other relevant details related to your cases.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Portal Case Cards widget, Set up Configurable Portal widgets, Set up self-service, Configure, Customer Service Management]
---

# Add and configure the Portal Case Cards widget

Add a Portal Case Cards widget to your portal and modify its data, presentation, and behavior. You can use the Portal Case Cards widget to display status, priority, and other relevant details related to your cases.

## Before you begin

The UI Components for Customer Portals plugin must have been activated. For more information, see [Activate the UI Components for Customer Portals plugin](activate-config-portal-widget.md)

If you have not already created the page to which you want to add the widget, see [Create a page for Configurable Portal widgets](create-page-configurable-portal-widget.md).

Role required: sp\_admin

## Procedure

1.  Navigate to the **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  On the Service Portal Designer page, search for and select the page to which you want to add the widget.

4.  Select the **Widgets** tab.

5.  In the Layouts section, drag the Container layout onto the portal edit page.

6.  On the container, add a set of columns by selecting the plus button \(![Plus button](../image/portal-plus-icon.png)\).

7.  On the Widgets pane, in the **Filter Widget** field, enter `Portal Case Cards`.

8.  Drag the widget onto the container.

9.  In the Edit page, select the Portal Case Cards widget.

10. Select the Pencil icon \(![Pencil icon](../image/icon-pencil-ac.png)\).

11. If you want to use configured background and text colors to indicate the state of the cases displayed in the widget, enter JSON code in the following format in the **State Highlight Color** field and modify it with your desired colors.

    The default text color for all case states is \#181A1F \(black\). If you create a state, the default highlight color is \#CBE9FC \(light blue\) and the text color is \#181A1F \(black\). For more information about the default color values, see [Default highlight color for different case states](../reference/portal-case-cards-widget-default-color.md).

    ```
    [
      {
        "value": "1",
        "background_colour": "#CBE9FC",
        "text_colour": "#181A1F"
      },
      {
        "value": "10",
        "background_colour": "#D1D2EE",
        "text_colour": "#181A1F"
      },
      {
        "value": "18",
        "background_colour": "#FBF7BF",
        "text_colour": "#181A1F"
      },
      {
        "value": "6",
        "background_colour": "#D2EABC",
        "text_colour": "#181A1F"
      },
      {
        "value": "3",
        "background_colour": "#C2C4CA",
        "text_colour": "#181A1F"
      },
      {
        "value": "7",
        "background_colour": "#FFCCD2",
        "text_colour": "#181A1F"
      }
    ]
    ```

    For &lt;value&gt;, enter an integer value of the case state for which you want to change the colors. For more information about finding this value, see [Display the integer values of all case states](integer-value-case-states.md).

12. On the Instance form, fill in the fields.

    For a description of the field values, see [Portal Case Cards widget instance options form](../reference/r-port-case-cards-instan-options.md).

13. Select **Save**.


