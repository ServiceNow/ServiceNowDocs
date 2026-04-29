---
title: Import CAD files to Map Studio
description: Create a campus, add few buildings and floors to the campus. Upload your CAD floor plan to make configuration changes and preview the CAD design layout.
locale: en-US
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Autocad tool, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Import CAD files to Map Studio

Create a campus, add few buildings and floors to the campus. Upload your CAD floor plan to make configuration changes and preview the CAD design layout.

## Before you begin

After making the required place type and file unit size changes, import it to the Map Studio to complete your building configuration. View the updated changes to places and place types in the Map studio \(**Manage Workplace** &gt; **Places**\).

Role required: map editor, map admin, map editor limited

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

2.  Create a Campus, add few buildings and floors to a campus or select an existing campus.

    For more information, see [Create a campus with buildings and floors](create-a-campus-building-and-floor.md)

3.  Navigate to **Manage workplace** &gt; **Floors and Floor plans**.

4.  If you want to add a floor, select **Add a floor** option.

5.  Select **Upload** to upload the CAD source file.

    For example: demo.dwf

6.  Complete the following information:

    1.  **File**: Name of the CAD source file.

        By default, the name of the source is the &lt;campus name-floor title-file name&gt;. For example, Lawson-B12.dwg

    2.  **Name**: Campus name.

7.  Click **Save**.

    A message with a clickable link to review the [AutoCAD guidelines](https://www.servicenow.com/community/wsd-blog/cad-file-guidelines-for-indoor-mapping/ba-p/2266775) is displayed.

    Review the guidelines before uploading the CAD file.

8.  Upload process may take sometime to complete depending on the CAD file size.

9.  After the upload process is complete, select **Configure**.

    In case of large files, the configuration process may take some time to complete.

10. The AutoCAD source page displays the following options:

    ![Autocad v1 configuration page.](../images/wsd-old-cad-preview-page.png)

    -   Georeference: Option to edit position and adust the location pins for a location.
    -   Layers: Option to configure layer types that you want to display on the global map.
    -   Places: Option to configure places that you want to display on the global map.
    -   Configuration preview: CAD file configuration preview.
    -   File preview: After making the required changes to Layers and Places, preview your changes on the Configuration preview layout.
11. Select **Edit georeference** to move the location pins and position the floor on the global map \(OpenStreetMap\).

    If location pins are not positioned, warning message **Not Configured yet** is shown.

    on the form, fill in the fields

    |Field|Description|
    |-----|-----------|
    |Display|From the drop-down option, select a floor or floors in a building. Enable the toggle option to display buildings and floors on the map. Drag and move around to position the location pins as required.|
    |Align with other sources|Select the campus or map objects from the list. Select **Align** to align your floor plan with the shape and size of a building on the global map.|

    1.  Click **Save**.

12. To preview the CAD file, select the following options:

    1.  **To be imported**: Dynamic preview will change based on the selections that you make.

    2.  **Uploaded**: Shows the preview for the uploaded CAD source file.

13. Select the required layers from the **Layers** section that you want to display on the map.

    A warning message is displayed if there are too many layers on your CAD source file. Select only the required layers.

14. To visualize CAD elements within each layer, select the **Make map full width** option.

15. Configure place type configuration using the **Places** section.

16. Select the Places from the list that you want to display on the map.

    On the form fill in the field

    |Field|Description|
    |-----|-----------|
    |Use polygon from layer|Layer on which the place shapes are located.|
    |Title template|Required title template from the list of available templates.|
    |Place Type|Place type to categorize the place type on the map. For example: Auditorium.|

17. Repeat the steps for places that you want to import and display on the map in the Map Studio.

18. Although the CAD import requirements state that polylines need to form closed shapes in order to create polygons, if some polylines are not properly closed in the file, Indoor Mapping offers a property to automatically close these shapes.

19. Enter the maximum distance between two points on the map and the system will close the points.

20. If there is a small disconnect between the first and last point, you can correct this by modifying the sys\_property automatically converting lines to polygon while importing a CAD file.

    1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Indoor Mapping properties**.

    2.  Search for **sn\_map\_core.line\_to\_polygon\_max\_distance**

        This property indicates the maximum distance in centimeters between the first and last point to convert a line to a polygon while importing an AutoCAD file.

    3.  Provide a value to this property within a range 1-100.

        For example: Set the sn\_map\_core.line\_to\_polygon\_max\_distance to 15.

    4.  Import the CAD file again and confirm that both the places are converted to Polygon now.

21. Select **Start Import**.

22. After import is complete, select **Manage Workplace** and select **Overview**.

23. Click on the building that you created.

    Your map is now available on the Map Studio with the CAD changes.

24. On the CAD configuration page menu, select the following options, as required:

    -   **Upload new file** to upload a new floor plan.
    -   **Download file** to download the CAD file.
    -   **Make a map full width** to view the CAD file in full mode.
25. Select the More actions menu icon \(![More actions menu icon.](../../legal-request-management/image/more-actions-icon.png)\):

    -   Edit name: Option to edit the CAD source name. Select **Save** after you update the name.
    -   Edit floor: Option to edit source floor. Select **Save** after updating the floor name.
    -   Edit file encoding: Option to edit source file encoding. Select a standard encoding format for your file. Select **Save and upload**.
    -   Edit file unit: Option to edit the CAD file unit. For example: Inches, feet, centimeters, and so on.
    -   Use new AutoCAD tool: Option to switch and navigate to the new Autocad processor configuration page to manage, edit, and optimize the layers, places, and objects in your CAD file.
    -   Delete: Option to delete the CAD source file.
    The CAD file is loaded into the Map Studio and the configuration for layers, layer types, and places is created. The application automatically applies the same configurations to subsequent floors that are imported. This is helpful in speeding up configurations of buildings that have multiple floors and where all the CAD files have similar layers. If the CAD layers within the subsequent files have the same layer names as the layers within the initial file, then layers, layer types, and places is pre-filled with the same values as those in the initial file.


**Parent Topic:**[Autocad tool](../concept/autocad-processor-v1.md)

**Previous topic:**[Autocad tool](../concept/autocad-processor-v1.md)

**Next topic:**[Indoor Mapping references](../concept/indoor-mapping-references.md)

