---
title: Compute CAD file properties to extract space or room surface area
description: Extract room and space dimensions from CAD files or Indoor Mapping Map Studio. Use the extracted properties in Workplace Service Delivery \(WSD\) space measurement table.
locale: en-US
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Compute CAD file properties to extract space or room surface area

Extract room and space dimensions from CAD files or Indoor Mapping Map Studio. Use the extracted properties in Workplace Service Delivery \(WSD\) space measurement table.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Space Mapping** &gt; **Indoor Mapping Administration** &gt; **Properties Mapping**.

    By default, the following properties are stored in the Indoor Mapping Properties Mapping table:

    -   **CAD\_COMPUTED\_SURFACE\_SQ\_METERS**: If the polylines are defined as closed shapes or if a unit is set, compute the surface area automatically in square meters from the CAD polylines. By default, this property is set to **false**.
    -   **CAD\_COMPUTED\_SURFACE\_SQ\_FEET**: If the polylines are defined as closed shapes or if a unit is set, compute the surface area automatically in square feet from the CAD polylines. By default, this property is set to **false**.
    -   **INDOORMAP\_COMPUTED\_SURFACE\_SQ.\_FEET**: Retrieve the **usable\_size\_sq\_feet** from polygons in Indoor Mapping. Activate this property if your CAD file doesn’t have closed shapes or if a unit isn’t defined in the file. This property is also used for raster files \(PNG\). The scale in Indoor Mapping varies slightly depending on how the building was stretched during the georeferencing process. By default, this property is set to **true**.
    -   **INDOORMAP\_COMPUTED\_SURFACE\_SQ\_METERS**: Retrieve the **usable\_size\_sq\_meter** from a CAD file for a surface area from polygons in Indoor Mapping. Activate this property if your CAD file doesn’t have closed shapes or if a unit isn’t defined in the file. This property is also used for raster files \(PNG\). The scale in Indoor Mapping varies slightly depending on how much the building was stretched during the georeferencing process. By default, this property is set to **true**.

        After activating, these properties are applied automatically during the synchronization process to your Indoor Mapping maps. The properties populate the useable square meters or square feet field of the Workplace Core space table by default. The space table form fields can be modified as required.

        **Note:** Select a value from the computed AutoCAD file or select a value that is available in the Indoor Mapping Map studio.

2.  Select **New** to create a property.

    On the form, fill in the fields.

<table id="table_ypr_cp5_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property

</td><td>

Name of the property as it appears in the AutoCAD file. For example: **CAPACITY**. This name cannot be changed.

</td></tr><tr><td>

WSD Space column

</td><td>

Table that is used for mapping a CAD property to a WSD space column when the Indoor Mapping map data is synchronized with Workplace Service Delivery. Select any value from the drop-down list. For example: **Capacity**.

</td></tr><tr><td>

Order

</td><td>

Option to specify an import order for each record in the CAD properties mapping table. The ordering is useful when there are two properties that must be placed in the same WSD space columns for two different files.

</td></tr><tr><td>

Active

</td><td>

Option to make a property active.

</td></tr><tr><td>

Domain

</td><td>

Option for domain separation.

The default value is **global**.

</td></tr></tbody>
</table>3.  Select **Submit**.

4.  After importing the CAD source files, navigate to **Places** in the Map Studio menu.

5.  Select to open a place.

    The Places panel opens in the edit mode. Notice that **Autocad properties** field is available. For more information, see [Manage places](manage-buildings.md).

6.  Make sure to synchronize your campus after adding a CAD property.

    For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](synchronize-ind-mapping-wsd.md).

7.  Navigate to **All** &gt; **Workplace Core** &gt; **Campuses**.

    Add place properties mapping to a space in a campus if these properties aren’t added to a space.

8.  Select a Campus.

9.  Select the personalized list columns icon \(![Personalized list columns icon.](../../workplace-central/images/gear-icon.png)\) to move the required values from the Collection list to the available list.

10. Select **OK**.

11. Spaces available in a campus are updated with the selected values after a CAD file is imported in the Map Studio and after the Indoor Mapping synchronization process is complete.


