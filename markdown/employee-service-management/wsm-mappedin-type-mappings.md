---
title: Maintain type mappings
description: Use Type mappings to convert the Type and Subtype locations in Mappedin to the Table and Space type used in Workplace Space Mapping.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Convert Mappedin data to Workplace Space Mapping data, Configure Mappedin, Configure, Workplace Space Mapping, Workplace Service Delivery, Employee Service Management]
---

# Maintain type mappings

Use **Type mappings** to convert the Type and Subtype locations in Mappedin to the Table and Space type used in Workplace Space Mapping.

## Before you begin

Role required: sn\_wsd\_mappedin.admin

**Important:** In the Workplace Service Delivery Suite, from Workplace Core version 2.5.3, the **Space type \(space\_type\)** choice field is depreciated. After the upgrade, Space types are configured in the **Space Type Configuration**. The **Space type \(space\_type\)** field is migrated as **Space type \(location\_type\)** field in the Space table \[sn\_wsd\_core\_space\]. Customers having customization on the depreciated **Space type \(space\_type\)** field are advised to manually migrate their flow to use the new **Space type \(location\_type\)** field. A new fix script, **Populate Location Type from Space Type**, is introduced to execute the schedule job, **Populate location\_type from space\_type**, on the Space table \[sn\_wsd\_core\_space\] to migrate the depreciated **Space type \(space\_type\)** field value to the new **Space type \(location\_type\)** field.

## Procedure

1.  Navigate to **All** &gt; **Space Mapping** &gt; **Mappedin Administration** &gt; **Type mappings**.

2.  Click **New** and complete the following:

<table id="table_l1l_1z1_3nb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Mappedin type

</td><td>

The Mappedin Location type.When a Mappedin map imports, the type is associated with the Space type.

 The base system provides Mappedin types and subtypes that are associated with Workplace Core Table and Space type.

</td></tr><tr><td>

Mappedin subtype

</td><td>

The Mappedin Location Amenities type.For example:

-   Women's washroom
-   Men's washroom


</td></tr><tr><td>

Table

</td><td>

The Space \(sn\_wsd\_core\_space\) table you want to import a Mappedin Location into.**Note:** The Location type and Subtype must match the Mappedin type and Mappedin subtype fields.

</td></tr><tr><td>

Space type

</td><td>

The space type you are associating a Mappedin location.**Note:** The Location type and subtype must match the Mappedin type and Mappedin subtype fields.

 The value in this field appears on the rendered map when an employee reserves a space.

</td></tr></tbody>
</table>3.  Click **Submit** or **Update**.


**Parent Topic:**[Convert Mappedin data to Workplace Space Mapping data](../concept/wsm-mappedin-type-table.md)

