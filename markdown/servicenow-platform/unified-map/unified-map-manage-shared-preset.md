---
title: Create or manage a shared preset
description: Admins can save a set of Unified Map map filter settings \(layer, CI class, relationship type, and other CI attribute settings\) as a shared preset that any user can apply to their map view.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Administer, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or manage a shared preset

Admins can save a set of Unified Map map filter settings \(layer, CI class, relationship type, and other CI attribute settings\) as a shared preset that any user can apply to their map view.

## Before you begin

Role required: sn\_cmdb\_config\_admin

## About this task

Follow this procedure to save specified filter settings as a shared preset. The workspace-specific filter criteria in a shared preset are available for all users of the current CMDB Unified Map page. Shared presets defined in one workspace are not available in other workspaces.

Configuration settings for shared presets are saved in the **Unified Map shared presets** profile in the configuration identifier that is applied to the workspace.

-   When a user applies a shared preset or a user preset, all filter settings are overridden. Filter attributes from a shared preset or a user preset that do not apply to the current map are listed in the **Unused filter attributes** section of the filter panel. The order of filter-setting precedence from the various sources is as follows:
    1.  user presets
    2.  shared presets
    3.  shared presets that are defined in a **Unified Map shared presets** profile
    4.  class profile \(Class profiles contain only layer settings and are defined in the **Node Map Profiles** related list.\)
-   You can include a shared preset in a node map profile. Layer settings in the shared preset will override the layer settings defined in the class profile.
-   A shared preset defined in a profile will be applied when the map opens. If the user has explicitly defined a shared preset or a user preset, then the preset takes precedence as outlined earlier.
-   An individual user can apply a shared preset and then save it as a user preset. For more information, see [Create or manage a user preset](unified-map-manage-preset-filter.md).
-   Unused filter criteria in the current filter are saved with a preset.

## Procedure

1.  While working in a map, select the Map filter icon ![](../image/icon-um-filter-outline.png) and then select or clear criteria in any filter category.

    Only attributes of elements currently on the map are listed as filter criteria. Attributes that do not apply to the current elements are listed in the **Unused filter attributes** list.

2.  Select the Manage presets icon ![](../image/icon-um-more-options-vertical.png) and, in the Manage shared presets list, select **Create shared preset**.

3.  Enter a preset name and then select **Save**.

4.  Close the Map filter panel.


## Result

The new shared preset is listed in the **Unified map shared presets** related list on the Configuration Identifier form. In addition, shared presets used in a map profile are listed in the **Node Map Profiles** related list. For more information, see [How configuration settings for Unified Map are stored](../concept/unified-map-config-settings-viewing.md)

## What to do next

-   **To apply a preset:**
    1.  While working in a map, select the open filter panel icon ![](../image/icon-um-filter-outline.png)
    2.  Select the View preset list icon ![](../image/icon-um-down-arrow-filled.png) and then select the preset.
-   **To update a preset or save an updated version as a new preset:**
    1.  While working in a map, select the open filter panel icon ![](../image/icon-um-filter-outline.png)
    2.  Apply the preset that you want to update and then make the desired changes.
    3.  Select the Manage presets icon ![](../image/icon-um-more-options-vertical.png) and then select **Update preset** or **Update shared preset**.
    4.  Select one of the following actions:
        -   Select **Update preset** to update the current preset with the current filter settings.
        -   Select **Save as new preset** and then enter a new name.
    5.  Select **Save**.
-   **To delete a preset:**
    1.  While working in a map, select the open filter panel icon ![](../image/icon-um-filter-outline.png)
    2.  Apply the preset that you want to delete.
    3.  Select the Manage presets icon ![](../image/icon-um-more-options-vertical.png) and then select **Delete preset** or **Delete shared preset**.
    4.  Select **Yes**.
-   **To apply the home CI default filter settings**

    Select **Reset filter**.


**Parent Topic:**[Configuring Unified Map — admin settings](../concept/administer-unified-map.md)

**Related topics**  


[Use filters to specify which nodes should appear on a map](unified-map-configure-filters.md)

[Create or manage a user preset](unified-map-manage-preset-filter.md)

[Create a class profile of visible layers for classes](unified-map-config-class-profile.md)

