---
title: Health Log Analytics release notes
description: The ServiceNow Health Log Analytics application predicts IT issues before they affect users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you to a possible business-impacting issue. See the following sections for release notes by version.This release enables operators to suppress noisy short-lived anomaly spikes and focus only on continuous issues, and includes enhancements to Smart Parser Gen AI reliability and testing. In addition, admins with access to the ITOM MCP Server Console can use an AI-enabled MCP Client to set up MID-less integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/health-log-analytics-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Health Log Analytics, HLA, release notes, Health Log Analytics, HLA, September 2026, release notes, Sustained Alert, Smart Parser]
breadcrumb: [ITOM AIOps release notes, IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Health Log Analytics release notes

The ServiceNow® Health Log Analytics application predicts IT issues before they affect users by ingesting, analyzing, and correlating machine-generated log data in real time. When Health Log Analytics detects a deviation from a normal pattern, it alerts you to a possible business-impacting issue. See the following sections for release notes by version.

## About Health Log Analytics

-   Stay ahead of issues with predictive alerts based on anomaly detection.
-   Detect anomalous behavior automatically with log analytics alert rules.
-   Reduce mean time to resolution by accelerating root cause analysis with contextual log data.
-   Simplify log ingestion by processing high-volume log data at scale.
-   Uncover patterns in log data using built-in AI and ML.

See [Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-landing-page.md) for more information.

## Activation and other requirements

**Note:** Health Log Analytics is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Install Health Log Analytics by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


## Accessibility and localization

-   **Localization information**

    The current available languages for Health Log Analytics are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


**Parent Topic:**[ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/itom-aiops-rn.md)

## Version 40.4.0

This release enables operators to suppress noisy short-lived anomaly spikes and focus only on continuous issues, and includes enhancements to Smart Parser Gen AI reliability and testing. In addition, admins with access to the ITOM MCP Server Console can use an AI-enabled MCP Client to set up MID-less integrations.

### What's new

-   **[Sustained Alert feedback](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-sustained-alert-apply.md)**

    Suppress alerts on short-lived anomaly spikes and receive notifications only when an issue persists continuously. Apply Sustained Alert feedback per metric from the Alert Card or Express List \(single or bulk\), setting a fixed duration threshold to define what counts as sustained.

-   **[Smart Parser Gen AI enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-source-type-structure-adjustment.md)**

    Increase confidence in Smart Parser Gen AI alerts by viewing the full parsing and alert generation flow, now backed by expanded automated testing.

-   **[MID-less integration setup through an MCP Client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/hla-mid-less-integrations-concept.md)**

    Admins with access to the ITOM MCP Server Console can use an AI-enabled MCP Client to set up MID-less integrations. You can use any MCP Client, such as AWS Claude, to create MID-less integrations through natural-language prompts, without navigating to the Integrations Launchpad.


### What's changed

-   **ServiceNow Otto®**

    ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Health Log Analytics. Your product entitlements remain unchanged. Check your entitlements to determine whether you have access to specific features.

-   **Health Log Analytics migration to LogDB for log storage**

    Health Log Analytics stores short-term troubleshooting logs in LogDB instead of Elasticsearch for significantly better compression and faster ingestion. No action is required from your organization. Alerts generated before the transition still appear, but their surrounding logs aren't available because existing log data remains in Elasticsearch. New logs generated after the switch populate normally. If you notice anything unexpected, contact ServiceNow support.


