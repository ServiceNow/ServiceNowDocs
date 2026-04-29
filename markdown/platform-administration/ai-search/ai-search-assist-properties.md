---
title: AI Search Assist properties
description: The AI Search Assist properties determine when searching begins based on characters entered and the time that has elapsed. These properties reduce the impact of searches for systems with many Catalog Items or Knowledge articles.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [AI Search record producer for Service Portal, Integrate, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# AI Search Assist properties

The AI Search Assist properties determine when searching begins based on characters entered and the time that has elapsed. These properties reduce the impact of searches for systems with many Catalog Items or Knowledge articles.

## AI Search Assist properties

<table id="table_xbs_wlj_h4b"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.ai\_search\_assist.min\_length

</td><td>

The minimum number of characters entered before a search initiates. The default is 3.

</td></tr><tr><td>

com.snc.ai\_search\_assist.wait\_time

</td><td>

The time elapsed after the user finishes entering characters in the search field before the search begins. **Note:** If you set the time to '-1', the search begins when the user leaves the search field. This behavior is known as 'Search on tab'.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search Assist record producer integration for Service Portal](../concept/ai-search-assist.md)

