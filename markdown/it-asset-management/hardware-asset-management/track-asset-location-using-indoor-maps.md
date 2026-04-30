---
title: Track asset location using indoor maps
description: Locate and track the consumables and hardware, bundle, and pallet assets in your organization by using indoor maps. Indoor maps provide an interactive interface that enables you to visualize the location of your assets within your campuses, buildings, floors, and places.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Track asset location using indoor maps

Locate and track the consumables and hardware, bundle, and pallet assets in your organization by using indoor maps. Indoor maps provide an interactive interface that enables you to visualize the location of your assets within your campuses, buildings, floors, and places.

## Before you begin

To be able to use indoor maps in Hardware Asset Workspace, make sure you fulfill the following requirements:

-   You should explicitly install Indoor Mapping for Assets \(com.sn\_ima\) application from the ServiceNow® Store. When you install this application, Indoor Mapping \(sn\_map\_core\) and Indoor Mapping component \(sn\_map\_component\) are also installed.

    **Note:** To be able to view demo data for indoor maps, you must reinstall demo data after you install the Indoor Mapping for Assets application. For more information, see [Add or repair demo data for applications and plugins](https://www.servicenow.com/docs/access?context=jny-dsgnr-install-repair-app-plugin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

-   Set the **com.sn\_ham.indoormap.enabled** asset parameter to **true** on your ServiceNow instance.

-   Set up your indoor maps: You can design indoor maps using Map Studio. For more information, see [Configure Indoor Mapping](https://www.servicenow.com/docs/access?context=configure-ind-mapping&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

    **Note:** When you install indoor maps using the entitlement to the Hardware Asset Management license, you can use only the PNG floor map files in the Map Studio. You can’t import the files that are in AutoCAD or Raster file format. To use AutoCAD or Raster files, you should have entitlement to Workplace Service Delivery.

-   Synchronize location data: The Hardware Asset Management application supports the following indoor mapping location types:

    -   Campus: Represents a set of buildings within the same geographic location.
    -   Building: Represents a multi-floor building within a specific campus.
    -   Floor: Represents a floor within a specific building.
    -   Place: Represents either a polygon or point of interest within a specific floor. Places can represent areas, rooms, desks, printers, assets, and more.
    **Note:** For indoor map to show assets in Hardware Asset Workspace, assets should be assigned to a location of the type **place** or **room** in the Location \[cmn\_location\] table.

    To view the newly created locations within the Hardware Asset Management application, make sure to synchronize the newly created locations from Map Studio to the Location \[cmn\_location\] table.

    You can associate the locations created in Map Studio with pre-existing records or new records in the Location \[cmn\_location\] table. For more information, see [Synchronize Indoor Mapping map data with CMN location](https://www.servicenow.com/docs/access?context=sync-ind-mapping-cmn-location&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).


Role required: admin or asset

## Procedure

1.  Navigate to **All** &gt; **Hardware Asset Workspace** &gt; **Asset estate**.

2.  Select the **Asset indoor map** tab.

3.  View the assets on a selected floor by using the **Campuses**, **Buildings**, and **Floors** filters.

4.  Select a display option at the bottom-right corner of the Indoor map page to view the assets and their location on the selected floor in a particular format.

    -   To show the location of the assets on an interactive map, select **Show map only**.
    -   To display both the interactive map and a list view of the assets, select **Show map and list**.
    -   To display only a list view of the assets, select **Show list only**.
5.  If you’re viewing the interactive map, view the list of assets in a selected location on the floor by selecting a location on the map.

6.  View the location of assets based on a department, user, or model category or a combination of these values.

    1.  Select the Filters Tab icon on the contextual sidebar of the map.

    2.  Select the values for the **Department**, **User**, or **Model category** filters in the Filter by dialog box.


**Parent Topic:**[Using Hardware Asset Management](../concept/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization](../concept/Work-with-hardware-normalization.md)

[Manage asset bundles from your inventory](create-bundled-assets.md)

[Manage your inventory through pallet assets](../concept/pallets-for-inventory-management.md)

[Manage loaner assets](manage-loaner-asset.md)

[Donate assets to charity organizations](../concept/donate-asset-to-charity-organizations.md)

[Use Advanced Shipment Notification](advanced-shipment-notification.md)

[Manage RMA requests](../concept/manage-rma-req.md)

[Create an inventory stock order request](create-inventory-stock-order.md)

[Create a disposal order](create-disposal-order.md)

[Use a hardware asset request flow](hardware-request-flow.md)

[Audit hardware asset inventory](../concept/ham-inventory-audit.md)

[Request a Hardware Asset Refresh](hardware-asset-refresh.md#)

[Manage your expiring contracts for leased hardware assets](manage-your-leased-hw-asts-expiring-contract.md)

[Reclaim hardware assets](../concept/manage-asset-reclaim.md)

[View RFID information of assets](view-rfid-info.md)

[Manage the lifecycle of hardware models with calculated lifecycle templates](../concept/manage-ham-lifecycle-temp.md)

[Receive asset warranty details from Lenovo](../concept/receive-warranty-details-lenovo.md)

[Manage stockrooms](../concept/manage-your-stockrooms.md)

[Track shipments using the integration framework](../concept/tracking-shipments-using-integration-framework.md)

[Assess performance of Hardware Asset Management](../concept/suc-goal-act-hw.md)

[Manage refresh of assets using Zero Touch Refresh](../concept/refresh-hardware-uisng-ztr.md)

[Configure the Total Cost of Ownership of assets](../concept/configure-ham-tco.md)

[Manage and monitor hardware asset performance](../concept/manage-and-monitor-hardware-asset-performance.md)

[Manage Hardware Asset Management subscriptions](../concept/managing-ham-subscriptions.md)

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace](../concept/manage-repair-of-defective-ham-assets.md)

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows](../concept/manage-asset-picking-stockroom-ham-ws.md)

[Manage asset put away using the Hardware Asset Workspace](../concept/manage-asset-putaway-stockroom-hardware-asset-workspace.md)

[Manage hardware asset tasks using the Mobile Agent application](../concept/manage-hardware-asset-tasks-mobile-agent.md)

[Audit your hardware assets by using Asset Attestation](../concept/audit-hardware-assets-attestation.md)

[Acknowledge receipt of assets on the Employee Center portal](receive-assets-employee-center.md)

[Update associated Decision tables for HAM flows](trigger-flow-ham.md)

