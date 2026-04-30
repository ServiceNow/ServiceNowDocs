---
title: Track assets using indoor maps in the Enterprise Asset Workspace
description: Use indoor maps to locate and track the enterprise assets, consumable assets, and pallets that are deployed across your organization. Each indoor map consists of an interactive interface that enables you to visualize where your assets are located within your campuses, buildings, floors, and places.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Create and manage enterprise assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Track assets using indoor maps in the Enterprise Asset Workspace

Use indoor maps to locate and track the enterprise assets, consumable assets, and pallets that are deployed across your organization. Each indoor map consists of an interactive interface that enables you to visualize where your assets are located within your campuses, buildings, floors, and places.

## Before you begin

To use indoor maps in Enterprise Asset Workspace, fulfill the following requirements:

-   Explicitly install the Indoor Mapping for Assets \(com.sn\_ima\) application from the ServiceNow® Store. When you install this application, Indoor Mapping \(sn\_map\_core\) and Indoor Mapping component \(sn\_map\_component\) are also installed.

    If you purchased an Enterprise Asset Management license after November 3, 2023 using the updated Enterprise Asset Management SKU \(PROD21613\), you can install the Indoor Mapping for Assets \(com.sn\_ima\) application.

    **Note:** To be able to view demo data for indoor maps, you must reinstall demo data after you install the Indoor Mapping for Assets application. For more information, see [Add or repair demo data for applications and plugins](https://www.servicenow.com/docs/access?context=jny-dsgnr-install-repair-app-plugin&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

-   Set the **com.sn\_eam.indoormap.enabled** asset parameter to **true** on your ServiceNow instance.

-   Set up your indoor maps: You can design indoor maps using Map Studio. For more information, see [Configure Indoor Mapping](https://www.servicenow.com/docs/access?context=configure-ind-mapping&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).

    **Note:** When you install indoor maps using the entitlement to the Enterprise Asset Management license, you can use only the PNG floor map files in the Map Studio. You can’t import the files that are in AutoCAD or Raster file format. To use AutoCAD or Raster files, you should have entitlement to the Workplace Service Delivery application.

-   Configure the option to display the **Asset indoor map** tab in the Enterprise asset estate view of the Enterprise Asset Workspace. For detailed instructions, see [Configure tabs in the Enterprise Asset Workspace](configure-model-asset-class-tabs.md).

    **Note:** This tab appears only if the **Include in tab** option is enabled in the Asset indoor map tab configuration.

-   Synchronize location data: The Enterprise Asset Management application supports the following indoor mapping location types:

    -   Campus: Represents a set of buildings within the same geographic location.
    -   Building: Represents a multi-floor building within a specific campus.
    -   Floor: Represents a floor within a specific building.
    -   Place: Represents either a polygon or point of interest within a specific floor. Places can represent areas, rooms, desks, printers, assets, and more.
    **Note:** For indoor maps to show assets in the Enterprise Asset Workspace, assets should be assigned to a location of the type **place** or **room** in the Location \[cmn\_location\] table.

    To view the newly created locations within the Enterprise Asset Management application, make sure to synchronize the newly created locations from Map Studio to the Location \[cmn\_location\] table. You can associate the locations created in Map Studio with pre-existing records or new records in the Location \[cmn\_location\] table. For more information, see [Synchronize Indoor Mapping map data with CMN location](https://www.servicenow.com/docs/access?context=sync-ind-mapping-cmn-location&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US).


Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From the Enterprise Asset Workspace, open the Enterprise asset estate view.

2.  Select the **Asset indoor map** tab.

    This tab contains an interactive map that enables you to view the real-time location of each enterprise asset, consumable asset, and pallet within a specific floor or place.

3.  Set the map to a specific floor by using the Campuses, Buildings, and Floors filters.

    By default, the map provides a high-level view of all campuses that are available across your organization. This default map view doesn’t display the locations of your assets. To view the locations of your assets, you must set the map to the floor that those assets are located in. To set the map to a specific floor, select the appropriate values in the Campuses, Buildings, and Floors filters.

4.  Specify the assets that you want the map to display the locations of.

    By default, the map displays the locations of all enterprise assets, consumable assets, and pallets that are deployed across your organization. If you want the map to display the locations of only certain assets, use the following steps:

    1.  Select the Filters Tab icon \(![Filters Tab icon.](../image/filters-tab-icon.png)\) on the sidebar of the map.

    2.  In the Filter by window, use any of the following filters to narrow down the assets that you want to display the location of:

        -   **Department**: Department that the asset belongs to.
        -   **User**: User who the asset belongs to.
        -   **Model category**: Model category of the asset.
        -   **Classification**: Classification code that is assigned to the asset model.
5.  Change the format through which you view your asset locations by selecting a display option at the bottom-right corner of the **Asset indoor map** tab.

    The **Asset indoor map** tab supports the following display options:

    -   **Show map only** \(default display option\): Displays an interactive map that shows the locations of the assets within the specified floor.
    -   **Show list only**: Displays the list of assets that are located within the specified floor.
    -   **Show map and list**: Displays both the interactive map and the list of assets.
6.  Use the interactive map or the list of assets to view the real-time locations of assets within the specified floor or place in that floor.

    Select an asset from the map or list to view additional details about that asset.


**Parent Topic:**[Create and manage enterprise assets](../concept/create-manage-enterprise-assets.md)

