---
title: Upload and manage floor map for your datacenter
description: Create, manage, and update your datacenter map objects in the Indoor Mapping Map Studio interface. You can view the datacenter's network infrastructure in Telecommunications Network Inventory application.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Floor map, Network visualization view, Use, Telecommunications Network Inventory]
---

# Upload and manage floor map for your datacenter

Create, manage, and update your datacenter map objects in the Indoor Mapping Map Studio interface. You can view the datacenter's network infrastructure in Telecommunications Network Inventory application.

## Before you begin

-   Make sure to install Indoor Mapping \(sn\_map\_core\) application.
-   Role required: sn\_ni\_core.dc\_floor\_designer

## About this task

With Indoor Mapping Map Studio, you can manage and edit map objects related to your datacenter infrastructure in one place. First, create a campus record with details about the building and floor. Then, upload a source image \(CAD file or raster image\) of the floor layout. With this layout, you can make architectural diagrams to show your datacenter facilities. You can define places using points or polygons. Link these places to place types like racks or transformers to categorize the network assets and different facilities.

Each place is marked with a title, making it easy to identify on the map. Once the campus record is created with building and floor details, you can map the campus with a datacenter using CMN location record. Then, you can map Configuration Items \(CIs\) to their corresponding places. Additionally, you can customize how operational data is displayed on the map, enabling real-time visualization of datacenter performance.

## Procedure

1.  Create a campus with buildings and floors.

    To learn more, see [Create a campus with buildings and floors](https://www.servicenow.com/docs/access?context=create-a-campus-building-and-floor&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

    **Note:** Make sure the campus and datacenter names that you want to map are the same.

2.  Use the boundary editor to map your campus on the global map.

    You can adjust the boundaries to show the location of your campus and buildings. Boundaries are used to differentiate between outdoor maps and indoor mapped areas. To learn more, see [Working with boundary editor](https://www.servicenow.com/docs/access?context=working-with-boundary-editor&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

3.  Upload your floor plan's CAD or raster file.

    You can use the floor plan to make configuration changes and preview the CAD design layout. To learn more, see [Import CAD files to Map Studio](https://www.servicenow.com/docs/access?context=CAD-file-import&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US). If you're uploading a raster file, then see [Import Raster files](https://www.servicenow.com/docs/access?context=import-raster-files&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more details.

4.  Import outdoor elements such as a logo or an outdoor cafeteria that you want to display on the indoor map.

    To learn more, see [Import outdoor elements](https://www.servicenow.com/docs/access?context=import-outdoor-elements&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

5.  Add places, icons, and place types to locate your network assets and facilities on a floor.

    To learn more, see [Manage places](https://www.servicenow.com/docs/access?context=manage-buildings&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).

    To create a place type, see [Create Indoor Mapping icons and place types](https://www.servicenow.com/docs/access?context=place-icons-place-type&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US). To learn about available place types, see [Data center place types](../reference/place-types-floor-map.md).

6.  Use the **Map Preview** to display maps and test directions that you have created.

7.  Export the updated CAD changes to your CAD file.

    Exporting the updated changes creates a copy of the modified CAD file in Indoor Mapping. To learn more about, see [Export CAD configuration](https://www.servicenow.com/docs/access?context=export-cad-config&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US).


## Result

A Indoor Mapping campus record is created with building and floor details.

## What to do next

After you create your Indoor Mapping campus record, do the following to view the datacenter infrastructure in floor map.

1.  [Map Indoor Mapping campus to a datacenter](map-campus-data-center.md)
2.  [Map a Configuration Item to a floor map](map-ci-floor-map-location.md)
3.  [Customize overlays on the floor map](customize-ovarlays-floor-map.md)
4.  [Customize overlay time series on the floor map](customize-overlay-time-series-floor-map.md)
5.  [View floor map details](view-details-floor-map.md)

**Parent Topic:**[Floor map](../concept/using-floor-map.md)

**Related topics**  


[Indoor Mapping](https://www.servicenow.com/docs/access?context=Indoor-mapping&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)

