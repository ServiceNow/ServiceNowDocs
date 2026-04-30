---
title: Configure layers
description: Select a layer on the Map Configuration preview and edit it.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure CAD objects using the Map Configuration tab, AutoCAD import tool, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Configure layers

Select a layer on the Map Configuration preview and edit it.

## Before you begin

Layers are the shapes or geometries in your CAD file.

Role required: admin

## Procedure

1.  Select the **Map Configuration** Tab.

    The Map Configuration preview page is brought into focus.

2.  Expand **Layers** by selecting the chevron toggle icon \(![Expand Layers icon.](../images/wsd-chevron-up-icon.png)\).

3.  Select **Layers** to select a layer.

4.  Select **Edit**.

    The edit panel appears.

    **Note:** **Use for floor surface area calculation** option is not available for selection after it’s enabled for a layer. For more information, see [Compute Autocad floor surface area](compute-autocad-floor-surface.md).

    ![Layer summary pill showing configuration information for a selected layer type.](../images/wsd-layers-expanded-autocadv2.png)

    The selected layer shows the layer name along with the number of elements in it. For example: Logo \(1442 elements\)

    The summary pill shows summarized information for a layer configuration. The summary pill summarizes information in the following colors based on the layer configuration and layer state:

    -   Neutral blue: Indicates the type of item selected. For example, Text or Block.
    -   Green: Indicates that the place configuration is correct for a selected place.
    -   Orange: Indicates minor configuration issues.
    -   Grey: Indicates layers that are not imported.
    -   Red: Indicates blocking errors.
5.  Select **Import** to import the elements in a layer on your CAD file.

    A validation message is displayed: Configuration saved successfully

6.  Select **Do not Import** when you don’t want to import a layer configuration to your CAD file.

    A validation message is displayed: Configuration saved successfully

    The selected layer elements are displayed on the Map configuration preview panel based on your selection.

    ![Selected layer type shown on the map preview.](../images/wsd-layer-elements-in-map-preview.png)

7.  Resolve a missing layer type \(highlighted in red in the summary pill\) by selecting a layer type from the **Select layer type** options.

    ![Summary pill showing the missing layer type information and the preview for the missing layer.](../images/wsd-missing-layer-type-map-config-page.png)

    The missing layer type is resolved and the summary pill shows the Layer type highlighted in green. The Map Configuration preview shows the missing layer type with the newly assigned layer type.

    **Note:** Layer types render on a map with default styles. If layer type is missing, elements will appear with a red default style.

    Layer type categorizes and applies a style to a layer from the Indoor mapping Layer types table \(**All** &gt; **Indoor Mapping** &gt; **Layer Types**\)

8.  To change a layer type from the current type to another, select the **Select the Layer type** option.

    For example, if your current Layer type is **Room** and you select **Building** from the list to change a layer type. The newly selected layer type along with its style and categories are applied.

9.  After making the changes, select **Close** to close the edit panel.

10. Repeat the steps for the layers that you want to import to your CAD source file.


**Parent Topic:**[Configure CAD objects using the Map Configuration tab](../concept/manage-cad-map-config.md)

**Previous topic:**[Georeference your floor plan](georeference-floor-plan.md)

**Next topic:**[Configure places](edit-places.md)

