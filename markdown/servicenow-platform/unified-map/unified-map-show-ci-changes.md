---
title: View historical changes for a CI
description: The Changes panel in Unified Map displays change details such as changes to life cycle stage or operational state for the selected CI.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View historical changes for a CI

The **Changes** panel in Unified Map displays change details such as changes to life cycle stage or operational state for the selected CI.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

Changes are also indicated on the timeline. For more information, see [Viewing related items on the Unified Map timeline](../concept/unified-map-timeline-working-on.md).

## Procedure

1.  While working in a map, select a CI on the map and then select the Changes icon ![](../image/icon-um-overview-panel.png).

    All changes for the selected CI appear on the panel.

    ![Details of changes for the CI.](../image/um-changes-panel.png)

    -   Select **Show more / Show less** for details on a card.
    -   To flag a change as important, hold the cursor over a change and then select the Flag as important icon.

2.  Perform other tasks.

    -   Select another CI on the map to view its changes.
    -   Select the Open filters ![](../image/icon-um-change-filter.png) and then select and configure any of the following filter types:
        -   Post types
        -   Field changes
        -   Flagged
        -   Filter sets
    -   Select the Search icon ![](../image/icon-um-change-search.png) and enter text in the **Search Activity stream** field to find specific changes by entering terms.
    -   Select the ascending ![](../image/icon-um-open-filter-panel.png) or descending sort icon ![](../image/icon-um-change-sort.png) to toggle between ascending or descending sort.
    -   Create a filter set to supplement the existing filtering options on the Changes panel. You can save filter settings for reuse. For more information, see [Create or manage a user preset](unified-map-manage-preset-filter.md).

**Related topics**  


[Viewing related items on the Unified Map timeline](../concept/unified-map-timeline-working-on.md)

