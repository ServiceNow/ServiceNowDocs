---
title: Use filters to specify which nodes should appear on a map
description: Customize the map to focus on the CIs that you want to work on by filtering out \(hiding\) irrelevant CIs. You can filter by layer count, CI class, relationship type, discovery source, location, and CI ownership.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/unified-map/unified-map-configure-filters.html
release: yokohama
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [UNDER CONSTRUCTION Use, Unified Map, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Use filters to specify which nodes should appear on a map

Customize the map to focus on the CIs that you want to work on by filtering out \(hiding\) irrelevant CIs. You can filter by layer count, CI class, relationship type, discovery source, location, and CI ownership.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational application services: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational application services: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

-   When a user applies a shared preset or a user preset, all filter settings are overridden. Filter attributes from a shared preset or a user preset that do not apply to the current map are listed in the **Unused filter attributes** section of the filter panel. The order of precedence from the various sources is as follows:
    1.  user presets
    2.  shared presets
    3.  shared presets that are defined in a **Unified Map shared presets** profile
    4.  class profile \(Class profiles are defined in the **Node Map Profiles** related list and contain only layer settings\)
-   Filter conditions that would filter out the home node might appear in the panel. You can't, however, filter out the home node even if it does not match the filter conditions.

## Procedure

1.  Select Open filter panel \(\[Omitted image "icon-um-filter-outline.png"\] Alt text: Open filter icon.\) and then select or clear filters.

    Each filtering category includes only items that are relevant to the current map. The map immediately applies the filters you select.

2.  Close the Map filter panel.

    -   A dot appears on the Map filter icon \[Omitted image "icon-um-filter-outline.png"\] to indicate that filters are applied.
    -   To expose filtered CIs and relationships on the map as dimmed view-only images, select the Show filtered items icon \[Omitted image "icon-um-show-hide-filtered-items.png"\].
    -   You can save filter settings for reuse. For more information, see [Create or manage a user preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-manage-preset-filter.md).
    -   Maps show up to 250 CMDB elements. Remaining elements are truncated and don't appear on the map.

## What to do next

To apply the home CI's default filter settings, select **Reset filter**.

Admins can save filter settings as a shared preset that all users can apply. For more information, see [Create or manage a user preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-manage-preset-filter.md).

**Related topics**  


[Create or manage a user preset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/unified-map/unified-map-manage-preset-filter.md)

