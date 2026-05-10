---
title: Data Table from URL definition widget
description: The Data Table from URL definition widget displays the table you select from the list. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Data Table from URL definition widget

The Data Table from URL definition widget displays the table you select from the list. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

![Data Table list with Incident Fact Table selected](../image/WidgetDataTableURL.png "Data Table from URL definition widget")

**Note:** If you want this widget to be accessed by guest users, you must select the **Public** option in the widget record for both this widget and the Data Table widget.

## Instance options

Complete the instance options to define the table.

|Field|Description|
|-----|-----------|
|Title|The title of the widget. Select the **Use Instance Title** check box to use this title instead of the name of the table.|
|Glyph|Icon that displays beside the widget title|
|Bootstrap color|Color scheme for the widget. The default colors are defined by the portal theme, but if you want the instance to have a specific color, select the option from the list.|
|Link to this page|Direct users to a specific page when the click a record. By default, clicking an entry in the table opens that entry in a form.|
|Fields|Columns to display in the table. For example, short description or priority.|
|Use Instance Title|Select to use the title in the Title field instead of the table title|
|Enable Filter|Select this check box to allow users to create their own filter for the table|

**Note:** Data Table from URL Definition widget instances do not support **Maximum entries**.

If **Enable filter** is enabled in the instance options, users can add custom conditions to filter the results.

![Condition builder has the following parameters: Priority = critical, Category = Network. The list shows only three times.](../image/WidgetDataTableFilter.png "Data Table URL with condition builder")

For more information on using the condition builder, see [Create a filter in List](../../../use/using-lists/task/t_CreatingFilters.md).

**Note:** The condition builder is only available in the desktop view.

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

