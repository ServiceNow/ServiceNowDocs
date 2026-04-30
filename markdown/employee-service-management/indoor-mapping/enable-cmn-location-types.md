---
title: Add CMN locations and map it to Indoor Mapping Place types
description: CMN Locations types are not available by default in the Indoor Mapping Place types table. Associate or map an existing CMN Location type in your instance with a corresponding CMN Location Type column in the Indoor Mapping Place Types table. When CMN Location types are not available, create a CMN location type to associate it with a Indoor Mapping Place type.
locale: en-US
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Synchronize Indoor Mapping with CMN Locations, Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Add CMN locations and map it to Indoor Mapping Place types

CMN Locations types are not available by default in the Indoor Mapping Place types table. Associate or map an existing CMN Location type in your instance with a corresponding CMN Location Type column in the Indoor Mapping Place Types table. When CMN Location types are not available, create a CMN location type to associate it with a Indoor Mapping Place type.

## Before you begin

Synchronization utility looks for a corresponding CMN location type and synchronizes it with a Indoor Mapping place type. For example: Indoor Mapping Place type **Desks** is mapped with CMN Location type **Desks**.

**Note:** In case of Indoor Mapping, all map objects like campus, building, floor, and Places have separate tables. But in case of CMN location, there’s only one table for Campus, buildings, floors and Location place types. The Parent column in CMN location table contains the hierarchy of campus, buildings, floors and so on. All map objects in the CMN location table have a parent location column and a child location according to which the locations are created in the Locations table \[cmn\_location\].

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Tables**.

2.  Select or search for the **Locations** \(cmn\_location\) table.

3.  In the Columns related list, select **Location type**.

    The Location type table is displayed.

4.  Add a location in the Location type table for a CMN location.

    The locations types are used in the CMN Location type column of Indoor Mapping Place types table. This is a mandatory step as CMN location types are not available by default in the Indoor Mapping Place types table.

5.  Click the **Choices** column to create corresponding Indoor Mapping Place types in the CMN location table.

    For example, Place types of Desks, Meeting rooms and so on.

    ![CMN location type table with the Choices column.](../images/wsd-location-type-table-choices-list.png)

6.  Select the **Inset a row option** in the **Label** column and add a CMN location place type \(for example, Desks\).

7.  Make inline edits and save the record.

8.  To map the CMN location types \(places, see step 6\) with Indoor Mapping Place Types, change the Application scope to Global.

9.  Select **Indoor Mapping**.

    ![Application scope changed to Indoor MMapping.](49ec0ad285c956a256c8114a498a847345c26828.png)

10. Navigate to the **All** &gt; **Indoor Mapping** &gt; **Place types** table.

11. Select the personalize list icon \(![Personalized list icon.](../images/wsd-personalize-gear-icon.png)\) and move **Location type** to the Selected list column.

12. Double click any row to make inline edits in the Location Type \(cmn\_location\_type\) column and add a CMN location to match corresponding Indoor Mapping place types.

    For example, add place types of **Desks**.

    **Note:** The place type \(Desks\) was added in the CMN locations table \(cmn\_locations\) Choices column in step 6.

    ![Adding CMN location type to the Indoor Mapping Place types table.](../images/wsd-cmn-location-type-add.png)

13. Save the record after making inline edits.

    This step should be done manually every time you want to add a corresponding Indoor Mapping place types and map it with a CMN location place types. The synchronization script maps the CMN locations with relevant Indoor Mapping places. If the CMN location types are not added, the synchronization script shows the **CMN Location Type** column as empty as it is unable to find a corresponding CMN location place type for Indoor Mapping places.

    ![Indoor Map and CMN Location Synchronization script showing the CMN Location Place Type column with CMN location place types](../images/wsd-cmn-location-type-sync.png)

    **Note:** Indoor Mapping Outdoor places \(for example, cafeteria, park, and so on\) are linked directly to a campus and not to a floor. While synchronizing the CMN locations, the outdoor places are also synchronized.


## Result

The CMN location types are added and ready to be mapped with corresponding Indoor Mapping places.

**Parent Topic:**[Synchronize Indoor Mapping with CMN Locations](../concept/sync-cmn-location.md)

**Previous topic:**[Enable the CMN location property](enable-cmn-sys-property.md)

**Next topic:**[Synchronize Indoor Mapping map data with CMN location](sync-ind-mapping-cmn-location.md)

