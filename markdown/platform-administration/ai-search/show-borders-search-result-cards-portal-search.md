---
title: Show borders between search result cards in portal search
description: Display borders between search result cards on the search results page for portal search applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/show-borders-search-result-cards-portal-search.html
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-11-03"
reading_time_minutes: 1
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer]
---

# Show borders between search result cards in portal search

Display borders between search result cards on the search results page for portal search applications.

## Before you begin

Role required: sp\_admin or admin

## About this task

By default, AI Search displays no borders between search result cards on the portal search results page. You can enable display of borders between search result cards on the portal search results page by configuring the Faceted Search Service Portal widget.

To learn more about Service Portal widgets, see [Using portal widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/service-portal/service-portal-widgets.md).

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

2.  Open the **Faceted Search** widget record.

3.  In the Body HTML template field, find the **show-card-border** setting and change its value from **\{\{false\}\}** to **\{\{true\}\}**.

4.  Select **Update**.


## Result

AI Search displays borders between search result cards on the search results page for portal search applications.

**Note:** Users who have the portal search results page open may not see the change take effect until they refresh the portal page.

## What to do next

For details on showing borders between search results cards in global search, see [Show borders between search result cards in global search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/show-borders-search-result-cards-global-search.md).

**Parent Topic:**[Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/configuring-ais.md)

