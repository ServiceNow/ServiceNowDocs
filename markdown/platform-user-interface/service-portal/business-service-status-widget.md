---
title: Business Service Status widget
description: View how services are running on your system. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Portal service status widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Business Service Status widget

View how services are running on your system. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

The Business Service Status widget pulls information from the cmdb\_ci\_service table. You can change where the data comes from in a cloned version of the widget by adjusting the settings in the widget server script.

![Business Service Status widget](../image/WidgetBusinessServiceStatus.png "Business Service Status widget")

## Instance options

![Instance options for the Business Service Status widget, which include the option to limit the number of services shown](../image/IOBusinessServiceStatus.png "Business Service Status widget instance options")

|Field|Description|
|-----|-----------|
|Title|Name of the widget. This only appears in the header for the widget instance options, it is not user-facing. To change the title for the list of services, clone and edit the widget HTML.|
|Glyph|Icon for the widget. This is not user-facing.|
|Number of Services|The number of services displayed in the widget. The default number is 250.|

**Parent Topic:**[Service Portal service status widgets](service-status-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

