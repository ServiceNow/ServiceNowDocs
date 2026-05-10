---
title: Indoor maps in Enterprise Asset Management
description: Indoor mapping provides granular location tracking to visualize asset location on a floor map.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 3
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Indoor maps in Enterprise Asset Management

Indoor mapping provides granular location tracking to visualize asset location on a floor map.

Each indoor map consists of an interactive interface that enables you to visualize where your assets are located within your campuses, buildings, floors, and places.

You can access the indoor map from the **Asset indoor map** tab in the Enterprise asset estate view of the Enterprise Asset Workspace. You can also view indoor mapping data for a specific asset from the corresponding asset record, stockroom record, or work order task.

## Location hierarchy

|Location type|Description|
|-------------|-----------|
|Campus|Represents a set of buildings within the same geographic location.|
|Building|Represents a multi-floor building within a specific campus.|
|Floor|Represents a floor within a specific building.|
|Place|Represents either a polygon or point of interest within a specific floor. Places can represent areas, rooms, desks, printers, assets, and more.|

## Key capabilities

-   View the granular location of each asset within a specific floor or place.
-   Filter the map or search for assets based on department, user, model category, and classification code.
-   Track enterprise assets, consumable assets, and pallets from a single interface.
-   Access real-time space utilization visualizations alongside asset location data.

## Requirements

To use indoor maps in the Enterprise Asset Workspace, fulfill the following requirements:

1.  Explicitly install the Indoor Mapping for Assets \(com.sn\_ima\) application from the ServiceNow Store. When you install this application, Indoor Mapping \(sn\_map\_core\) and Indoor Mapping component \(sn\_map\_component\) are also installed.

    **Note:** If you purchased an Enterprise Asset Management license after November 3, 2023 using the updated Enterprise Asset Management SKU \(PROD21613\), you can install the Indoor Mapping for Assets \(com.sn\_ima\) application.

2.  Set the **com.sn\_eam.indoormap.enabled** asset parameter to **true** on your ServiceNow instance.
3.  Set up your indoor maps using Map Studio.

    For more information, see [Configure Indoor Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/indoor-mapping/configure-ind-mapping.md).

    **Note:** When you install indoor maps using the entitlement to the Enterprise Asset Management license, you can use only PNG floor map files in Map Studio. You cannot import files in AutoCAD or Raster file format. To use AutoCAD or Raster files, you must have entitlement to the Workplace Service Delivery application.

4.  Configure the option to display the **Asset indoor map** tab in the Enterprise asset estate view of the Enterprise Asset Workspace.

    For detailed instructions, see [Configure tabs in the Enterprise Asset Workspace](../task/configure-model-asset-class-tabs.md).

    **Note:** This tab appears only if the **Include in tab** option is enabled in the Asset indoor map tab configuration.

5.  Synchronize location data.

    **Note:** For indoor maps to show assets in the Enterprise Asset Workspace, assets must be assigned to a location of the type **place** or **room** in the Location \[cmn\_location\] table. To view newly created locations within the Enterprise Asset Management application, synchronize the locations from Map Studio to the Location \[cmn\_location\] table. You can associate the locations created in Map Studio with pre-existing records or new records in the Location \[cmn\_location\] table. For more information, see [Synchronize Indoor Mapping map data with CMN location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/indoor-mapping/sync-ind-mapping-cmn-location.md).


For more details on using indoor maps, see [Track assets using indoor maps in the Enterprise Asset Workspace](../task/track-enterprise-assets-indoor-maps.md).

