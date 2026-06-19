---
title: AI Search activity reports
description: Reports summarize your AI Search configurations and trends.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/ais-admin-console-activity-reports.html
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Track your AI, Using AI Search Admin console, AI Search Admin console, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# AI Search activity reports

Reports summarize your AI Search configurations and trends.

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Applications that need configuration|Single Score \(\[Omitted image "single-score.svg"\] Alt text: Single score icon.\)|ais\_publish\_history, sp\_portal, sys\_cs\_context\_profile\_search, sys\_properties, sys\_search\_context\_config, and sys\_sg\_global\_search \(all accessed via AISGetAppStatus script include\)|Shows the number of search applications that need configuration before AI Search can be enabled.|
|Applications ready to turn on|Single Score \(\[Omitted image "single-score.svg"\] Alt text: Single score icon.\)|ais\_publish\_history, sp\_portal, sys\_cs\_context\_profile\_search, sys\_properties, sys\_search\_context\_config, and sys\_sg\_global\_search \(all accessed via AISGetAppStatus script include\)|Shows the number of search applications that have AI Search configurations and are ready to have AI Search enabled.|
|Applications with AI Search on|Single Score \(\[Omitted image "single-score.svg"\] Alt text: Single score icon.\)|ais\_publish\_history, sp\_portal, sys\_cs\_context\_profile\_search, sys\_properties, sys\_search\_context\_config, and sys\_sg\_global\_search \(all accessed via AISGetAppStatus script include\)|Shows the number of search applications that have AI Search enabled.|
|Indexed documents by month|Bar \(\[Omitted image "column-icon.png"\] Alt text: Bar icon.\)|sn\_ais\_admin\_tools\_ai\_search\_dashboard\_documents\_by\_month|Shows the number of searchable records newly indexed by AI Search, grouped by month.|
|Documents by indexed sources|Donut \(\[Omitted image "donut-icon.png"\] Alt text: Donut icon.\)|sn\_ais\_admin\_tools\_ai\_search\_dashboard\_total\_indexed\_documents|Shows the number of searchable records indexed by AI Search, grouped by indexed source.|
|Queries by search profile|Donut \(\[Omitted image "donut-icon.png"\] Alt text: Donut icon.\)|sys\_search\_event|Shows the number of search queries, grouped by search profile used.|

**Parent Topic:**[Track your AI Search activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/ais-admin-console-track-activity.md)

