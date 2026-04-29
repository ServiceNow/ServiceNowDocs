---
title: Hardware Asset Management integration with Zero Touch Mobility
description: ServiceNow Hardware Asset Management is integrated with Samsung SDS Zero Touch Mobility to manage the complete life-cycle of mobile devices.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [HAM integrations, Hardware Asset Management, IT Asset Management]
---

# Hardware Asset Management integration with Zero Touch Mobility

ServiceNow® Hardware Asset Management is integrated with Samsung SDS Zero Touch Mobility to manage the complete life-cycle of mobile devices.

The benefits of Hardware Asset Management integration with Zero Touch Mobility are as follows:

-   Deploy, manage, and monitor mobile assets on a single platform leveraging automated workflows for day-to-day mobile device management tasks like the following:
    -   Onboarding new devices
    -   Unenrolling devices
    -   Requesting new orders, upgrades, or replacements with self-service options
-   Manage and report on the mobile device life-cycle with an integrated solution that improves visibility and collaboration across the organization.
-   Optimize costs and utilization of all your mobile devices.

## Requirements and limitations

Requirements and limitations for Hardware Asset Management integration with Zero Touch Mobility solution are as follows:

-   The solution is dependent on the Hardware Asset Management \(sn\_hamp\) application.
-   Only the Mobile Device resource category is available. This resource category is opted-in automatically.

    Based on the acquisition method of assets, the following resource subcategories are available for the Mobile Device:

    -   Bring Your Own Asset
    -   Corporate Asset
-   Only mobile devices are licensed under this solution. You can view the subscription details using the ITAM license report. For more information, see [View the license report for the Hardware Asset Management application](../task/view-license-report-ham.md).

    **Note:** Even if Hardware Asset Management is activated explicitly on your ServiceNow instance, the mobile devices are licensed only under the Mobile Device resource category of the Hardware Asset Management integration with Zero Touch Mobility solution. For more information, see [Licensing framework for Hardware Asset Management solutions](licensing-ham-solutions.md).

-   The following Hardware Asset Management features aren't available:

    -   Hardware Model Normalization
    -   Content upload and download
    -   Performance Analytics Dashboard
    -   Asset Executive Dashboard
    -   Success Portal
    **Note:** HAM Guided Setup is available. However, it isn't required to run the setup.

    For more information on the Hardware Asset Management workflows and features, see [Hardware Asset Management subscription](ham-subscription.md).


## Supported Hardware Asset Management features

The following Hardware Asset Management features are available without any restrictions:

-   [Stock order](../task/create-inventory-stock-order.md)
-   [Advanced Shipment Notification](../task/advanced-shipment-notification.md)
-   [Standard Asset Request flow](../task/hardware-request-flow.md)
-   [Shipment carrier integration](integrating-with-third-party-carrier-apps.md)
-   [Advanced inventory and distribution](../task/associate-stockroom-with-distribution-channels.md)
-   [Asset reclamation](reclaim-asset.md#)

The following Hardware Asset Management features have limited availability:

-   HAM workflows: Non-mobile devices are excluded from the HAM workflows.
-   [Lease expiration flow](../task/manage-your-leased-hw-asts-expiring-contract.md): Non-mobile devices are excluded from this flow.
-   [Hardware Asset Workspace](using-ham-workspace.md): Reports and dashboards related to normalization of assets aren't available.

**Parent Topic:**[Hardware Asset Management integrations](ham-integrations.md)

**Related topics**  


[Exploring Hardware Asset Management](exploring-ham.md)

