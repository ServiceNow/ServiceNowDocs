---
title: Configure places
description: Configure Places using the Map Configuration preview layout. Retrieve place types from the CAD file.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Configure CAD objects using the Map Configuration tab, Autocad import tool, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Configure places

Configure Places using the Map Configuration preview layout. Retrieve place types from the CAD file.

## About this task

You can also configure shapes, names, and titles for a place type.

## Before you begin

Role required: admin

## Procedure

1.  Select the **Map Configuration** Tab.

    The Map Configuration preview page is brought into focus.

2.  Expand **Places** by selecting the chevron toggle icon \(![Expand Layers icon.](../images/wsd-chevron-up-icon.png)\).

3.  Select **Edit** to edit the place attributes and elements.

    The edit panel appears.

    ![Summary pill showing additional information for a selected place.](../images/wsd-places-expanded-view-autocad-v2.png)

    The selected place shows the number of elements in a place. For example: Breakout Room \(1 element\).

    The summary pills summarize information about your place configuration. For example, the summary pill shows if the place is a block or text, the place type is cafeteria or patio \(configuration information\).

    If you missed something in your configuration, the summary pills provide alerts \(highlighted in red\) like missing polyline, missing polygon.

    The summary pill summarizes information in the following colors based on the place configuration and place state:

    -   Neutral blue: Indicates the type of item selected. For example, text or blocks.
    -   Green: Indicates that the place configuration is correct for a selected place.
    -   Orange: Indicates minor configuration issues.
    -   Grey: Indicates layers that are not imported.
    -   Red: Indicates blocking errors.
4.  Select Import options \(**Import as a polygon**: Step 5 or **Import as Point**: Step 7\) to import the configuration to your CAD file.

    You can also select **Do not Import** if you do not want to import the configuration to your CAD file.

5.  Select **Import as polygon** to import a place as a polygon in your CAD file.

    ![Map configuration tab with the Import as polygon option selected.](../images/wsd-map-config-import-as-polygon.png)

    **Note:** The text appears in red on the Map Configuration preview when you select create as polygon and the shape is missing.

    1.  From the **Fetch polygons from this layer** list, select the layer that specifies where the shapes for these places are located on the map.

        If the shapes for meeting rooms are on the Meeting-Room layer, select Meeting-Room from the drop-down list.

    2.  In the **Name template** field, enter the name template that you want to use for the places.

        You can select the following options to be used from the CAD file:

        -   Select **TEXT** if you want the place name to be copied from the CAD file.

            If the place is defined a block in your CAD file, you can also select a block attribute for the Name template.

        -   Select **autocad\_entity\_handle** if you want to use a CAD-generated unique ID for a layer. Entity names and handles are unique within a CAD drawing.
    3.  Select **Blocks** if you have defined block attributes in your configuration.

        **Note:** Blocks are not available from Indoor Mapping version 1.13.0.

    4.  From the **Title text layer** list, select the layer that contains titles for the places.

        The current layer is selected by default.

    5.  In the **Title template** field, enter the title template that you want to use for the places.

        If this field is left empty, the name is used as Place type title.

        You can select **TEXT** or **autocad\_entity\_handle** to add it to the field.

        If the place is defined a block in your CAD file, you can also select a block attribute for the Title template.

6.  In **Retrieve place type from**, select the option to retrieve place types from the CAD file.

    You can select any of the following options to retrieve place types from the CAD file:

    -   **Place type catalog**: Select this option if you want to apply the default Indoor Mapping place type styles and categories to a place type. The place type catalog or the Place types table \(**All** &gt; **Indoor Mapping** &gt; **Place types**\) contains Indoor Mapping place types and their default styles. For more information, see [Create Indoor Mapping icons and place types](place-icons-place-type.md).
        -   **Place types**: Select an appropriate Indoor Mapping place type to style and categorize it. For example: Fire Extinguisher. Selected place type is displayed on the CAD editor preview.
        -   When Indoor Mapping Places are integrated with Workplace Service Delivery, the places are categorized as meeting room, fire extinguisher, and so on. Based on this categorization, you can also verify if the meeting rooms are reservable.

    -   **Block attributes**: Select this option if you want the retrieve the place type from the block attributes.

        **Note:** The Block attributes name contain the place type information. The place type name in a CAD file must be the same as the place type names in the Indoor Mapping Place type catalog. If the Block attributes name doesn't match with the Place type name in Indoor Mapping, create the place type, styles, and icons in Indoor Mapping Place types. For more information, see [Create Indoor Mapping icons and place types](place-icons-place-type.md).

        ![Retrieve place type from a block or text attributes.](../images/wsd-place-type-template-options.png)

        ![Block Reference edit panel showing the type of space and name attributes.](../images/wsd-block-attribute-reference.png)

    -   **Other layer**: Select this option if you want to apply place types from another layer.

        From the **Place Type Text Layer** list, select the layer that contains the place types for the locations on the map, then in the **Placetype template** field, enter the template that you want to use for the place types.

    -   **Manually set later**: If place types are set using the **Manually set later** option, the Map Configuration preview shows the place as an unknown place type.

        When a default place type that is set manually is selected on the CAD editor preview, the message “information isn’t available on a floor plan, set manually” is displayed.

        The place type is shown as Miscellaneous or unknown type in the Indoor Mapping Place types table \(**All** &gt; **Indoor Mapping** &gt; **Place types**\). The undefined place type is matched to a miscellaneous place type in the Place types table so that it isn’t ignored during the synchronization process.

        To assign place types manually, perform any of the following:

        -   Set the places manually using the CAD editor. Select the appropriate **Active layer**. Select places and add the place type information to the text or block attribute, if it exists.
        -   Navigate to Indoor Mapping Map Studio **Manage Workplace****Manage Places**. Multi-select places or select a place using a lasso or by using the Shift key option to select the required places. Select an appropriate **Place type** in the Place edit panel. For more information, see [Manage places](manage-buildings.md).

            ![Manually set places using Manage Places in Map Studio.](../images/wsd-manually-set-places-map-studio.png)

7.  Select **Import as point** to import a place as a point in your CAD file.

    **Note:** The text appears in red on the Map Configuration preview when you select create as point and the shape is missing.

    1.  Select the following options to configure place types:

    1.  **Name template**: Configure the name for your template.

        -   Select **TEXT** if you want the Text or name to be copied from the CAD file.

            The Map configuration preview shows the name on the map for a selected place.

        -   Select **autocad\_entity\_handle** to use a CAD generated unique ID. Entity names and handles are unique within a CAD drawing.
    2.  Select **Blocks** if you have defined block attributes in your configuration.

    3.  **Title template**: Select **TEXT** or **autocad\_entity\_handle** if you want the Text or name from Autocad to be used.

        **Note:** If this field is left empty, the name is used as the title \(See step 6 a\).

8.  In Retrieve Place type, select the following options:

    -   **Place type catalog**: Option to apply Indoor mapping default style to place types. The place type catalog or Place types table \(**All** &gt; **Indoor Mapping** &gt; **Place types**\) contains Indoor Mapping place types and default styles.
        -   **Place types**: Select an appropriate Indoor Mapping place type to style and categorize places. For example: Fire extinguishers.
        -   The selected place type is displayed on the CAD editor preview.

            ![CAD editor preview showing the retrieved place type from the place type catalog](../images/wsd-autocadv2-place-type-catalog.png)

    -   **Block attributes**: Select this option if you want the retrieve the place type from the block attributes.

        **Note:** The Block attributes name in a CAD file must be the same as the place type names in the Indoor Mapping Place type catalog. If the Block attributes name doesn't match with the Place type name in Indoor Mapping, make sure to first create the place type, styles, and icon in Indoor Mapping and then retrieve it.

    -   **Manually set later**: If Place types are set using the **Manually set later** option, the Map Configuration preview shows the place as an unknown place type.

        When a default place type that is set manually is selected on the CAD editor preview, the message “information isn’t available on a floor plan, set manually” is displayed.

        The place type is shown as Miscellaneous or unknown type in the Indoor Mapping Place types table \(**All** &gt; **Indoor Mapping** &gt; **Place types**\). The undefined place type is matched to a miscellaneous place type in the Place types table so that it isn’t ignored during the synchronization process.

        To assign place types manually, perform any of the following:

        -   Set the places manually using the CAD editor. Select the appropriate **Active layer**. Select places and add the place type information to the text or block attribute, if it exists.
        -   Navigate to Indoor Mapping Map Studio **Manage Workplace****Manage Places**. Multi-select places or select a place using a lasso or by using the Shift key option to select the required places. Select an appropriate **Place type** in the Place edit panel. For more information, see [Manage places](manage-buildings.md).

            ![Manually set places using Manage Places in Map Studio.](../images/wsd-manually-set-places-map-studio.png)

9.  Select the warning check boxes to display the warnings on the map.

    The check boxes are updated based on the changes made on the edit panel.

    ![Map configuration tab with warning check boxes selected and the warnings displayed on the map.](../images/wsd-map-studio-errors.png)

10. To resolve issues like a missing polygon, perform the following steps:

    -   From the Map Configuration preview, switch to the CAD Editor tab.

        For more information, see [Configure CAD objects using the CAD Editor tab](../concept/cad-editor-v2-ovw.md).

    -   Select the place on the CAD Editor preview and add a polygon or a missing line.
    -   Switch back to the Map configuration preview.

        Notice that the summary pill for the place shows the **Import as polygon** highlighted in green and the text is not highlighted in red. The style appears along with the polygon.


**Parent Topic:**[Configure CAD objects using the Map Configuration tab](../concept/manage-cad-map-config.md)

**Previous topic:**[Configure layers](wsd-edit-layers.md)

**Next topic:**[Configure CAD objects using the CAD Editor tab](../concept/cad-editor-v2-ovw.md)

