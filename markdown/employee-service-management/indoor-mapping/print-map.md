---
title: Print a map
description: Print a map by configuring relevant options and applying filters.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-11-13"
reading_time_minutes: 3
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Print a map

Print a map by configuring relevant options and applying filters.

## About this task

You can print a map from one of the following applications.

-   Location directory
-   Workplace Central
    -   Building overview

## Before you begin

**Note:** Map printing is not supported on Mozilla Firefox.

Role required: sn\_map\_core.map\_printer

## Procedure

1.  Navigate to the map view in your app, then select **Print map**.

2.  On the Edit Map Content panel, configure the fields.

<table id="table_afx_3ws_ldc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Pin on map

</td><td>

Option to display a pin on the map.

</td></tr><tr><td>

Pin label

</td><td>

Label text for the pin on the map. This field is available only if **Show Pin on map** is selected.This field appears only if **Show Pin on map** is selected and the pin position is saved. You can change the label by selecting **Edit Pin** from the Edit Map Content panel.

</td></tr><tr><td>

Remove Outdoor Background

</td><td>

Option to remove the map area outside the selected building.

</td></tr></tbody>
</table>3.  Select a position on the map to place the pin, then select **Save Placement**.

    To place a pin on the map, the **Show Pin on map** field must be selected. You can change the position of the pin by selecting **Edit Pin** from the Edit Map Content panel.

4.  On the Edit Map page, select a space to customize the space settings.

<table id="table_blt_2xs_ldc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Space Text

</td><td>

Option to display the space label on the map.

</td></tr><tr><td>

Show Space Marker

</td><td>

Option to display the space icon on the map.

</td></tr><tr><td>

Order on Map

</td><td>

Order of the space text and marker on the map.-   Bring to Top: Space text and marker are moved to the top layer of the map.
-   Default: Space text and marker are on the default layer of the map.
-   Send to Back: Space text and marker are moved to the lowest layer of the map.


</td></tr><tr><td>

Space label text size

</td><td>

Size of the space label text on the map.

</td></tr></tbody>
</table>5.  Select **Continue** to open the print layout page.

6.  Select the paper size and orientation from the Print Layout panel.

    For more information about the options, see [Map printing options](../reference/map-printing-options.md).

7.  In the preview area, zoom and drag the map based on your requirement.

    You can use right-click to rotate the map.

8.  Configure the options in the Print Layout panel.

    For a description of the field values, see [Map printing options](../reference/map-printing-options.md).

9.  Select **Print**.


## Result

You can use your web browser to print the map or save it as a PDF.

-   If the aspect ratio of the map is not the same as your instance, verify that the layout settings \(like page size and orientation\) of the print dialog of your browser are the same as the settings on your instance.
-   If the map is shifted on the printed page, or the position of icons or the pin is not the same as your instance, set the margins in the print dialog of your browser to **None**.
-   The license text is automatically added to the outdoor map and is included in the printed map. To remove the license text, you must remove the outdoor map by using the **Remove Outdoor Background** option.

**Parent Topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Previous topic:**[Map preview](map-preview-indoor-mapping.md)

**Next topic:**[Create Snapshots to migrate Indoor Mapping data](snapshot-ind-mapping.md)

