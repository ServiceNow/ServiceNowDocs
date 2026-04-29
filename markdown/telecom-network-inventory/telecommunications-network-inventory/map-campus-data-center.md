---
title: Map Indoor Mapping campus to a datacenter
description: Map an Indoor Mapping campus to a datacenter Configuration Item \(CI\) so you can view the datacenter's network infrastructure in the Telecommunications Network Inventory.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Floor map, Network visualization view, Use, Telecommunications Network Inventory]
---

# Map Indoor Mapping campus to a datacenter

Map an Indoor Mapping campus to a datacenter Configuration Item \(CI\) so you can view the datacenter's network infrastructure in the Telecommunications Network Inventory.

## Before you begin

-   Your campus record is created with building and floor details.
-   Your campus record name is the same as the datacenter record.
-   Make sure that you have configured Indoor Mapping campus with a floor plan and map objects. To learn more, see [Upload and manage floor map for your datacenter](create-floor-map-data-center.md).
-   Role required: sn\_ni\_core.dc\_ops\_agent

## About this task

After you create a Indoor Mapping campus record, you must map it to the datacenter Configuration Item \(CI\). Synchronize the campus with a location record, which is where the datacenter is located. Now you can open the campus in the floor map and view the datacenter infrastructure.

**Note:** If you use the same CMN location when creating the data center and campus, the campus will be automatically mapped to the CI.

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Campuses**.

2.  Open the campus record that you want to map to the datacenter CI.

3.  Select **Synchronize with CMN Locations**.

    The Indoor Map/CMN Location Synchronization form appears.

4.  Select the location record in the **CMN Location Campus** field.

    If you don't have a location record for your datacenter location, create one. Make sure to use the same location as the datacenter you want to map. To learn more about how to create location record, see [6910616cfeec459a9e107f2dc838f3f3b508f6ea.dita](define-tni-locations.md).

5.  Select **Update** to map the campus with the location record.

6.  Open the campus record that you want to map to the datacenter record.

7.  Select **Synchronize with CMN Locations**.

    The Indoor Map/CMN Location Synchronization form appears.

8.  Complete the synchronization steps.

    To learn more about the synchronization steps, see [Synchronize Indoor Mapping map data with CMN location](https://www.servicenow.com/docs/access?context=sync-ind-mapping-cmn-location&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).


## Result

The Indoor Mapping campus record including buildings, floors, places are mapped to the datacenter CI.

## What to do next

View the details of your datacenter infrastructure using the floor map. To learn more, see [View details of floor map](view-details-floor-map.md).

**Parent Topic:**[Floor map](../concept/using-floor-map.md)

**Related topics**  


[Synchronize Indoor Mapping with CMN Locations](https://www.servicenow.com/docs/access?context=sync-cmn-location&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)

[Floor map](../concept/visualization-floor-maps.md)

