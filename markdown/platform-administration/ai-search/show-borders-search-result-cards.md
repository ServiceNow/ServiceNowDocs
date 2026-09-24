---
title: Show borders between search result cards
description: Display borders between search result cards in portal search and in global and workspace search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ai-search/show-borders-search-result-cards.html
release: brazil
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Show borders between search result cards

Display borders between search result cards in portal search and in global and workspace search.

## Before you begin

Role required: admin

## About this task

By default, AI Search doesn't show borders between search result cards. You can configure AI Search to display borders between search result cards by creating a **glide.search.show\_result\_card\_border** system property with value **true**.

This system property controls search result card borders in portal search and in global and workspace search.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Select **New**.

3.  On the System Property form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Name|glide.search.show\_result\_card\_border|
    |Type|true \| false|
    |Value|true|

4.  Select **Submit**.


## Result

AI Search shows borders between search result cards in portal search and in global and workspace search.

**Parent Topic:**[Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ai-search/configuring-ais.md)

