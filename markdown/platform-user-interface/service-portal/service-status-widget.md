---
title: Service Status widget
description: The Service Status widget provides a visual representation of service availability over the past three months. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Portal service status widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Status widget

The Service Status widget provides a visual representation of service availability over the past three months. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

The Service Status widget displays the history of service availability for one service from the Services \[cmdb\_ci\_service\] table. The widget uses the page URL to determine which service to represent.

![Service Status widget](../image/WidgetServiceStatus.png "Service Status widget")

Each pill represents one day. Each color correlates with a type of service availability. To include additional details when you hover over a pill, such as the task number or short description, you must clone the widget and edit the server script.

|Color|Service availability|
|-----|--------------------|
|Green|No issues|
|Blue|Planned maintenance|
|Yellow|Service degradation|
|Red|Outage|

## Instance options

The Service Status widget does not have any included instance options.

**Parent Topic:**[Service Portal service status widgets](service-status-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

