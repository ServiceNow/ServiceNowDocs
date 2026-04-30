---
title: Licensing framework for Hardware Asset Management solutions
description: Manage the subscription units purchased and consumed by your organization for all the Hardware Asset Management solutions with the improved HAM licensing framework. When more than one Hardware Asset Management solution is activated on a ServiceNow instance, any licensable and opted-in resource category is licensed only under one solution.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
keywords: [HAM licensing, Hardware Asset Management licensing]
breadcrumb: [Hardware Asset Management subscription, Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Licensing framework for Hardware Asset Management solutions

Manage the subscription units purchased and consumed by your organization for all the Hardware Asset Management solutions with the improved HAM licensing framework. When more than one Hardware Asset Management solution is activated on a ServiceNow instance, any licensable and opted-in resource category is licensed only under one solution.

The licensed solutions like Hardware Asset Management integration with Zero Touch Mobility and Hardware Asset Management integration with Telecommunications Network Inventory install the Hardware Asset Management on your ServiceNow instance.

Each Hardware Asset Management solution supports some default resource categories that can avail Hardware Asset Management features and workflows.

<table id="table_ecs_3gz_x1c"><thead><tr><th>

Application/Solution

</th><th>

Supported resource categories

</th></tr></thead><tbody><tr><td>

Hardware Asset Management integration with Zero Touch Mobility

</td><td>

Mobile Device

</td></tr><tr><td>

Hardware Asset Management integration with Telecommunications Network Inventory

</td><td>

-   Telecom Network Inventory
-   Server
-   Network Gear

</td></tr><tr><td>

Hardware Asset Management

</td><td>

-   End User Computers
-   Mobile Device
-   Server
-   Network Gear
-   Printers
-   Monitors
-   Storage
-   Unclassified hardware

</td></tr></tbody>
</table>HAM licensing is based on the subscription unit ratio defined for each resource category. You can opt in and pay for only those resource categories that you want to use. For more information, see [Hardware Asset Management licensing](ham-licensing.md).

## License prioritization for Hardware Asset Management solutions

**Important:** The HAM license prioritization feature is available with Hardware Asset Management version 10.1.0 and later.

When you activate all the Hardware Asset Management solutions on your ServiceNow instance and opt-in all resource categories, consider the following:

-   A resource category is licensed only under one application based on the application priority that is defined in the HAM licensing framework.
-   The application priority is set based on the licensing cost and is in the following order:
    1.  Hardware Asset Management integration with Zero Touch Mobility
    2.  Hardware Asset Management integration with Telecommunications Network Inventory
    3.  Hardware Asset Management
-   Mobile Device is licensed under Hardware Asset Management integration with Zero Touch Mobility.
-   Telecom Network Inventory, Servers, and Network Gear are licensed under Hardware Asset Management integration with Telecommunications Network Inventory.
-   End User Computers is licensed under Hardware Asset Management.

|Resource category|Subscription Unit Ratio|HAM integration with Zero Touch Mobility|HAM integration with Telecommunications Network Inventory|Hardware Asset Management|Licensed under|
|-----------------|-----------------------|----------------------------------------|---------------------------------------------------------|-------------------------|--------------|
|Mobile|10:1|Installed|Resource category isn't available|Installed|Zero touch Mobility|
|Server|1:1|Resource category isn't available|Installed|Installed|Telecommunications Network Inventory|
|Network gear|5:1|Resource category isn't available|Installed|Installed|Telecommunications Network Inventory|
|Telecom Network Inventory|1:1|Resource category isn't available|Installed|Installed|Telecommunications Network Inventory|
|End User Computers|4:1|Resource category isn't available|Resource category isn't available|Installed|Hardware Asset Management|

You can view the subscription details of your Hardware Asset Management application and solutions using the ITAM License Report. For more details, see [View the license report for the Hardware Asset Management application](../task/view-license-report-ham.md).

## Exclusion of Operational Technology \(OT\) hardware assets from HAM licensing

The licensing model of the OT Asset Management \(OTAM\) application supports a few default hardware resource categories to license OT hardware assets. For more details on OT hardware assets, see [OT Asset Workspace](../../enterprise-asset-management/concept/ot-asset-ws-otam.md). These OTAM hardware resource categories have equivalent HAM licensing resource categories.

|HAM resource category|Equivalent OTAM hardware resource category|
|---------------------|------------------------------------------|
|Servers|OT Servers|
|Network Gear|OT Network Gear|
|Storage|OT Storage|
|End User Computers|OT End User Computers|
|Mobile Devices|OT Mobile Devices|
|Monitors|OT Monitors|
|Printers|OT Printers|
|Unclassified hardware|OT Unclassified Hardware|

When you activate all the Hardware Asset Management solutions along with the OT Asset Management application, and opt-in HAM resource categories, consider the following points:

-   Non-OT hardware assets, with the **OT entity** flag set to **false**, are licensed only under the resource categories of HAM licensing.
-   OT hardware assets, with the **OT entity** flag set to **true**, are licensed only under the hardware resource categories of the OT Asset Management application. For details, see [OT Asset Management licensing](../../enterprise-asset-management/concept/licensing-ot-asset-management.md).
-   HAM workflows support both OT hardware assets and non-OT hardware assets.
-   OT Asset Management workflows support only OT hardware assets.

**Parent Topic:**[Hardware Asset Management subscription](ham-subscription.md)

**Related topics**  


[Hardware Asset Management licensing](ham-licensing.md)

[Hardware Asset Management license exclusion](ham-license-exclusion.md)

[Hardware Asset Management integration with Zero Touch Mobility](ham-for-ztm.md)

[Telecommunications Network Inventory integration with Hardware Asset Management](https://www.servicenow.com/docs/access?context=integration-with-hardware-asset-management&version=yokohama&pubname=yokohama-telecom-network-inventory&ft:locale=en-US)

