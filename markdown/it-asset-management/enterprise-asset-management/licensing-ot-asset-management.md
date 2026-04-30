---
title: OT Asset Management licensing
description: The ServiceNow platform uses a licensing method where your organization is charged for using the OT Asset Management application. In this licensing model, all assets of the Industrial and Hardware model categories are charged based on the Subscription unit ratio.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [OT Asset Management, Explore, Enterprise Asset Management, IT Asset Management]
---

# OT Asset Management licensing

The ServiceNow® platform uses a licensing method where your organization is charged for using the OT Asset Management application. In this licensing model, all assets of the Industrial and Hardwaremodel categories are charged based on the Subscription unit ratio.

The ServiceNow® OT Asset Management licensing is based on resource categories. A resource category is a group of related model categories. The OT Asset Management application supports some default resource categories. These resource categories enable assets of the Industrial and Hardwaremodel categories to use the features and workflows of the OT Asset Management application. Any asset of the Industrial and Hardwaremodel category is counted toward a Subscription Unit based on the predefined ratio of number of assets to subscription units.

When you create a custom model category with a licensable Industrial or Hardwaremodel category as its parent, the custom model category is automatically associated with the resource category of the parent model category. Based on the resource category, the assets of these custom model categories are licensed and counted toward a Subscription Unit.

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

</td></tr><tr><td class="sub-head" colspan="3">

Hardware resource categories

</td></tr><tr><td>

OT Servers

</td><td>

1:1

</td><td>

Any model category which contains **Server** in the name and belongs to the alm\_asset or alm\_hardware class. Examples:-   AIX Server
-   ESX Server
-   HPUX Server
-   Linux Server
-   Netware Server
-   OS/X Server
-   Solaris Server
-   UNIX Server
-   Windows Server

</td></tr><tr><td>

OT Network Gear

</td><td>

5:1

</td><td>

-   IP Router
-   IP Switch
-   Network Gear

</td></tr><tr><td>

OT Storage

</td><td>

3:1

</td><td>

Storage Device

</td></tr><tr><td>

OT End User Computers

</td><td>

4:1

</td><td>

Computer

</td></tr><tr><td>

OT Mobile Devices

</td><td>

10:1

</td><td>

Mobile Device

</td></tr><tr><td>

OT Monitors

</td><td>

15:1

</td><td>

Monitor

</td></tr><tr><td>

OT Printers

</td><td>

10:1

</td><td>

Printer

</td></tr><tr><td>

OT Unclassified Hardware

</td><td>

1:1

</td><td>

Hardware

</td></tr></tbody>
</table>The Subscription unit ratio is the ratio of the number of assets to the number of subscription units. For example, the subscription unit ratio of Industrial Consumable is 25:1, where 25 assets require a single unit of license. If 1 license costs $100, then 25 industrial consumable assets cost $100 and 50 industrial consumable assets cost $200.

You can view the subscription details of your OT Asset Management application using the ITAM License Report. For more details, see [View the license report for the OT Asset Management application](../task/view-license-report-otam.md).

## OT hardware assets in OT Asset Management licensing

The OT Asset Management licensing model includes a few default hardware resource categories to license OT hardware assets.

In the OT Asset Management licensing model, only hardware assets with the **OT entity** flag set to **true** are licensed and counted toward a Subscription unit under the hardware resource categories of OT Asset Management licensing. The OT Asset Management workflows support OT hardware assets.

**Note:** Non-OT Hardware assets with the **OT entity** flag set to **false** can't use the features and workflows of the OT Asset Management application even if you have installed the application. The non-OT hardware assets aren't licensed under OT Asset Management.

The Hardware Asset Management \(HAM\) licensing model includes default resource categories equivalent to the hardware resource categories of OT Asset Management.

|OTAM hardware resource category|Equivalent HAM resource category|
|-------------------------------|--------------------------------|
|OT Servers|Servers|
|OT Network Gear|Network Gear|
|OT Storage|Storage|
|OT End User Computers|End User Computers|
|OT Mobile Devices|Mobile Devices|
|OT Monitors|Monitors|
|OT Printers|Printers|
|OT Unclassified hardware|Unclassified Hardware|

When both OT Asset Management and Hardware Asset Management applications or licensed HAM solutions are activated, and HAM resource categories are opted in, consider the following points:

-   OT hardware assets are licensed only under the hardware resource categories of OT Asset Management licensing.
-   Non-OT hardware assets are licensed only under the resource categories of HAM licensing.
-   OT Asset Management workflows support only OT hardware assets.
-   HAM workflows support both OT hardware assets and non-OT hardware assets.

For more details on licensing hardware assets, see [Licensing framework for Hardware Asset Management solutions](../../hardware-asset-management/concept/licensing-ham-solutions.md).

**Parent Topic:**[OT Asset Management](ot-asset-management.md)

**Related topics**  


[View the license report for the OT Asset Management application](../task/view-license-report-otam.md)

[OT Asset Workspace](ot-asset-ws-otam.md)

[Asset and Configuration Item \(CI\) synchronization for Operational Technology \(OT\) assets](asset-ci-sync-ot-assets.md)

