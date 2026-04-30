---
title: Security Operations Integration - Sightings Search Flow
description: Security Operations Integration - Sightings Search flow is a high-level flow independent of integrations. It uses the configured queries to search for a set of observables based on the configured integrations which support the capability. Use it to fulfill an integration such as Splunk or Elasticsearch.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create sightings search configuration records, Security Operations Integration- Sightings Search capability, Integration capabilities, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration - Sightings Search Flow

**Security Operations Integration - Sightings Search** flow is a high-level flow independent of integrations. It uses the configured queries to search for a set of observables based on the configured integrations which support the capability. Use it to fulfill an integration such as Splunk or Elasticsearch.

## Before you begin

Role required: sn\_si.analyst

## About this task

If a security incident has an observable attached to it, this flow is triggered when you click on **Run Sighting Search** in the **Actions on selected rows...** drop-down menu in the **Security Incident Observables** tab.

![Flow design for Security Operations Integration- Sightings Search](../image/integration-sightings-search.png "Sightings Search")

Activities specific to this flow are described here. For more information on other activities, see [Common Security Operations integration flows and orchestration activities](../../security-operations-common/concept/common-wf-activities.md).

-   **[Sightings Search - Determine Observables activity](../reference/determine-observables-sightings-search-activity.md)**  
The **Sightings Search - Determine Observables** workflow activity determines which observables to include in the workflow.
-   **[Persistent Observable Sightings activity](../reference/persistent-observable-sightings-activity-arcsight-wf.md)**  
The **Persistent Observable Sightings** workflow activity retrieves observables from the third-party integration.
-   **[Get Observable Sightings Queries activity](../reference/get-observable-sightings-queries-activity.md)**  
The **Get Observable Sightings Queries** workflow activity retrieves queries from the integration configuration.
-   **[Security Operations - Arcsight Logger Sightings Search Flow](../concept/secops-integration-sightings-search-arcsight-workflow.md)**  
**Security Operations - ArcSight Logger Sightings Search** flow is the implementation for the Splunk integration launched by the **Security Operations Integration - Sightings Search Flow**.
-   **[Security Operations - Elasticsearch Sightings Search Flow](../concept/secops-integration-sightings-search-es-workflow.md)**  
**Security Operations - Elasticsearch Sightings Search** flow is the Elasticsearch implementation launched by the **Security Operations Integration - Sightings Search** flow.
-   **[Security Operations - McAfee ESM Sightings Search Flow](../concept/secops-integration-sightings-search-mcafee-workflow.md)**  
**Security Operations - McAfee ESM Sightings Search** flow is the implementation for the McAfee Sighting Search implementation launched by the **Security Operations Integration - Sightings Search Flow**.
-   **[Security Operations - QRadar Sightings Search Flow](../concept/secops-integration-sightings-search-qradar-workflow.md)**  
**Security Operations - QRadar Sightings Search** flow is the implementation for the IBM QRadar integration launched by the **Security Operations Integration - Sightings Search flow**.
-   **[Security Operations Integration - Splunk Sightings Search Flow](../concept/secops-integration-sightings-search-splunk-workflow.md)**  
**Security Operations - Splunk Sightings Search** flow is the implementation for the Splunk integration launched by the **Security Operations Integration - Sightings Search flow**.

**Parent Topic:**[Create sightings search configuration records](../../security-incident-response/task/sightings-search-configurations.md)

