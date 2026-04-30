---
title: Filtering activities and connections
description: Focus in on how activities relate to your process by refining the activities and connections views.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Filtering project data, Analyzing and getting process insights, Using Process Mining, Process Mining, Platform Analytics]
---

# Filtering activities and connections

Focus in on how activities relate to your process by refining the activities and connections views.

From the process map screen, you can choose to show more or fewer variances relevant to activities by moving the activities and connections sliders.

Use the Activities slider to zoom in on records that pass a certain activities more or less often than a certain threshold.

Use the Connections slider to zoom in on a lower limit of records which followed an activity sequence within routes.

**Note:**

-   Process Mining generates a limit of 5000 elements per defined activity.
-   If you slide both the Activities and Connections sliders to their maximum ranges, process map rendering may be impacted. To optimize the map's rendering, configure the project to group more of the activities that are defined. See [Configure an activity definition](../task/configure-activity.md).

![Refine connections or activities](../image/refine-activities-connections.gif)

In comparing connections for various routes in the process map, you will see that they may have different widths. The widths correspond to a smaller or larger number of records that followed a connection or route.

**Parent Topic:**[Filtering project data](../task/filter-project.md)

