---
title: Monitor an enrichment job
description: Open a submitted enrichment job to see its progress and how many suggestions are pending review, published to catalog, or rejected.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/monitor-enrichment-job-dc.html
release: australia
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [enrichment job, monitor, Data Catalog, AI metadata]
breadcrumb: [Enriching data assets with AI, Metadata enrichment with ServiceNow Otto, Data Catalog, Workflow Data Fabric]
---

# Monitor an enrichment job

Open a submitted enrichment job to see its progress and how many suggestions are pending review, published to catalog, or rejected.

## About this task

The Metadata Enrichment workspace provides a consolidated view of all enrichment activity. It includes a dashboard summary of jobs completed, in progress, and failed, along with enrichment status charts and a cross-job list of assets and fields. From the workspace, select a job ID to open and monitor a specific job.

\[Omitted image "dc-bulk-enrich-ai-workspace.png"\] Alt text: Metadata Enrichment workspace showing dashboard summary, enrichment status charts, and enrichment jobs list

## Before you begin

A bulk enrichment job has already been submitted from either ServiceNow Otto or Data Catalog. See [Bulk-enrich assets with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/bulk-enrich-assets-otto-dc.md) or [Bulk-enrich assets from the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/bulk-enrich-assets-data-catalog-dc.md).

Role required: df\_data\_steward

## Procedure

1.  Open the monitor job progress link returned when the job was created.

2.  From the enrichment job page, review the job details and suggestion counts.

    The page shows:

    -   Job details: The number of assets included, when the job started and finished, and how long it took
    -   Suggestion counts by status: The number of assets processed and how many suggestions are pending, published, or rejected
    -   Asset and field list: Each asset included in the job and the fields that were enriched
    For a description of each status, see [Data assets enrichment statuses and AI confidence scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/enrichment-job-statuses-dc.md).

3.  Select a job to open its detailed view.\[Omitted image "dc-bulk-enrich-ai-view-job-01.png"\] Alt text: Enrichment job page showing job details and suggestion counts


## Result

The job's detail view opens, listing every processed asset and field. To act on the suggestions, see [Review and publish suggested metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/review-publish-ai-metadata-dc.md).

**Parent Topic:**[Enriching data assets with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/enrich-data-assets-ai-dc.md)

