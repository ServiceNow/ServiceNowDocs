---
title: Create or manage a user preset
description: Save useful Unified Map filter settings as a user preset that you can apply to a map at any time. For example, define a filter to display only CIs of a particular class and then save the filter settings as a user preset.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/unified-map/unified-map-manage-preset-filter.html
release: yokohama
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-08-04"
reading_time_minutes: 3
breadcrumb: [Filter CIs, UNDER CONSTRUCTION Use, Unified Map, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create or manage a user preset

Save useful Unified Map filter settings as a user preset that you can apply to a map at any time. For example, define a filter to display only CIs of a particular class and then save the filter settings as a user preset.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational application services: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational application services: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

-   Follow this procedure to create a user preset that applies specified filter settings. Only you can apply your user presets to your personal view of the map.
-   In addition, admins can define shared presets that you and other users can access. For more information, see [Create or manage a shared preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-manage-shared-preset.md).
-   -   When a user applies a shared preset or a user preset, all filter settings are overridden. Filter attributes from a shared preset or a user preset that do not apply to the current map are listed in the **Unused filter attributes** section of the filter panel. The order of precedence from the various sources is as follows:
    1.  user presets
    2.  shared presets
    3.  shared presets that are defined in a **Unified Map shared presets** profile
    4.  class profile \(Class profiles are defined in the **Node Map Profiles** related list and contain only layer settings\)
-   Filter conditions that would filter out the home node might appear in the panel. You can't, however, filter out the home node even if it does not match the filter conditions.

## Procedure

1.  Select Open filter panel \(\[Omitted image "icon-um-filter-outline.png"\] Alt text: Open filter icon.\) and then select or clear filters.

    Each filtering category includes only items that are relevant to the current map. The map immediately applies the filters you select.

2.  Select the Manage presets icon \[Omitted image "icon-um-more-options-vertical.png"\] and then, in the Manage my presets list, select **Create preset**.

3.  Enter a preset name and then select **Save**.

4.  Close the Map filter panel.


## What to do next

-   **To apply a preset:**
    1.  While working in a map, select the open filter panel icon \[Omitted image "icon-um-filter-outline.png"\]
    2.  Select the View preset list icon \[Omitted image "icon-um-down-arrow-filled.png"\] Alt text: and then select the preset.
-   **To update a preset or save an updated version as a new preset:**
    1.  While working in a map, select the open filter panel icon \[Omitted image "icon-um-filter-outline.png"\]
    2.  Apply the preset that you want to update and then make the desired changes.
    3.  Select the Manage presets icon \[Omitted image "icon-um-more-options-vertical.png"\] Alt text: and then select **Update preset** or **Update shared preset**.
    4.  Select one of the following actions:
        -   Select **Update preset** to update the current preset with the current filter settings.
        -   Select **Save as new preset** and then enter a new name.
    5.  Select **Save**.
-   **To delete a preset:**
    1.  While working in a map, select the open filter panel icon \[Omitted image "icon-um-filter-outline.png"\]
    2.  Apply the preset that you want to delete.
    3.  Select the Manage presets icon \[Omitted image "icon-um-more-options-vertical.png"\] Alt text: and then select **Delete preset** or **Delete shared preset**.
    4.  Select **Yes**.
-   **To apply the home CI's default filter settings**

    Select **Reset filter**.


**Related topics**  


[Use filters to specify which nodes should appear on a map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-configure-filters.md)

