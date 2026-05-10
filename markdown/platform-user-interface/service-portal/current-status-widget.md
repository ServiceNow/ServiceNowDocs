---
title: Current Status widget
description: The Current Status widget displays any issues reported in the system. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Portal service status widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Current Status widget

The Current Status widget displays any issues reported in the system. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

The Current Status widget checks the Outages \[cmdb\_ci\_outage\] table to see if the system is experiencing any outages.

Service owners and service desk managers report planned or unplanned outages by creating outage records. Each outage record includes **Begin** and **End** fields to indicate the duration of the outage. If the **End** time is later or empty, then the outage is still ongoing. The Current Status widget displays all ongoing outages.

![Current Status widget](../image/WidgetCurrentStatus.png "Current Status widget")

The Current Status displays outages only for services, which are tracked in the Services \[cmdb\_ci\_service\] table.

## Instance options

Use the instance options to configure the Current Status widget for a portal page.

|Field|Description|
|-----|-----------|
|Show outage details|Option to display details from the Outage \[cmdb\_ci\_outage\] record.|
|Standalone|Option to remove explanatory information. This option also adds a link to more information.|

**Parent Topic:**[Service Portal service status widgets](service-status-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

