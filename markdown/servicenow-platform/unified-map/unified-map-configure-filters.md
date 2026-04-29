---
title: Use filters to specify which nodes should appear on a map
description: Customize the map to focus on the CIs that you want to work on by filtering out \(hiding\) irrelevant CIs. You can filter by layer count, CI class, relationship type, discovery source, location, and CI ownership.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use filters to specify which nodes should appear on a map

Customize the map to focus on the CIs that you want to work on by filtering out \(hiding\) irrelevant CIs. You can filter by layer count, CI class, relationship type, discovery source, location, and CI ownership.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

When a user applies a shared preset or a user preset, all filter settings are overridden. Filter attributes from a shared preset or a user preset that do not apply to the current map are listed in the **Unused filter attributes** section of the filter panel. The order of filter-setting precedence from the various sources is as follows:

1.  user presets
2.  shared presets
3.  shared presets that are defined in a **Unified Map shared presets** profile
4.  class profile \(Class profiles contain only layer settings and are defined in the **Node Map Profiles** related list.\)

**Note:** Filter settings that would filter out the home node might appear in the list. You can't, however, filter out the home node even if it meets filter settings.

## Procedure

1.  While working in a map, select the Map filter icon ![](../image/icon-um-filter-outline.png) and then select or clear criteria in any filter category.

    Only attributes of elements currently on the map are listed as filter criteria. Attributes that do not apply to the current elements are listed in the **Unused filter attributes** list.

2.  Close the Map filter panel.

    -   A dot appears on the Map filter icon ![](../image/icon-um-filter-outline.png) to indicate that filters are applied.
    -   To expose filtered CIs and relationships on the map as dimmed view-only images, select the Show filtered items icon ![](../image/icon-um-show-hide-filtered-items.png).
    -   You can save filter settings for reuse. For more information, see [Create or manage a user preset](unified-map-manage-preset-filter.md).
    -   Maps show up to 250 CMDB elements. Remaining elements are truncated and don't appear on the map.

## What to do next

To apply the home CI's default filter settings, select **Reset filter**.

Admins can save filter settings as a shared preset that all users can apply. For more information, see [Create or manage a user preset](unified-map-manage-preset-filter.md).

**Related topics**  


[Create or manage a user preset](unified-map-manage-preset-filter.md)

