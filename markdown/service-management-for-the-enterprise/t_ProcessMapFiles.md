---
title: Process GeoJSON map files
description: Processing GeoJSON map files includes parsing data from a map and importing that information to the campus space management tables. Use this process to set up your spaces or update bulk changes to your campus without having to enter each change manually.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [GeoJSON map files, Space management, Facilities Service Management overview, Facilities Service Management, Service Management]
---

# Process GeoJSON map files

Processing GeoJSON map files includes parsing data from a map and importing that information to the campus space management tables. Use this process to set up your spaces or update bulk changes to your campus without having to enter each change manually.

## Before you begin

Role required: facilities\_admin

## About this task

To process the files properly:

-   Include the area file in the map set and follow the proper naming convention \(`-area-geom-`\)
-   Set the **facilities.management.fvw.geojson.space.area.parsing** property to true

## Procedure

1.  Navigate to **All** &gt; **Space Management** &gt; **Campus**.

2.  Click the name of the campus.

3.  Click the **Facilities Map Sets** related list to see all the maps sets associated with this campus.

4.  Click the name of the map set you want to parse.

    All files associated with that map set are shown as attachments.

5.  Click **Process the Map Files** related link.

    All the files that will be read and parsed \(processed\) are shown.

6.  Click **Preview**.

    A summary of all the spaces that will be created are shown.

    |Field|Description|
    |-----|-----------|
    |Summary|The total for each space that will be added or retired: buildings, levels, spaces|
    |Facility space creation|
    |Feature type|All the types of spaces that will be created|
    |Class name| |
    |Creating|The total amount of each space type that will be created.|
    |Existing|The existing amount of each space type.|
    |Ignoring|The amount of each space type that not is created.|
    |Icon Creation|
    |Icon|The names of all icons that will be included within this campus.|
    |Parsing label|The parsing label of all icons that will be included within this campus.|
    |Creating|The total number of that icon type that will be created for this campus.|
    |Existing|The total number of that icon type that already exists within this campus.|

7.  Review the process map set summary carefully, to be sure if the space adds and ignores make sense.

    If the summary does not make sense, refer to the \[fm\_facility\_feature\] table.

8.  Click **Process**.

    A summary of all spaces created is displayed when the map file has been processed.


**Parent Topic:**[GeoJSON map files](../reference/r_GeoJSONMapFiles.md)

