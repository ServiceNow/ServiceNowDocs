---
title: Portal Data List widget instance options form
description: The instance options enable you to configure the Portal Data List widget on a portal page.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configurable Portal widgets instance options, Customer Service Management reference, Customer Service Management]
---

# Portal Data List widget instance options form

The instance options enable you to configure the Portal Data List widget on a portal page.

<table id="table_csm_base_entities"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Data

</td><td>

Defines the configuration of different categories in the navigation within the widget.

</td></tr><tr><td>

Dynamic data list

</td><td>

Option to display records dynamically based on the configuration provided in the parameter of a portal page URL. **Note:**

-   The configuration enables administrator to display records from any tables by passing following URL parameters: table, filter, sort order, view, and target view page.
-   When the **Dynamic data list** is selected, the JSON configuration in the **Data** field is not available.

</td></tr></tbody>
</table>|Instance option|Description|
|---------------|-----------|
|Categories heading|Required title for all categories. The default text is `Categories`.|

<table id="table_hsg_14z_2zb"><thead><tr><th>

Instance option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Layout

</td><td>

Layout type of the case records and their details displayed in the widget. The available options are:

-   List view \(for both desktop and mobile\)
-   Card view \(for both desktop and mobile\)
-   List view \(for desktop\) &amp; Card view \(for mobile\)

**Note:** Currently, if you select None, the layout is set to List view \(for desktop\) &amp; Card view \(for mobile\).

The default layouts are:

-   Desktop: List view \(for desktop\) &amp; Card view \(for mobile\)
-   Mobile: Card view \(for both desktop and mobile\)

</td></tr><tr><td>

Number of records per page \(Desktop\)

</td><td>

The number of cases to appear by default on the widget in the desktop. The default value is 20. The maximum value is 1000.

</td></tr><tr><td>

Number of records per page \(Mobile\)

</td><td>

The number of cases to appear by default on the widget on a mobile device. The default value is 8.

</td></tr><tr><td>

Show search

</td><td>

Option to display a search field in the widget.

</td></tr><tr><td>

Show export actions

</td><td>

Option to enable the export of records in pdf, Excel, and csv formats.

</td></tr><tr><td>

Categories condition script

</td><td>

Script to show or hide the data list category on the widget. For more information, see [Hide or show categories in the Data List widget](../task/create-cond-script-datalist-widget.md).The default script is **DataListCategoryConditionScript**.

</td></tr></tbody>
</table>**Related topics**  


[Portal Data List widget](../concept/portal-data-list-widget.md)

[Add and configure the Portal Data List widget](../task/config-data-list-widget-inst-optns.md)

[Hide or show categories in the Data List widget](../task/create-cond-script-datalist-widget.md)

