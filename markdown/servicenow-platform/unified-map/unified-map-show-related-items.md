---
title: View related items for a CI
description: Open the Related items panel in Unified Map to show all related items \(typically, events such as changes, active incidents, or active problems\) for the selected CI.
locale: en-US
release: zurich
product: Unified Map
classification: unified-map
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# View related items for a CI

Open the **Related items** panel in Unified Map to show all related items \(typically, events such as changes, active incidents, or active problems\) for the selected CI.

## Before you begin

Role required:

-   To access maps: sn\_cmdb\_user, sn\_cmdb\_editor or sn\_cmdb\_admin
-   To access maps with operational service instances: app\_service\_user, and sm\_user or sm\_admin
-   To access maps with operational and non-operational service instances: app\_service\_admin, and sm\_user or sm\_admin
-   To access and view related items: itil

## About this task

**Note:** The timeline also indicates related items \(events\). One important difference is that the timeline indicates only historical related items — events that occurred before the timeline's map time. In contrast, the **Related items** panel lists all related items. For more information, see [Viewing related items on the Unified Map timeline](../concept/unified-map-timeline-working-on.md).

## Procedure

1.  While working in a map, select a CI on the map and then select the Related items icon ![](../image/icon-um-related-items-panel.png).

    Related items are grouped by category. Badges show the count of related items for the selected CI \(or for all CIs if no CI is selected\).

    ![Related items for the selected CI.](../image/um-related-items-panel.png)

    To specify which related item categories should appear on the **Related items** panel, see [Configure the Related items panel](unified-map-configure-rel-items.md).

2.  Select an arrow to view the details of the related item record.

    Details of the change, incident, or problem appear on a card in the Related items panel. Select a card to highlight the associated CI on the map.


## What to do next

-   Select another CI on the map to show its related items.
-   Select an empty space on the map to show all related items for all CIs on the map.
-   Select a related item category with one or more items to view detailed related item cards. On a card:
    -   Select the related item link to drill down to the related item record.
    -   Open the filter panel to set a sorting category and order for the cards.
    -   Some details, such as **Priority** and **Risk**, are color-coded using the default platform color code settings.

