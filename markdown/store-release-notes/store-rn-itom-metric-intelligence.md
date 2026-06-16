---
title: Metric Intelligence release notes
description: Version history for the Metric Intelligence application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-itom-metric-intelligence.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - ITOM AIOps release notes, ServiceNow Store - IT Operations Management release notes, ServiceNow Store release notes]
---

# Metric Intelligence release notes

Version history for the Metric Intelligence application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 2.8.0 - June 2026**

    Fixed: Minor issue in the error log registration causing some group alerts to present the metric line chart \[in Express List, preview panel\] with an error

-   **Version 2.7.11 - December 2025**
    -   New:
        -   Kafka metrics connector instance: New Kafka connector to stream time-series metric data from Kafka topics into ServiceNow Metric Intelligence for real-time monitoring, anomaly detection, and alerting.
        -   Datadog metrics connector instance: Out-of-the-box Datadog metric connector to integrate Datadog metrics with ServiceNow Metric Intelligence, enabling anomaly detection, metric visualization, enrichment, and correlation of metric anomalies with events and log alerts.
        -   Added support for multiple subscriptions of AWS account: Enable one AWS Connector instance to support multiple subscription IDs, eliminating additional instances per subscription.
        -   Dynatrace metric connector from Integrations Launchpad: Set the Dynatrace metric connector from the Integration Launchpad to bring metrics from Dynatrace into ServiceNow Metric Intelligence.
        -   Added support for SCOM 2025 version:Check SCOM 2025 compatibility with the current code, ensuring that the connector setup, alert collection, and Metric Intelligence data ingestion work seamlessly with the latest SCOM release. This helps maintain integration reliability, reduces configuration errors, and ensures smooth upgrade readiness.
    -   Fixed:
        -   Incorrect Resource Type Mapping:Fixed an issue where the CI metric resource table populated wrong values for Resource Type after Xanadu upgrade.
        -   Metric rules
            -   Resolved defect causing improper domain separation in Metric rules, ensuring correct data isolation across domains.
            -   Prevented use of unsupported virtual fields as filter criteria in Metric Rule tags
            -   Fixed an issue where Metric Rule creation failed with “Duplicate levels are not allowed” due to duplicate level values
        -   MetricBase Self-Monitor NoiseTuned self-monitoring for MetricBase connections to reduce excessive alerts and improve signal-to-noise ratio.
-   **Version 2.7.1 - August 2025**
    -   New: Exp. List Alert Preview Panel now supports a new line chart showing the metric data at the time the anomaly took place.
    -   Fixed:
        -   Resolved a problem in creating events when the static threshold is based on fields found on a CI class table
        -   Timezone changes issue fixed
-   **Version 2.6.3 - May 2025**

    Changed: The Metric Intelligence plugin will automatically pull the latest 'Advanced Promotion Engine' plugin for anomaly promotion.

-   **Version 2.5.3 - June 2024**
    -   Fixed:
        -   Fixes for translation and localization issues.
        -   Added a missing menu item.
        -   Fix auto sync of existing threshold rules with new registered metrics.
        -   Fix the CMDB relations when creating records in sa\_threshold\_map.
-   **Version 2.5.0 - February 2024**

    New: Metric Rules \(New application\) is now part of Metric Intelligence, providing new experience setting and managing alert manual thresholds for metrics. Refer to "Metric Rules" store page for more details.

-   **Version 2.2.3 - May 2023**
    -   New: Self-monitoring alerts in case metrics are not being collected.
    -   Fixed: Advanced Promotion Engine \(APE\) performance issues in scale.
-   **Version 2.0.0 - March 2023**

    New: Advanced Promotion Engine - Allows promotion of anomaly alerts to IT alerts only if they meet a set of predefined conditions

-   **Version 1.3.0 - May 2022**
    -   New: Scale and performance numbers added to documentation
    -   Fixed: Threshold crossing events don't bind to CIs

**Parent Topic:**[ServiceNow Store - ITOM AIOps release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-rn-itom-ai-ops-landing.md)

