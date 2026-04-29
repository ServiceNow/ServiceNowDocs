---
title: Dashboard library recommendations
description: Analytics managers can view information about potentially problematic dashboards.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Library recommendations, Platform Analytics experience, Platform Analytics]
---

# Dashboard library recommendations

Analytics managers can view information about potentially problematic dashboards.

## Dashboard recommendation panel

![Dashboard library showing recommendation panel.](../image/db-recommendation-panel.png)

Visible to roles: dashboard\_admin and higher.

The book icon ![](../image/book-icon.png) expands and hides the dashboard recommendation panel. It also shows how many recommendation tiles there are. Selecting a tile filters the library on the matching dashboards.

The following types of recommendations are currently available:

|Tile|Description|
|----|-----------|
|n Unused dashboards|Number of dashboards without recent views. "Recent" is defined in the system property sn\_analytics\_rcmnd.recommendation\_metrics\_time\_period|
|n Empty dashboards|Number of dashboards that do not contain any widgets|
|n No active owner|Number of dashboards without an active owner|

**Parent Topic:**[Platform Analytics library recommendations](../concept/pa-library-recommendations.md)

