---
title: RPA Desktop Design Studio ports
description: Components in the RPA Desktop Design Studio have ports that are used while creating an automation workflow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Build, RPA Desktop Design Studio, Workflow Data Fabric]
---

# RPA Desktop Design Studio ports

Components in the RPA Desktop Design Studio have ports that are used while creating an automation workflow.

The ports are categorized as Control ports and Data ports.

The gray ports are called the Control ports and the orange ports are called the Data ports.

![Control ports and Data ports of a component.](../image/ports-overview-studio.png)

The ports are subcategorized into input ports and output ports.

Control ports are subcategorized into Control In and Control Out ports. Control ports decide the flow of the automation execution \(which component to execute next\).

Data ports are subcategorized into Data In and Data Out ports. Data ports transfer data between components.

Arrow heads on the connection lines indicate the flow of the direction.

Input ports always appear on the left of the component and output ports appear on the right of the component.

Hover over the port to see the function of the port.

![Control In, Control Out, Data In, and Data Out ports.](../image/ports-in-out-studio.png)

A Data port turns red when you turn off the logging on that port. For example, select this option if you don’t want to log sensitive information such as password or banking details. To do that, right-click the Data In or Data Out port and select **Turn off logging**. ![Turn off logging for a Data port.](../image/port-turn-off-logging.png)

To turn on the logging, right-click the inactive Data port and select **Turn on logging**.

A Data port turns green when the data is transformed. For example, it turns green when it converts any information existing within a Data port from one format to another. To do that, right-click the Data In or Data Out port and select **Transform Data**. For more information, see [Transform the data in RPA Desktop Design Studio](../task/transform-data-gen-rpa-studio.md).

**Parent Topic:**[Building automations](rpa-studio-build.md)

