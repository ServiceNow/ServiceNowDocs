---
title: Indexed Source History form
description: The Indexed Source History form records details of content and metadata ingestion and indexing for an AI Search indexed source. Use this form when reviewing the ingestion history for an indexed source.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer]
---

# Indexed Source History form

The Indexed Source History form records details of content and metadata ingestion and indexing for an AI Search indexed source. Use this form when reviewing the ingestion history for an indexed source.

To learn how to review the ingestion history for an indexed source, see [Review ingestion history for an indexed source](../task/review-history-indexed-source-ais.md).

<table id="table_nds_jcb_5nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Indexed Source

</td><td>

Reference to the indexed source from which AI Search ingested records for indexing.

</td></tr><tr><td>

Ingestion Event ID

</td><td>

Sys\_id of the ingestion event.

</td></tr><tr><td>

Partial Ingestion

</td><td>

Option indicating whether AI Search ingested all parent and child tables defined in the indexed source. Valid values:

-   **false**: AI Search ingested records from the indexed source table and all child tables configured for indexing.
-   **true**: AI Search only ingested records from a subset of the indexed source tables configured for indexing.

</td></tr><tr><td>

Number of Errors

</td><td>

Count of error messages logged for the ingestion event.

</td></tr><tr><td>

Number of Minor Errors

</td><td>

Count of minor error messages logged for the ingestion event.

</td></tr><tr><td>

Number of Warnings

</td><td>

Count of warning messages logged for the ingestion event.

</td></tr><tr><td>

Ingestion State

</td><td>

State for the ingestion event. Valid values:

-   **cancelled**: Ingestion and indexing didn't complete successfully.
-   **indexed**: Ingestion and indexing completed successfully.
-   **indexing**: Ingestion and indexing are ongoing.
-   **not\_started**: Ingestion and indexing are pending.

</td></tr><tr><td>

Start Time

</td><td>

System time at which the ingestion event began.

</td></tr><tr><td>

End Time

</td><td>

System time at which the ingestion event completed.

</td></tr><tr><td>

Content Preparation Duration

</td><td>

Total time that the ServiceNow AI Platform® spent retrieving source records for the ingestion event.

</td></tr><tr><td>

Indexing Duration

</td><td>

Total time that AI Search spent indexing source records for the ingestion event.

</td></tr><tr><td>

Records Processed

</td><td>

Count of source records processed for the ingestion event.

</td></tr><tr><td>

Attachments Processed

</td><td>

Count of source record attachments processed for the ingestion event.

</td></tr><tr><td>

Documents Processed per Second \(DPS\)

</td><td>

Average number of source records and attachments processed per second for the ingestion event.

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

