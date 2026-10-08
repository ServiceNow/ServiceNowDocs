---
title: Metadata enrichment with ServiceNow Otto
description: ServiceNow Otto can generate AI-suggested metadata for a batch of Data Catalog assets for a data steward to review and publish.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/ai-metadata-enrichment-overview-dc.html
release: australia
topic_type: concept
last_updated: "2026-09-17"
reading_time_minutes: 2
keywords: [AI metadata enrichment, Otto, Data Catalog, bulk enrichment, data steward]
breadcrumb: [Data Catalog, Workflow Data Fabric]
---

# Metadata enrichment with ServiceNow Otto

ServiceNow Otto can generate AI-suggested metadata for a batch of Data Catalog assets for a data steward to review and publish.

Data Catalog assets accumulate incomplete or missing metadata over time —domains, tags, and glossary-term associations— especially as new sources are onboarded through metadata collectors. Filling this in one asset at a time is not practical. ServiceNow Otto can generate suggested metadata for many assets at once, as a tracked, asynchronous job. Nothing changes in the catalog until a data steward reviews the suggestions and chooses to publish them.

## Entry points

Start a bulk enrichment job two ways — from ServiceNow Otto, using the assistant icon available in the Workflow Data Fabric header, or directly from the Data Catalog page. Both entry points create the same kind of job and route to the same review workspace. For step-by-step instructions, see [Bulk-enrich assets with ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/bulk-enrich-assets-otto-dc.md) and [Bulk-enrich assets from the Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/bulk-enrich-assets-data-catalog-dc.md).

\[Omitted image "dc-bulk-enrich-with-ai.png"\] Alt text: Enrich data assets with AI

## How it works

Enrichment jobs run asynchronously, in the background, and can take from a few minutes to a few hours depending on the number of assets and fields included. You're notified by email when the job finishes.

Every suggestion includes an AI confidence score and stays in a pending state. Submitting a job doesn't enrich assets immediately — a suggestion has no effect on the actual asset until a data steward reviews and either publishes or rejects it. For a list of job statuses and their meanings, see [Data assets enrichment statuses and AI confidence scores](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/enrichment-job-statuses-dc.md). \[Omitted image "dc-bulk-enrich-ai-view-job-01.png"\] Alt text: Enrichment job page showing job details and suggestion counts

## Metadata Enrichment workspace

The Metadata Enrichment workspace gives a consolidated view of all enrichment activity across jobs. Use it to track the overall enrichment program rather than a single job.

The workspace includes:

-   A dashboard summary showing the number of jobs completed, in progress, and failed
-   Asset enrichment status and metadata field enrichment status charts, showing counts across all jobs
-   An enrichment jobs list with job status, asset counts, and duration for each job
-   An enrichment assets and fields list, grouped by job, where you can select a job ID, asset ID, or field ID to review enrichments at the level of detail you need

\[Omitted image "dc-bulk-enrich-ai-workspace.png"\] Alt text: Metadata Enrichment workspace showing dashboard summary, enrichment status charts, and enrichment jobs list

## Prerequisites

This capability requires ServiceNow Otto to be configured and Data Catalog to be installed.

