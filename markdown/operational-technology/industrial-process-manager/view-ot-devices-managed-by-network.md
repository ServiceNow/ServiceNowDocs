---
title: View all OT devices by managed network
description: View your Operational Technology \(OT\) devices by managed network on the ServiceNow AI Platform.
locale: en-US
release: australia
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Review and update the equipment model details, Managing equipment models, Use, Industrial Process Manager, Operational Technology]
---

# View all OT devices by managed network

View your Operational Technology \(OT\) devices by managed network on the ServiceNow AI Platform.

## Before you begin

Role required: cmdb\_ot\_isa\_viewer and cmdb\_ot\_viewer

## About this task

The All OT Devices by Managed Network list on the ServiceNow AI Platform is a database view with data populated from the following tables.

-   OT Entity \[cmdb\_ot\_entity\]
-   Configuration Items \[cmdb\_ci\]
-   Configuration Item Relationships \[cmdb\_rel\_ci\]
-   Allocated IP Address \[cmdb\_ci\_allocated\_ip\_address\]
-   IP Network Subnet \[cmdb\_ci\_ip\_network\_subnet\]
-   Managed Network \[cmdb\_ci\_managed\_network\]

Using the All OT Devices by Managed Network list can help you understand the relationship between OT devices and their network.

For more information about the OT Device Network Connection data model, see the **OT Device Network Connection data model** section of Operational Technology \(OT\) extension classes.

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **Industrial Process Manager**.

2.  Select **All OT Devices by Managed Network**.

3.  In the list, you can view the following information.

    |Field|Description|
    |-----|-----------|
    |Managed Network|Name of the managed network that the OT device belongs to.|
    |IP Network Subnet Name|Identifier for the specific IP subnet that the OT device belongs to.|
    |Device IP Address|IP address assigned to the OT device that is used for communication and device management.|
    |OT Device|Name of the OT device.|
    |Parent Managed Network|Higher-level managed network that contains or oversees the current managed network.|


**Parent Topic:**[Review and update the equipment model details](equipment-model-workspace.md)

