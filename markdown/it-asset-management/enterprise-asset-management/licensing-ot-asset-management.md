---
title: OT Asset Management licensing
description: The ServiceNow platform uses a licensing method where your organization is charged for using the OT Asset Management application. In this licensing model, all assets of the Industrial model categories are charged based on the Subscription unit ratio.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [OT Asset Management, Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# OT Asset Management licensing

The ServiceNow® platform uses a licensing method where your organization is charged for using the OT Asset Management application. In this licensing model, all assets of the Industrial model categories are charged based on the Subscription unit ratio.

The ServiceNow® OT Asset Management licensing is based on resource categories. A resource category is a group of related model categories. The OT Asset Management application supports some default resource categories. These resource categories enable assets of the Industrial model categories to utilize the features and workflows of the OT Asset Management application. Any asset of the Industrial model category is counted toward a Subscription Unit based on the predefined ratio of number of assets to subscription units.

When you create a custom model category with a licensable Industrial model category as its parent, the custom model category is automatically associated with the resource category of the parent model category. Based on the resource category, the assets of these custom model categories are licensed and counted toward a Subscription Unit.

**Note:** When the OT Asset Management application is activated on your ServiceNow instance, all the OT Asset Management license resource categories are opted in by default.

<table id="table_u3k_gqm_1bc"><thead><tr><th>

Resource category

</th><th>

Subscription unit ratio

</th><th>

Model category

</th></tr></thead><tbody><tr><td>

Unclassed OT

</td><td>

1:1

</td><td>

-   Industrial
-   Industrial General

</td></tr><tr><td>

OT Supervisory System

</td><td>

1:1

</td><td>

-   OT Supervisory
-   OT Supervisory EWS
-   OT Supervisory Historian
-   OT Supervisory HMI
-   OT Supervisory OPC
-   OT Supervisory SCADA

</td></tr><tr><td>

OT Control System

</td><td>

3:1

</td><td>

-   OT Control
-   OT Control 3D Printer
-   OT Control CNC
-   OT Control DCS
-   OT Control DPU
-   OT Control IED
-   OT Control Module
-   OT Control PLC
-   OT Control RTU
-   OT Control SCADA
-   OT Control Server

</td></tr><tr><td>

OT Field Devices

</td><td>

10:1

</td><td>

-   OT Field Actuator
-   OT Field Device
-   OT Field Drive
-   OT Field Robot
-   OT Field Sensor

</td></tr><tr><td>

Industrial Consumable

</td><td>

25:1

</td><td>

Any consumable asset created using any of the preceding model categories.

</td></tr><tr><td>

Operational Equipment

</td><td>

1:1

</td><td>

Not applicable

</td></tr></tbody>
</table>The Subscription unit ratio is the ratio of the number of assets to the number of subscription units. For example, the subscription unit ratio of Industrial Consumable is 25:1, where 25 assets require a single unit of license. If 1 license costs $100, then 25 industrial consumable assets cost $100 and 50 industrial consumable assets cost $200.

You can view the subscription details of your OT Asset Management application using the ITAM License Report. For more details, see [View the license report for the OT Asset Management application](../task/view-license-report-otam.md).

**Parent Topic:**[OT Asset Management](ot-asset-management.md)

**Related topics**  


[OT Asset Workspace](ot-asset-ws-otam.md)

