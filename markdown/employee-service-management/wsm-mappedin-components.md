---
title: Components installed with Workplace Space Mapping
description: Several types of components are installed with Workplace Space Mapping, including tables and user roles.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Workplace Space Mapping reference, Workplace Service Delivery, Employee Service Management]
---

# Components installed with Workplace Space Mapping

Several types of components are installed with Workplace Space Mapping, including tables and user roles.

## Roles installed with Workplace Space Mapping

<table id="table_otr_ffn_5nb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Workplace Space Mapping admin \[sn\_wsd\_space\_map.admin\]

</td><td>

As a system admin, you can do the following:-   Access the application completely.
-   Create, manage, and edit a Connection configuration.
-   Establish OAuth credentials.
-   Create, manage, and edit Calendar providers.

 As a Workplace Space Mapping space map admin, you can do the following:

-   Create, manage, and edit floor maps from Mappedin.
-   Manage map properties and customize the map legend.

</td><td>

sn\_wsd\_mappedin.admin

</td></tr><tr><td>

Workplace Service Delivery Mappedin admin \[sn\_wsd\_mappedin.admin\]

</td><td>

Create, manage, and edit floor maps from Mappedin.

</td><td>

-   flow\_operator
-   import\_admin
-   web\_service\_admin

</td></tr><tr><td>

Indoor Mapping administratorsn\_wsd\_indoor\_map.admin

</td><td>

-   Sets up the Indoor Mapping map data and objects in the Workplace Indoor Mapping map studio.
-   Has complete access to the application.

</td><td>

user\_criteria\_adminCan manage the User Criteria records.

</td></tr></tbody>
</table>## Tables Installed with Workplace Indoor Mapping

<table id="table_vxm_frg_3tb"><thead><tr><th>

Table Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indoor Place Type Mapping\(sn\_wsd\_indoor\_map\_place\_type\_mapping\)

</td><td>

Indoor Mapping place and place types are mapped to Workplace Service Delivery places and space types.

</td></tr><tr><td>

Indoor Map / WSD Floors Synchronizationsn\_wsd\_indoor\_map\_floor\_sync

</td><td>

Synchronizes Indoor Mapping floors with Workplace Service Delivery floors.

</td></tr><tr><td>

Indoor Map / WSD Types Synchronizationsn\_wsd\_indoor\_map\_type\_sync

</td><td>

Synchronizes Indoor Mapping Types with Workplace Service Delivery Types. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr><tr><td>

Indoor Map / WSD Cleaningsn\_wsd\_indoor\_map\_clean\_sync

</td><td>

If Indoor Mapping map objects or map data is removed from a campus, the Cleaning process is available as a first step in the Synchronization process. For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](../../wsd-indoor-mapping/task/synchronize-ind-mapping-wsd.md).

</td></tr></tbody>
</table>**Parent Topic:**[Workplace Space Mapping reference](../concept/wsm-reference.md)

**Related topics**  


[Properties installed with Workplace Space Mapping](wsd-space-mapping-properties.md)

