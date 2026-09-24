---
title: Dashboard library recommendations
description: Analytics managers can view information about potentially problematic dashboards.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/dashboard-library-recommendations.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Library recommendations, Platform Analytics experience, Platform Analytics]
---

# Dashboard library recommendations

Analytics managers can view information about potentially problematic dashboards.

## Dashboard recommendation panel

\[Omitted image "db-recommendation-panel.png"\] Alt text: Dashboard library showing recommendation panel.

Visible to roles: dashboard\_admin and higher.

The book icon \[Omitted image "book-icon.png"\] expands and hides the dashboard recommendation panel. It also shows how many recommendation tiles there are. Selecting a tile filters the library on the matching dashboards.

If the system property com.glide.par.v\_table\_join.enabled is true, only Next Experience dashboards are included in the recommendations. If this property is false or null, both Next Experience and Core UI dashboards are included in recommendations.

The following types of recommendations are available:

|Tile|Description|
|----|-----------|
|n Unused dashboards|Number of dashboards without recent views. "Recent" is defined in the system property sn\_analytics\_rcmnd.recommendation\_metrics\_time\_period|
|n Empty dashboards|Number of dashboards that contain no widgets|
|n No active owner|Number of dashboards without an active owner|

**Parent Topic:**[Platform Analytics library recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/pa-library-recommendations.md)

