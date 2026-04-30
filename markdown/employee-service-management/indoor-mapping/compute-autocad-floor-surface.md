---
title: Compute Autocad floor surface area
description: Compute floor size area and dimensions in Indoor Mapping Map Studio while importing your AutoCAD floor sources.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Compute Autocad floor surface area

Compute floor size area and dimensions in Indoor Mapping Map Studio while importing your AutoCAD floor sources.

## Before you begin

The computed floor size area measurements in Indoor Mapping are available in the Workplace Core Floor table form with pre-filled field values. For example, **Total Square feet**, **Usable Square feet**.

Role required: admin

## Procedure

1.  To compute the Floor size area from an AutoCAD file, activate the floor size computation property.

    1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Indoor Mapping Properties**.

    2.  Enable editing and set the property **Set true to activate floor size computation** to true.

    3.  Click **Save**.

2.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

3.  Select a campus for which you want to compute the floor surface area.

    For example: Demo Campus.

4.  Select a Building in the Map Studio.

5.  Select **Manage Workplace** &gt; **Floor &amp; Floorplans**.

6.  Select a floor plan and select **Configure**.

7.  In the AutoCAD source page, select the **Use for floor surface area calculation** from the list optionsx.

    The **Use for floor surface area calculation** option is only visible after you have enabled the floor size computation property as shown in Step 1.

    **Note:** It's optional and not mandatory to select a **Layer** while selecting the **Use for floor surface area calculation** option.

    ![AutoCAD source page showing floor surface area computation property.](../images/wsd-map-studio-compute-floor.png)

8.  Select a **Layer** that represents the outline of the floor to compute the floor surface area value.

    The layer for which **Use for floor surface area calculation** computation is selected is used for the floor surface area calculation.

    **Note:** Only one layer can be selected at a time. Ensure that the selected layer has closed polylines.

9.  Select **File Preview** to preview and verify if the polylines are closed for a selected layer.

    If in case, the selected Floor layer has several closed polylines, then the biggest polyline is used.

    1.  Select **Yes** from the drop-down list.

10. Select **Start Import** to import the CAD floor source plan.

    The computed floor surface area value is stored in the Floor configuration on the Map Studio.

11. Navigate to **All** &gt; **Space Mapping** &gt; **Properties Mapping**.

    This will push the computed floor surface area value from the Map Studio to the Workplace Core Floor table form.

12. On the Indoor Place Properties Mapping page, Click **New** and fill in the form fields:

    **Note:** This step needs to be only configured once.

<table id="table_abz_yyz_zyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property

</td><td>

Name of the property. For example:**CAD\_COMPUTED\_SURFACE\_SQ\_FEET** and **CAD\_COMPUTED\_SURFACE\_SQ\_METERS**. **Note:** Name of the property cannot be modified or edited. The property name must be same as what you have used in your AutoCAD file as a label.

</td></tr><tr><td>

WSD table

</td><td>

The table where you want to populate or place the property.Select **Floor** from the drop-down list to compute the floor surface area value in the Floor table.

</td></tr><tr><td>

WSD field

</td><td>

The field where you want the floor surface area to be auto-populated. Select **Total Square feet** or **Usable Square feet**.

</td></tr><tr><td>

Order

</td><td>

You can keep the order as 0.

</td></tr><tr><td>

Active

</td><td>

When this option is not selected, your property will be automatically deactivated on your different maps.Select this option to activate the property.

</td></tr><tr><td>

Domain

</td><td>

Default value is **Global**. Retain **Global** to avoid any conflicts between your different applications.

</td></tr></tbody>
</table>13. Click **Update**.

14. Navigate to **All** &gt; **Space Mapping** &gt; **Indoor Map/WSD Synhronizations** to run the Synchronization script to update the selected floor with the updated property.

15. Select a campus.

    The synchronization script syncs the newly added computed floor surface area fields on the Floor table.

16. Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration** &gt; **Floors**.

17. Select the Floor for which you computed the surface area value and verify the Measurement Details section.

    For example, the following field values will be pre-filled depending on user configuration:

    1.  **Total square feet**: The floor surface area value is auto-populated.

    2.  **Usable Square Feet**: The floor surface area value of the floor is auto-populated.

        **Note:** If the CAD values are incorrect or empty when you are importing the CAD file in the Map studio, it is most likely that the CAD file did not have a unit or may have an incorrect unit. In such cases, CAD file conversions in the Map Studio are not accurate.

        The CAD file unit value can be computed correctly in the Map Studio based on the AutoCAD file coordinates. Navigate back to the CAD file configuration page for a floor plan and perform the following;

        -   Select the More actions icon \(![more options icon.](../../wsd-for-mobile/images/more-options-icon.png)\) on the top right pane of the Map Studio.
        -   Select the **Edit file unit** option.

            ![CAD file edit unit option on the CAD configuration page.](../images/wsd-edit-file-unit-autocad.png)

        -   Select a unit from the drop-down list.

            For example; Feet.

        -   Click **Save**.
        -   Click **Start Import** and run the synchronization again.

            For more information, see [Synchronize Indoor Mapping with Workplace Service Delivery](synchronize-ind-mapping-wsd.md).

            The conversions are now accurate.


