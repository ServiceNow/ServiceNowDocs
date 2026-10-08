---
title: Review and publish suggested metadata
description: Compare ServiceNow Otto's suggested values against previous values, correct anything that needs it, then publish or reject the suggestions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/review-publish-ai-metadata-dc.html
release: brazil
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [AI metadata, review, publish, Data Catalog, data steward]
breadcrumb: [Enriching data assets with AI, Metadata enrichment with ServiceNow Otto, Data Catalog, Workflow Data Fabric]
---

# Review and publish suggested metadata

Compare ServiceNow Otto's suggested values against previous values, correct anything that needs it, then publish or reject the suggestions.

## Before you begin

Role required: df\_data\_steward

## About this task

Every row in the job's field list shows an asset, a field name, the field's previous value \(if they exist\), the suggested value, and an AI confidence score. You can review at the job level, or drill into a single asset or a single field for the same information and the same actions. You can also reach individual job, asset, and field records directly from the Metadata Enrichment workspace, which provides a consolidated view across all jobs.

**Warning:** AI-generated suggestions may be inaccurate. Review each suggestion carefully before publishing. Published suggestions update Data Catalog assets immediately.

## Procedure

1.  Open an enrichment job.

    \[Omitted image "dc-bulk-enrich-ai-view-job-01.png"\] Alt text: Enrichment job page showing job details and suggestion counts

2.  From the Enrichment fields tab, review the suggested values against the previous values and the AI confidence score.

3.  To see the full asset details before accepting or rejecting a suggestion, select an asset ID to open the enrichment asset record, then select **View asset in catalog**.

    \[Omitted image "dc-bulk-enrich-ai-view-job-02.png"\] Alt text: Enrichment fields tab showing suggested values, previous values, and AI confidence scores

    The asset opens in the Data Catalog in a new tab.

4.  If a suggestion needs a change, select it, edit the value inline, and save.

5.  Select the suggestions you want to act on.

6.  Choose one of the following actions.

    -   Select **Publish selected** to write the selected values to their Data Catalog assets.
    -   Select **Reject selected** to discard the selected suggestions without changing the catalog.

## Result

Published suggestions update their Data Catalog assets and drop off the pending list. See [Data assets enrichment statuses and AI confidence scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/enrichment-job-statuses-dc.md).

**Parent Topic:**[Enriching data assets with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/enrich-data-assets-ai-dc.md)

