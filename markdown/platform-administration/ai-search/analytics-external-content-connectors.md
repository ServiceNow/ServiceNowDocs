---
title: Analytics for external content connectors
description: Metrics that show how your external content connector has run over time.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-10-23"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Reference, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Analytics for external content connectors

Metrics that show how your external content connector has run over time.

You can view analytics for an external content connector by navigating to the **Analytics** tab in the connector editor. For more details on this procedure, see [Review analytics for an external content connector](../task/review-analytics-external-content-connector.md).

## Date range

Use the **Date range** interactive filter to specify the reporting time period for all external content connector analytics reported on this page.

## Document statistics

<table id="table_ohq_4zv_5gc"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Documents indexed

</td><td>

**Timeseries visualization:** Graph shows the number of items \(documents with searchable content and metadata\) the connector retrieved that were included in the AI Search index for each date in the selected date range.

</td></tr><tr><td>

Quota usage

</td><td>

**Single score with progress bar:**-   First value shows the number of items the connector retrieved that are currently included in the AI Search index.

**Note:** Deleted items are not deducted from this quota usage figure.

-   Second value shows the indexing limit for the connector.
-   Progress bar shows how close the connector is to its indexing limit.

</td></tr><tr><td>

New

</td><td>

**Single score with trend:**-   Score shows the number of new items the connector added to the AI Search index in the selected date range.
-   Trend shows how this score changed in the selected date range as compared with the previous time period.

</td></tr><tr><td>

Updated

</td><td>

**Single score with trend:**-   Score shows the number of items the connector updated in the AI Search index \(to reflect content and metadata changes\) in the selected date range.
-   Trend shows how this score changed in the selected date range as compared with the previous time period.

</td></tr><tr><td>

Discovered

</td><td>

**Single score with trend:**-   Score shows the number of items the connector processed in the selected date range.
-   Trend shows how this score changed in the selected date range as compared with the previous time period.

</td></tr><tr><td>

Indexed

</td><td>

**Single score with trend:**-   Score shows the number of items the connector fed to the AI Search index in the selected date range.
-   Trend shows how this score changed in the selected date range as compared with the previous time period.

</td></tr><tr><td>

Deleted

</td><td>

**Single score with trend:**-   Score shows the number of items the connector deleted from the AI Search index in the selected date range.
-   Trend shows how this score changed in the selected date range as compared with the previous time period.

</td></tr><tr><td>

Skipped

</td><td>

**Single score with trend:**-   Score shows the number of items skipped due to processing errors in the selected date range.

**Note:** This number does not include items excluded by crawl settings specified for the connector.

-   Trend shows how this score changed in the selected date range as compared with the previous time period.

</td></tr></tbody>
</table>## Crawl statistics

<table id="table_qxy_4zv_5gc"><thead><tr><th>

Metric

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Crawls executed

</td><td>

**Timeseries visualization:**-   Histogram area chart shows the number of successful crawls run for the connector for each date in the selected date range.
-   Histogram line chart shows the number of failed crawls run for the connector for each date in the selected date range.

Select an individual crawl's name from the histogram legend to hide its entries from the histogram or display them again.

</td></tr><tr><td>

Document crawls

</td><td>

**Dual score:**-   First value shows the number of successful content crawls run for the connector in the selected date range.
-   Second value shows the number of failed content crawls run for the connector in the selected date range.

</td></tr><tr><td>

User permission crawls

</td><td>

**Dual score:**-   First value shows the number of successful user permission crawls run for the connector in the selected date range.
-   Second value shows the number of failed user permission crawls run for the connector in the selected date range.

</td></tr></tbody>
</table>**Parent Topic:**[External Content Connectors reference](../concept/reference-ext-cont-connectors.md)

