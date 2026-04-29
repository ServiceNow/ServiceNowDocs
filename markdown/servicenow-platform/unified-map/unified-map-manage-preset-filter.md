---
title: Create or manage a user preset
description: Save useful Unified Map filter settings as a user preset that you can apply to a map at any time. For example, define a filter to display only CIs of a particular class and then save the filter settings as a user preset.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Filter CIs, Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or manage a user preset

Save useful Unified Map filter settings as a user preset that you can apply to a map at any time. For example, define a filter to display only CIs of a particular class and then save the filter settings as a user preset.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

-   Follow this procedure to create a user preset that applies specified filter settings. Only you can apply your user presets to your personal view of the map.
-   In addition, admins can define shared presets that you and other users can access. For more information, see [Create or manage a shared preset](unified-map-manage-shared-preset.md).

    When a user applies a shared preset or a user preset, all filter settings are overridden. Filter attributes from a shared preset or a user preset that do not apply to the current map are listed in the **Unused filter attributes** section of the filter panel. The order of filter-setting precedence from the various sources is as follows:

    1.  user presets
    2.  shared presets
    3.  shared presets that are defined in a **Unified Map shared presets** profile
    4.  class profile \(Class profiles contain only layer settings and are defined in the **Node Map Profiles** related list.\)
    **Note:** Filter settings that would filter out the home node might appear in the list. You can't, however, filter out the home node even if it meets filter settings.


## Procedure

1.  While working in a map, select the Map filter icon ![](../image/icon-um-filter-outline.png) and then select or clear criteria in any filter category.

    Only attributes of elements currently on the map are listed as filter criteria. Attributes that do not apply to the current elements are listed in the **Unused filter attributes** list.

2.  Select the Manage presets icon ![](../image/icon-um-more-options-vertical.png) and then, in the Manage my presets list, select **Create preset**.

3.  Enter a preset name and then select **Save**.

4.  Close the Map filter panel.


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


**Related topics**  


[Use filters to specify which nodes should appear on a map](unified-map-configure-filters.md)

