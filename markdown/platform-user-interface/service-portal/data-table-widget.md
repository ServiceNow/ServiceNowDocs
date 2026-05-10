---
title: Data table from instance definition widget
description: Display a filtered list on your portal using the data table from instance definition widget. From the widget's context menu, portal users can export the filtered list. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Data table from instance definition widget

Display a filtered list on your portal using the data table from instance definition widget. From the widget's context menu, portal users can export the filtered list. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

After you add the data table from instance definition widget to a page, use the instance options to configure the appearance of the table.

![Data table from instance definition widget with instance option set to table=incident](../image/DataTableInstanceDefinition.png "Data table from instance definition widget")

**Note:** If you want this widget to be accessed by guest users, you must select the **Public** option in the widget record for both this widget and the Data Table widget.

## Instance options

|Field|Description|
|-----|-----------|
|Table|The table that the widget displays records from.|
|Filter|Text field from the condition builder that you can use to limit the items returned in the table. To create a filter, use the context menu to open the widget instance in the platform. Then use the condition builder to create a filter.|
|Fields|Columns to display in the table.|
|Maximum entries|Limits the number of items displayed in the table. If there are more entries than allowed in the table, users can scroll to the next page.|
|Order by|The table field used to order items.|
|Order direction|The direction to order items: ascending or descending.|
|Title|The title of the widget. If you leave this field empty the name of the table displays as the widget name.|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Glyph|Icon that displays beside the widget title.|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Link to this page|Direct users to a specific page when they click a record. By default, clicking an entry in the table opens that entry in a form.|

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

