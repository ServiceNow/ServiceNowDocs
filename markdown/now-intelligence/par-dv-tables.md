---
title: Platform Analytics data visualization tables
description: The following tables relate to Platform Analytics data visualizations and can be accessed through scripts.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-02-24"
reading_time_minutes: 1
breadcrumb: [Platform Analytics]
---

# Platform Analytics data visualization tables

The following tables relate to Platform Analytics data visualizations and can be accessed through scripts.

|Table|Description|
|-----|-----------|
|par\_component|Contains all data visualizations in the visualization library and all filters in the filter library. Extends sys\_metadata.|
|par\_component\_permission|Contains the role, group, and user permissions for all data visualizations and filters in their respective libraries.|
|par\_export|Lists all scheduled dashboard and data visualization exports. Extends sys\_metadata.|
|par\_export\_job|Stores details of every attempt to export a dashboard or data visualization.|
|par\_export\_visualization|Stores the export details of all scheduled data visualization exports. Extends par\_export.|
|par\_metadata|Stores the metadata for each data visualization type.|
|par\_notification|Lists email notification definitions of scheduled dashboard and data visualization exports. Extends sys\_metadata.|
|par\_notification\_email|Stores metadata of scheduled dashboard and data visualization export emails, including subject and message. Extends par\_notification.|
|par\_notification\_email\_recipients|Stores groups and users who receive a notification email with a scheduled dashboard and data visualization export. Contains the non-metadata information for the emails.|
|par\_visualization|Contains all data visualizations in the visualization library. Extends par\_component.|
|par\_visualization\_permission|Contains the role, group, and user permissions for all data visualizations in the visualization library. Extends par\_component\_permission.|

**Parent Topic:**[Platform Analytics](../../performance-analytics/concept/c_performanceAnalyticsAndReporting.md)

