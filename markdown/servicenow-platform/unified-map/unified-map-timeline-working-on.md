---
title: Viewing related items on the Unified Map timeline
description: The timeline indicates related items like incidents, problems, and changes over a specified period of time for the selected CI. You can use the timeline to visualize the history of changes to a CI and how they affect the topology of the CMDB.
locale: en-US
release: australia
product: Unified Map
classification: unified-map
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Unified Map, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Viewing related items on the Unified Map timeline

The timeline indicates related items like incidents, problems, and changes over a specified period of time for the selected CI. You can use the timeline to visualize the history of changes to a CI and how they affect the topology of the CMDB.

## Viewing related items

-   When you first open a map, CIs and relationships appear as they are at the current moment in time. When you select a CI on the map, the timeline displays related items for the CI.

-   You can drag the map time marker \(A in the image\) on the timeline to specify the end date \(the map time\) for data that should appear on the map and on the timeline. The default map time is "now", but you can specify a particular date or drag the marker to a date.

-   The map and the timeline are synchronized. The map shows the selected CI and its connections as they existed \(based on the creation date of nodes\) at the specified map time. The timeline displays markers \(B in the image\) to indicate related items that happened at or before map time.

    ![The timeline indicates all related items for the CI within a time span that happened before the specified map time.](../image/um-timeline.png)

-   You can also specify the overall time span \(C in the image\) of the timeline view.

-   CIs that were created after the map time don't appear on the timeline and don't affect items on the timeline.
-   Multiple related items on the same date are indicated by a badge that shows the count of related items.

## Actions on the timeline

<table id="table_nnx_x43_ccc"><thead><tr><th>

Desired result

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Show or hide the timeline

</td><td>

Select the Timeline icon ![](../image/icon-um-toggle-timeline.png).

</td></tr><tr><td>

Set the map time marker \(and therefore the items on the map\) to the current time

</td><td>

Select **Now**.

</td></tr><tr><td>

Set map time to a particular date and time

</td><td>

Drag the map time marker.

</td></tr><tr><td>

Scroll the timeline toward the past or the future

</td><td>

Select an arrow at the side of the timeline.

</td></tr><tr><td>

View the date and time for a related item marker

</td><td>

Move to the marker.

</td></tr><tr><td>

View the details for a related item

</td><td>

Move to the badge for the related item.

</td></tr><tr><td>

Change the time span of the timeline

</td><td>

Select a zoom icon ![](../image/icon-um-timeline-zoom-out.png) or ![](../image/icon-um-timeline-zoom-in.png).

 The time span can range from six months in the past to six months in the future.

 A related item that has occurred or that will occur outside the range doesn't appear on the timeline. Such related items, however, still appear in the corresponding **Related items** panel. In addition, a badge in the map might show data for the related item.

</td></tr><tr><td>

Manage a marker

</td><td>

Select the marker, select the more actions icon ![](../image/icon-um-more-options-vertical.png), and then select one of the following actions:

 -   **Replace marker**: Replace the current marker with a marker for the specified date.
-   **Clear marker**: Clear all markers.
-   **Add marker**: Add a marker for the specified date.

</td></tr><tr><td>

View related items for all CIs on the map

</td><td>

Select an empty space on the map.

</td></tr></tbody>
</table>## Configuring general timeline properties

Admins can configure some properties of the timeline that affect all users, such as which related item details appear on timelines. For more information, see [Configure how to display related items on the map](../task/unified-map-config-related-items.md).

