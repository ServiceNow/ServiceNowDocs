---
title: Telecommunications Service Operations Management \(TSOM\) release notes
description: The ServiceNow Telecommunications Service Operations Management \(TSOM\) application empowers communication service providers to proactively monitor, analyze, and resolve network and service issues before they impact customers. See the following sections for release notes by version.Monitor Mobile Private Network \(MPN\) performance with new connectors for latency, security logs, and health status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/telecommunications-service-operations-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [MPN, Mobile Private Network, latency, RAG status, security log]
breadcrumb: [Telecommunications, Media, and Technology release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Telecommunications Service Operations Management \(TSOM\) release notes

The ServiceNow® Telecommunications Service Operations Management \(TSOM\) application empowers communication service providers to proactively monitor, analyze, and resolve network and service issues before they impact customers. See the following sections for release notes by version.

## About Telecommunications Service Operations Management

-   Proactively identify and resolve network and service issues before they impact customers, reducing mean time to detect \(MTTD\) and mean time to resolve \(MTTR\).
-   Gain end-to-end visibility into how network and infrastructure issues affect customer-facing services, and prioritize remediation based on business impact.
-   Reduce operational noise and streamline resolution with event correlation, guided workflows, and automated remediation.
-   Integrate seamlessly with existing network monitoring and telemetry systems using open standards and TM Forum-aligned APIs.
-   Build and maintain a telecom-aware CMDB that links infrastructure, services, and configuration items for accurate root cause analysis.

See [Exploring Telecommunications Service Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/exploring-tsom.md) for more information.

## Activation and other requirements

**Note:** Telecommunications Service Operations Management is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Request and activate the Telecommunications Service Operations Management \(com.sn\_tsom\_core\) plugin. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Accessibility information**
    -   Telecommunications Service Operations Management follows standard ServiceNow AI Platform accessibility support, including keyboard navigation and compatibility with screen readers.
-   **Localization information**

    Telecommunications Service Operations Management does not include dedicated language packs. Language support relies on the base system language plugins active on your instance.


**Parent Topic:**[Telecommunications, Media, and Technology release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/technology-industry-rn-landing.md)

## Version 4.0

Monitor Mobile Private Network \(MPN\) performance with new connectors for latency, security logs, and health status.

### What's new

-   **[Elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/configure-mpn-connectors-for-events-and-metrics.md)**

    Collect metrics, including latency KPIs, from Nokia Med, Elastic, Prometheus, and Netcool KPI domains using a configurable Mobile Private Network \(MPN\) pull connector. Published metrics feed assurance monitoring and analytics.

-   **[MPN Latency Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/mpn-latency-dashboard.md)**

    Monitor UE-to-switch latency and related KPIs across MPN-connected devices with combined and per-KPI trend views, an instance summary table, and a last-recorded-value panel.

-   **[Security log collection for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/configure-security-log-collection-for-mpn.md)**

    Collect MPN security logs with an out-of-box Health Log Analytics Elasticsearch data input. Raw logs are converted into structured log records for triage and analysis.

-   **[MPN health status collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/configure-mpn-rag-status-collection.md)**

    Collect and aggregate red/amber/green health status from MPN Elastic index data at the tower and site level. Customize rules for calculating status based on your requirements.


### What's changed

-   **[Fortinet discovery with large port counts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-service-ops/telecom-discovery-via-fortinet.md)**

    Fortinet devices with more than 600 ports no longer fail discovery due to memory constraints. Ports are now processed in batches to prevent out-of-memory errors.


