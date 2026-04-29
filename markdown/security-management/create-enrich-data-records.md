---
title: Create Enrichment Data records Flow Action
description: The Create enrichment data records flow action creates or updates enrichment records to use in the flow.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common Security Operations integration flows and orchestration activities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Create Enrichment Data records Flow Action

The **Create enrichment data records** flow action creates or updates enrichment records to use in the flow.

The **Create Enrichment Data records** flow action can be used with any flow to update enrichment records in the flow.

## Results

Possible results for this flow action are:

|Result|Description|
|------|-----------|
|Success|Enrichment record updated.|
|Failure|Enrichment record not updated. More error information is available in the flow action output error.|

## Input variables

Input variables determine the initial behavior of the flow action.

|Variable|Description|
|--------|-----------|
|task\_id|Task identifier.|
|content|Raw content \(running processes data\).|
|enrichment\_mapping\_id|Enrichment mapping identifier.|
|ci\_id|Configuration item identifier.|
|reference\_value|Unused.|

## Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|result|GlideRecords created using the enrichmentUtils script.|

**Parent Topic:**[Common Security Operations integration flows and orchestration activities](common-wf-activities.md)

