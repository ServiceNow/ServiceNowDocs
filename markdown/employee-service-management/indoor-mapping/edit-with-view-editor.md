---
title: Edit with view editor
description: Edit and customize indoor maps with the Map Studio view editor. Enabling the default view in Indoor Mapping is a mandatory step so that maps can render in Workplace Service Delivery.
locale: en-US
release: yokohama
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Edit with view editor

Edit and customize indoor maps with the Map Studio view editor. Enabling the default view in Indoor Mapping is a mandatory step so that maps can render in Workplace Service Delivery.

## Before you begin

For Indoor Mapping View editor, as a map administrator you cab decide which elements should be visible to map users. You can also define the style of different items such as layers and places. A default view type is available with Indoor Mapping but needs to be enabled. This is a mandatory step. If the default view is not enabled, Indoor Mapping maps are not rendered in Workplace Service Delivery.

You can create and customize additional view types as required. However, only the default view type is used in Workplace Service Delivery currently. View type and View editor are capabilities of Indoor Mapping.

**Note:** Ensure that you have installed both Indoor Mapping and Workplace Indoor Mapping plugins.

Role required: map admin, map editor, map editor limited

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

2.  Select a campus or building from the home page and select **View editor**.

    The **Default** view and other view types that you have added to the View editor is displayed. For example, click **Default**. The **Edit** button is displayed when the view has already been configured and is not blank. If the view is never configured or is blank, it is replaced by a **Not enabled** warning. Click to edit and enable the view.

    ![edit with view editor](../images/view-editor-initial-content.png "View Editor")

3.  You are provided with the following four options.

    These options define the content that you want to display on you map. For example, adding multiple view types in your campus such as layers, places, place types, etc.

    -   **All content**: In this option, the view is automatically generated. All buildings and floors are selected. All layer types, place types, connector types are also selected with the default style. All direction modes are selected.
    -   **Copy from view**: Option to select a view. It can be other view types from the same campus or a view type from another campus. Only views that are configured appears. When selecting a view from the same campus, all view content is copied including buildings and floors. When selecting a view from a different campus, all buildings and floors are included with default options as they cannot be copied from the other campus.

        You can copy the selected content and style from another view. For example, if you want to change the display of place types in a view, you don't have to redo the whole process for each place type. You can just copy the configurations from another view and make the required adjustments to suit your needs.

    -   **Specific content**: Pop-up dialog box option to select the buildings/floors, layer types, place types, connector types, and direction modes from the check list. The selected content is added to the view with its default style.
    -   **Start from a blank view**: In this option, you are not selecting any content. Nothing is displayed on the view and the map.
4.  Select any of the four options from Step 3.

    For example, **Use the default configuration**.

5.  Click **Continue**.

    The view content is loaded for the selected option and the map for selected campus along with view type is shown.

6.  Click **Save this view** to save the changes.

7.  When there is more than one View type, map creators can select **Copy another view** and then, **Import Styles from an existing**.

8.  The **View Editor Content** displays content based on your selection.

    For more information, see [View editor content](view-editor-content.md).

9.  Click **Apply** to apply the view changes.

10. Click **Save this view**.

    You also have the option to reset the view by clicking the More options menu icon \( ![More options icon.](../../wsd-for-mobile/images/more-options-icon.png)\) available next to **Save this view option**.


-   **[View editor content](view-editor-content.md)**  
Work with the View Editor content and customize the campus, buildings, layers, places, connectors, and direction modes properties.

**Parent Topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Previous topic:**[Copy direction graphs to multiple floors](copy-directions-multiple-floors.md)

**Next topic:**[View editor content](view-editor-content.md)

