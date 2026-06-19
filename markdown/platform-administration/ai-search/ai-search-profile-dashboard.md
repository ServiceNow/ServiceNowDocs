---
title: AI Search Profile dashboard
description: The AI Search Profile dashboard summarizes indexed record counts and search query traffic associated with a search profile defined in AI Search. Interactive filters enable users to choose a search profile and select the time frame for analysis of search query traffic.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/ai-search-profile-dashboard.html
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# AI Search Profile dashboard

The AI Search Profile dashboard summarizes indexed record counts and search query traffic associated with a search profile defined in AI Search. Interactive filters enable users to choose a search profile and select the time frame for analysis of search query traffic.

\[Omitted image "adv-ais-mgmt-dashboard-profile.png"\] Alt text: AI Search Profile dashboard.

To access the dashboard, navigate to **All** &gt; **AI Search** &gt; **AI Search Analytics** &gt; **Search Profile Analytics**.

**Note:** If the dashboard displays a `Read operation on table '<name>' from scope 'Advanced AI Search Management Tools' was denied` informational message, ask your administrator to perform the steps described in [Create a cross-scope access privilege for the AI Search dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/ais-dashboards-cross-scope-access.md) for the listed table.

## Required ServiceNow AI Platform® roles

To view or edit the dashboard, you must have the ais\_admin role.

You may need additional roles to view and select search profiles for some AI Search applications or portals. For example, the **ESC Portal Default Search Profile** for the ESC portal is only visible in the search profile list if you have Employee Center administrator \[sn\_hr\_sp.esc\_admin\] role.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|AI Search administrator|Reviews indexed record counts and follows search query traffic trends for search profiles defined in AI Search.|

## Data visualizations

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Searchable Documents|Single Score \[Omitted image "single-score.svg"\] Alt text:|sn\_ais\_admin\_tools\_ai\_search\_dashboard\_documents\_by\_search\_profile|Shows the number of indexed records that users can find when searching with the selected search profile.|
|Documents by Search Source|Donut \[Omitted image "donut-icon.png"\] Alt text:|sn\_ais\_admin\_tools\_ai\_search\_dashboard\_documents\_by\_search\_source|Shows the number of indexed records accessible from each search source linked to the selected search profile.|
|Queries by Application|Bar \[Omitted image "column-icon.png"\] Alt text:|sys\_search\_event|Shows the number of search queries that used the selected search profile in the selected query time frame, grouped by search application.|
|Queries Run Against This Profile|Line \[Omitted image "line-icon.png"\] Alt text:|sys\_search\_event|Shows the number of search queries that used the selected search profile in the selected query time frame, grouped by month.|

