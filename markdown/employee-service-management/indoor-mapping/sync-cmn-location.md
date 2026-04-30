---
title: Synchronize Indoor Mapping with CMN Locations
description: Create a new CMN Location or synchronize an existing CMN Location with a corresponding Indoor Mapping Place type.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Synchronize Indoor Mapping with CMN Locations

Create a new CMN Location or synchronize an existing CMN Location with a corresponding Indoor Mapping Place type.

**Note:**

Synchronize CMN Locations with Indoor Mapping map data objects. Workplace Service Delivery is not installed in your instance in this case and you have CMN location types that you want to synchronize with Indoor Mapping.

**Note:** After installing Indoor Mapping and updating locations in the Map Studio, run the sync script to synchronize it with CMN locations and keep it up-to-date. The synchronization process must be performed every time a new place or location is updated in the Indoor Mapping Map Studio. For more information, see [Synchronize Indoor Mapping map data with CMN location](../task/sync-ind-mapping-cmn-location.md).

Ensure that your CMN Locations \(cmn\_location\) have the correct CMN Location types mapping to synchronize with Indoor Mapping campuses, buildings, floors, and places. For example, when you are synchronizing Indoor Mapping buildings, the sync script checks and ensures that the corresponding CMN location has the location type as Building/Structure. If the sync script is unable to find the appropriate CMN location type, then, it gives a suggestion for you to create a new building. Hence, mapping the CMN Locations with appropriate CMN Location types is required.

During the synchronization process all CMN Locations are renamed to match with location names in Indoor Mapping. For example, if your campus name in Indoor Mapping is Demo Campus. Then, the corresponding CMN Campus too will be renamed to Demo Campus in the CMN Location Table.

Consider the following to synchronize CMN locations with Indoor Mapping locations and map data:

1.  [Enable the CMN location property](../task/enable-cmn-sys-property.md)  
To synchronize CMN Location types with Indoor Mapping, enable the system property **sn\_map\_core.cmn\_location\_sync\_enabled**.
2.  [Add CMN locations and map it to Indoor Mapping Place types](../task/enable-cmn-location-types.md)  
CMN Locations types are not available by default in the Indoor Mapping Place types table. Associate or map an existing CMN Location type in your instance with a corresponding CMN Location Type column in the Indoor Mapping Place Types table. When CMN Location types are not available, create a CMN location type to associate it with a Indoor Mapping Place type.
3.  [Synchronize Indoor Mapping map data with CMN location](../task/sync-ind-mapping-cmn-location.md)  
Synchronize the CMN Locations and Location place types with Indoor Mapping map data, places, and place types.

**Parent Topic:**[Manage map objects and data](using-indoor-mapping.md)

**Previous topic:**[Synchronize Indoor Mapping with Workplace Service Delivery](../task/synchronize-ind-mapping-wsd.md)

**Next topic:**[Enable the CMN location property](../task/enable-cmn-sys-property.md)

