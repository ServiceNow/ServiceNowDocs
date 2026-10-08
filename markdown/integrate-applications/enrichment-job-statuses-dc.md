---
title: Data assets enrichment statuses and AI confidence scores
description: Enrichment statuses track the state of AI-generated suggestions at the field, asset, and enrichment run levels. Each suggestion also carries a confidence score that reflects how certain ServiceNow Otto is about that suggestion.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/enrichment-job-statuses-dc.html
release: brazil
topic_type: reference
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [enrichment job, statuses, AI confidence score, Data Catalog]
breadcrumb: [Reference, Data Catalog, Workflow Data Fabric]
---

# Data assets enrichment statuses and AI confidence scores

Enrichment statuses track the state of AI-generated suggestions at the field, asset, and enrichment run levels. Each suggestion also carries a confidence score that reflects how certain ServiceNow Otto is about that suggestion.

## Enrichment job statuses

|Status|Description|
|------|-----------|
|Processing|Number of jobs currently generating enrichment recommendations.|
|Completed|Number of jobs where review is finished with nothing published — every field was rejected or had no recommendation.|
|Cancelled|Number of jobs stopped by a Data Steward before completion.|

## Data asset enrichment statuses

|Status|Description|
|------|-----------|
|Recommended|Enrichment recommendations have been generated for the requested fields on this asset.|
|Error|Enrichment generation failed for one or more fields on this asset.|
|Pending review|One or more field recommendations on this asset are awaiting Data Steward or Asset Owner review.|
|Partially accepted|Some field recommendations on this asset were accepted and published to the data catalog; the remainder were rejected.|
|Rejected|All AI-generated field recommendations on this asset were rejected by the Data Steward or Asset Owner.|
|Published|All AI-generated field recommendations on this asset were published to the data catalog.|

## Field enrichment statuses

|Status|Description|
|------|-----------|
|Pending review|AI-generated enrichment suggestions are awaiting validation by the Data Steward or Asset Owner.|
|Published|AI-generated enrichment recommendations have been reviewed, approved, and published to the data catalog.|
|Rejected|AI-generated enrichment suggestions rejected by the Data Steward or Asset Owner.|
|No recommendation|No enrichment recommendations were generated for this field due to insufficient information or context.|

## AI confidence scores

Every suggestion carries a confidence score, shown alongside its previous and suggested values, so a data steward can judge how much to trust it before publishing or rejecting.

**Parent Topic:**[Data catalog reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/data-catalog-reference.md)

