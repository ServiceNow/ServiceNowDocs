---
title: Data visualization library recommendations
description: Analytics managers can view information about potentially problematic data visualizations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/data-viz-library-recommendations.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Library recommendations, Platform Analytics experience, Platform Analytics]
---

# Data visualization library recommendations

Analytics managers can view information about potentially problematic data visualizations.

## Data visualization recommendation panel

\[Omitted image "dv-recommendation-panel.png"\] Alt text: Data visualization library showing recommendation panel.

Visible to roles: viz\_admin and higher, including pa\_admin.

The book icon \[Omitted image "book-icon.png"\] expands and hides the data visualization recommendation panel. It also shows how many recommendation tiles there are. Selecting a tile filters the library on the matching data visualizations.

If the system property com.glide.par.v\_table\_join.enabled is true, only Next Experience data visualizations are included in the recommendations. If this property is false or null, both Next Experience and Core UI data visualizations are included in recommendations.

The following types of recommendations are currently available:

|Tile|Description|
|----|-----------|
|n Unused data visualizations|Number of data visualizations that aren't used in any dashboards|
|n No active owner|Number of data visualizations without an active owner|

**Parent Topic:**[Platform Analytics library recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/pa-library-recommendations.md)

