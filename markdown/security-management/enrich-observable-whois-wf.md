---
title: Enrich Observable WhoIs workflow
description: The Enrich Observable WhoIs workflow performs enrichment on selected observables. If the observables are of a type recognized by the WhoisXML API Integration, the observables are enriched.The Observable Enrichment Lookup workflow activity initiates the observable enrichment process.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [WhoisXML API integration, Threat Intelligence integrations, Threat Intelligence, Enterprise security case management applications, Security Operations]
---

# Enrich Observable WhoIs workflow

The **Enrich Observable WhoIs** workflow performs enrichment on selected observables. If the observables are of a type recognized by the WhoisXML API Integration, the observables are enriched.

## Before you begin

Role required: admin

## About this task

This workflow is triggered by the [Security Operations Integration- Enrich Observable capability](../../../security-operations-common/concept/enrich-observable-capability.md) when you perform enrichment on one or more observables, and the WhoIs implementation is selected.

![Enrich Observable WhoIs workflow](../image/enrich-observ-whois-wf.png "Enrich Observable WhoIs workflow")

Activities specific to this integration are described here. For more information on other activities, see [Common Security Operations integration flows and orchestration activities](../../../security-operations-common/concept/common-wf-activities.md).

## Observable Enrichment Lookup activity

The **Observable Enrichment Lookup** workflow activity initiates the observable enrichment process.

The **Observable Enrichment Lookup** activity can be used with any observables workflow to begin enrichment.

### Results

Possible results for this activity are:

|Result|Description|
|------|-----------|
|Success|The lookup is successful.|
|Fail|An error occurred while attempting to perform the lookup. More error information is available in the activity output error.|

### Input variables

Input variables determine the initial behavior of the activity.

|Variable|Description|
|--------|-----------|
|implementation\_id|System identifier of the implementation used to perform the lookup.|
|domain\_id|The domain identifier for the domain within which the lookup is being performed.|
|observable\_ids|One or more observables to perform the desired action against. The IDs are used as a workflow input.|
|capabilityExcutionId|System identifier of the capability that launched the implementation workflow. Only required for Integration Capability implementation workflows such as Splunk, Elasticsearch.|
|task\_sys\_id|System identifier for any task associated with the workflow.|

### Output variables

The output variables contain data that can be used in subsequent activities.

|Variable|Description|
|--------|-----------|
|response\_data|Raw data returned by the implementation's API endpoint for the given domain.|
|mapping\_id|The identifier for the enrichment mapping. For example, the WhoIs integration returns data in two different format, IP and URL, with a mapping id for each.|

