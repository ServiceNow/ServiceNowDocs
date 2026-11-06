---
title: Allow source facet filters to trigger query resubmission for multi-term search queries
description: Allow source facet filter selections to reduce the search result count used by the system when checking whether to resubmit multi-term search queries using the OR operator.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/ai-search/allow-src-facet-filters-trigger-query-resubmission.html
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-10-24"
reading_time_minutes: 2
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Allow source facet filters to trigger query resubmission for multi-term search queries

Allow source facet filter selections to reduce the search result count used by the system when checking whether to resubmit multi-term search queries using the OR operator.

## Before you begin

Role required: admin

## About this task

AI Search includes an AND-to-OR fallback mechanism that can be triggered when your multi-term search query matches less than one full page of results. When this query resubmission mechanism is triggered, the system resubmits your affected search query using the OR operator instead of the default AND operator. Query resubmission improves search recall at the expense of search precision, allowing your search to match additional results which only contain some of your search terms.

As an example, a search for query `Lake Ontario offices` initially uses the AND operator and so only matches results that contain all three of your search terms. If this search doesn't return enough results to fill a full page, AI Search triggers query resubmission. The resubmitted query uses the OR operator and looks for results that match at least half \(rounded up\) of your search terms. This means your search might return results that only match two of your three search terms, instead of just the results that match all three terms.

**Note:** Query resubmission behavior is controlled by the value of the **glide.ais.query.search\_operator** system property. For more details on this system property and its supported values, see [AI Search system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/system-properties-ais.md).

In family releases prior to the Brazil release, applying a source facet filter to your multi-term search query can trigger query resubmission if the filter reduces your result count below the one-page threshold. For example, suppose your multi-term search query returns 17 results in an application that displays 10 results per page. In this case, your initial result count is high enough that AI Search doesn't trigger query resubmission. But if you apply a source facet filter that reduces your result count below 10, that does trigger query resubmission. This means that you might see new results less relevant to your search when applying a source facet filter.

Starting with the Brazil release, AI Search uses the search query's original result count, without any source facet filters applied, when determining whether to trigger query resubmission. This means that your query won't match additional results just because you apply a source facet filter.

If you prefer the behavior from previous family releases, allowing query resubmission to trigger when source facet filters reduce your search result count below one page's worth, you can set the value of the **glide.ais.query.sticky\_fallback** system property to **false**. This change makes the system use the filtered result count when determining whether to trigger query resubmission for multi-term search queries.

## Procedure

1.  Navigate to the System Property \[sys\_properties\] table's list view.

    1.  Select **All**.

    2.  In the navigation field, enter `sys_properties.list`.

    3.  Press Enter.

2.  Edit the **glide.ais.query.sticky\_fallback** system property record.

3.  In the System Property form's **Value** field, change **true** to **false**.

4.  Select **Update**.


## Result

The system uses the result count with source facet filters applied when determining whether to trigger query resubmission for multi-term search queries.

You can undo this change by setting the system property record's **Value** field value back to **true**.

**Parent Topic:**[Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/ai-search/configuring-ais.md)

