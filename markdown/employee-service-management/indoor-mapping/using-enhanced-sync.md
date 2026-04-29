---
title: Using enhanced synchronization
description: Synchronize your workplace locations with your Indoor Mapping data by using the enhanced sync feature.
locale: en-US
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Using enhanced synchronization

Synchronize your workplace locations with your Indoor Mapping data by using the enhanced sync feature.

To use the enhanced sync feature, you must have completed the initial manual sync to link Indoor Mapping and WSD. You must have the sn\_wsd\_indoor\_map.admin role or the sn\_wsd\_core.workplace\_manager role to access the relevant modules.

**Warning:** Ensure that you have a one-to-one relationship between Space Types and Place Types for the bidirectional functionality to work.

To use the enhanced sync feature, see the following steps.

1.  Configure the Enhanced Sync properties to define the behavior of the sync operations between Indoor Mapping and Workplace Service Delivery.

    For more information about the Enhanced Sync properties, see [Enhanced Sync Properties](../reference/enhanced-sync-properties.md).

2.  Update data in Workplace Core.

    Updates to the location hierarchy objects in Workplace Core are synced to the Indoor Mapping objects based on the sync properties. These objects include the names and titles of Campuses, Buildings, Floors, and Spaces.

    The Place Type attribute is also updated in Indoor Mapping when the Space Type value for a Workplace Space is updated. When a Space in Workplace Core is deleted or changed to retired status, the related Indoor Mapping place is deactivated.

3.  Update data in Indoor Mapping Indoor Mapping.

    Updates to the location hierarchy objects in Indoor Mapping are synced to Workplace Core based on the sync properties. These objects include field values like the name and title.

    The Place Types are synced from Indoor Mapping places to Workplace Core. Objects are created in Workplace Core when they’re created in Indoor Mapping. For example, if an update to a CAD file introduces three new Indoor Mapping places, the three places are created as Workplace Spaces based on the sync properties.

    Place Properties are synced to the mapped fields in Workplace Core as configured in the Indoor Place Properties Mapping. For example, square feet \(SQ FT\) or square meters \(SQ M\) calculated from the CAD surface area information. When a Place in Indoor Mapping is deleted or its deactivated, the related Workplace Space is Retired.

4.  Review pending sync operations to process or ignore the operations.

    For more information about Enhanced Sync operations, see [Manage enhanced sync operations](../task/manage-sync-operations.md).

5.  Review the sync activities for information about the updates made to Indoor Mapping and Workplace Core as part of enhanced sync.

    You can view the sync activities by navigating to **All** &gt; **Workplace Core** &gt; **Enhanced Sync** &gt; **Enhanced Sync Activities**.

    The Enhanced Sync Activities list contains information about sync operations like the timestamp, the impacted table, and the workplace location.

6.  Review the sync error logs for informational messages, warnings, or errors.

    You can view the sync error logs by navigating to **All** &gt; **Workplace Core** &gt; **Enhanced Sync** &gt; **Enhanced Sync Error Logs**.


-   **[Manage enhanced sync operations](../task/manage-sync-operations.md)**  
Review pending sync operations and decide whether to process or ignore the operation.

**Parent Topic:**[Manage map objects and data](using-indoor-mapping.md)

**Previous topic:**[Synchronize Indoor Mapping map data with CMN location](../task/sync-ind-mapping-cmn-location.md)

**Next topic:**[Manage enhanced sync operations](../task/manage-sync-operations.md)

