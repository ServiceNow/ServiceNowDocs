---
title: Review record counts for indexed sources
description: Understand where your indexed content originates by viewing record counts for your indexed sources in the AI Search Indexed Source Statistics table.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Review record counts for indexed sources

Understand where your indexed content originates by viewing record counts for your indexed sources in the AI Search Indexed Source Statistics table.

## Before you begin

Role required: ais\_admin

## About this task

The AI Search Indexed Source Statistics \[ais\_datasource\_stats\] table contains entries showing the indexed record counts for each of your indexed sources. These entries are logged every 24 hours by the **AIS Collect Ingestion Stats** scheduled job. You can review the statistics entries to see how many records each indexed source contributes to the AI Search index.

## Procedure

1.  Navigate to the AI Search Indexed Source Statistic \[ais\_datasource\_stats\] table's list view.

    1.  Select **All**.

    2.  In the **Filter** field, enter `ais_datasource_stats.list`.

    3.  Press Enter.

2.  If the Updated field doesn't appear, select the Personalize List icon ![](../../../common/image/gear.png) and use the slushbucket to add the Updated field to the list view.

3.  To display the most recent indexed record-count entries first, select the Updated field's column options icon ![](../image/polaris-ui-column-options-header.png) in Next Experience UI or ![](../image/ui16-column-options-header.png), then select **Sort \(z to a\)**.

4.  Review the indexed record-count entries for each of your indexed sources.

    **Note:** The entry for an indexed source indicates the number of indexed records from that source when the **AIS Collect Ingestion Stats** scheduled job ran at the time listed in the Updated field.


**Parent Topic:**[Administering AI Search](../concept/administer-ais.md)

