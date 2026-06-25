---
title: Track asset location using indoor maps
description: Locate and track the consumables and hardware, bundle, and pallet assets in your organization by using indoor maps. Indoor maps provide an interactive interface that enables you to visualize the location of your assets within your campuses, buildings, floors, and places.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/track-asset-location-using-indoor-maps.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
---

# Track asset location using indoor maps

Locate and track the consumables and hardware, bundle, and pallet assets in your organization by using indoor maps. Indoor maps provide an interactive interface that enables you to visualize the location of your assets within your campuses, buildings, floors, and places.

## Before you begin

To be able to use indoor maps in Hardware Asset Workspace, make sure you fulfill the following requirements:

-   You should explicitly install Indoor Mapping for Assets \(com.sn\_ima\) application from the ServiceNow® Store. When you install this application, Indoor Mapping \(sn\_map\_core\) and Indoor Mapping component \(sn\_map\_component\) are also installed.

    **Note:** To be able to view demo data for indoor maps, you must reinstall demo data after you install the Indoor Mapping for Assets application. For more information, see [Add or repair demo data for applications and plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/jny-dsgnr-install-repair-app-plugin.md).

-   Set the **com.sn\_ham.indoormap.enabled** asset parameter to **true** on your ServiceNow instance.

-   Set up your indoor maps: You can design indoor maps using Map Studio. For more information, see [Configure Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/configure-ind-mapping.md).

    **Note:** When you install indoor maps using the entitlement to the Hardware Asset Management license, you can use only the PNG floor map files in the Map Studio. You can’t import the files that are in AutoCAD or Raster file format. To use AutoCAD or Raster files, you should have entitlement to Workplace Service Delivery.

-   Synchronize location data: The Hardware Asset Management application supports the following indoor mapping location types:

    -   Campus: Represents a set of buildings within the same geographic location.
    -   Building: Represents a multi-floor building within a specific campus.
    -   Floor: Represents a floor within a specific building.
    -   Place: Represents either a polygon or point of interest within a specific floor. Places can represent areas, rooms, desks, printers, assets, and more.
    **Note:** For indoor map to show assets in Hardware Asset Workspace, assets should be assigned to a location of the type **place** or **room** in the Location \[cmn\_location\] table.

    To view the newly created locations within the Hardware Asset Management application, make sure to synchronize the newly created locations from Map Studio to the Location \[cmn\_location\] table.

    You can associate the locations created in Map Studio with pre-existing records or new records in the Location \[cmn\_location\] table. For more information, see [Synchronize Indoor Mapping map data with CMN location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/sync-ind-mapping-cmn-location.md).


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


**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Analyze hardware assets using the Generate hardware asset insights generative AI skill]()

[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create an inventory stock order request]()

[Create a disposal order]()

[Fulfilling hardware asset requests]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

