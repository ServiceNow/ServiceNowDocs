---
title: Print a floor map
description: Print the entire canvas of the floor map based on your map selection in the Telecommunications Network Inventory application. You can use it as a reference to view the floor map details.
locale: en-US
release: australia
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Floor map, Network visualization view, Use, Telecommunications Network Inventory]
---

# Print a floor map

Print the entire canvas of the floor map based on your map selection in the Telecommunications Network Inventory application. You can use it as a reference to view the floor map details.

## Before you begin

Role required: sn\_ni\_core.dc\_ops\_agent

## About this task

You can print the floor map by configuring relevant options and applying filters and save the copy to your local system.

## Procedure

1.  Navigate to **Workspaces** &gt; **Network Inventory Workspace**.

2.  Select the blue hub icon ![Blue Hub Icon.](../image/icon-blue-hub.png).

    The Network viewer window is displayed.

3.  Select the **Floor map** tab.

4.  Apply filters and select your floor.

5.  Select the print icon \(![Print Icon.](../image/icon-print-floor-map.png)\).

6.  On the map pane, select the download icon \(![Download Icon](../image/icon-download.png)\).

7.  On the Edit Map Content panel, configure the fields.

    |Field|Description|
    |-----|-----------|
    |Show Pin on map|Option to display a pin on the map.|
    |Remove Outdoor Background|Option to remove the map area outside the selected building.|

8.  Select a place to customize the place settings.

<table id="table_blt_2xs_ldc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show Space Text

</td><td>

Option to display the place label on the map.

</td></tr><tr><td>

Show Space Marker

</td><td>

Option to display the place icon on the map.

</td></tr><tr><td>

Order on Map

</td><td>

Order of the place text and marker on the map.-   Bring to Top: Place text and marker are moved to the top layer of the map.
-   Default: Place text and marker are on the default layer of the map.
-   Send to Back: Place text and marker are moved to the lowest layer of the map.


</td></tr><tr><td>

Space label text size

</td><td>

Size of the place label text on the map.

</td></tr></tbody>
</table>9.  Select **Continue** to open the print layout page.

10. Select the paper size and orientation from the Print Layout panel.

    For more information about the options, see Map printing options.

11. In the preview area, zoom and drag the map based on your requirement.

    You can use select and hold \(or right-click\) to rotate the map.

12. Configure the options in the Print Layout panel.

    For a description of the field values, see Map printing options.

13. Select **Print**.


## Result

You can use your web browser to print the map or save it as a PDF.

-   If the aspect ratio of the map is not the same as your instance, verify that the layout settings \(like page size and orientation\) of the print dialog of your browser are the same as the settings on your instance.
-   If the map is shifted on the printed page, or the position of icons or the pin isn’t the same as your instance, set the margins in the print dialog of your browser to **None**.

**Parent Topic:**[Floor map](../concept/using-floor-map.md)

