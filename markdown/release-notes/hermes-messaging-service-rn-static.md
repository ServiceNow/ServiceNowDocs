---
title: Hermes Messaging Service release notes
description: The ServiceNow Hermes application delivers asynchronous event streaming and messaging capabilities for enterprise workflows. See the following sections for release notes by version.The ServiceNow Hermes application delivers asynchronous event streaming and messaging capabilities for enterprise workflows. Hermes was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/hermes-messaging-service-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Hermes, messaging service, real-time messaging, Hermes, messaging, usage tracking, reporting, Application ID, topic retention]
breadcrumb: [ServiceNow AI Platform capabilities release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Hermes Messaging Service release notes

The ServiceNow® Hermes application delivers asynchronous event streaming and messaging capabilities for enterprise workflows. See the following sections for release notes by version.

## About Hermes

-   Delivers asynchronous event streaming and messaging capabilities for enterprise workflows.
-   Enables scalable message delivery across distributed systems with configurable retention policies.
-   Provides comprehensive usage tracking and reporting for messaging operations.
-   Supports integration with applications such as Instance Data Replication and Log Export Service.

See [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/hermes-messaging-service.md) for more information.

## Activation and other requirements

-   **Activation information**

    Hermes is a ServiceNow AI Platform feature that is available with activation of the ServiceNow Stream Connect Installer \(com.glide.hub.stream\_connect.installer\) plugin or the installation of the Log Export Service application.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-capabilities-rn-landing.md)

## Brazil Early Availability

The ServiceNow® Hermes application delivers asynchronous event streaming and messaging capabilities for enterprise workflows. Hermes was enhanced and updated in the Brazil release.

### What's new

-   **Configurable topic retention period**

    Define custom retention policies for Hermes topics directly within Hermes Topic Manager to enable flexible data lifecycle management aligned with organizational compliance requirements and storage optimization strategies.

-   **Simplified topic options**

    Streamline the administrative user interface with renamed and simplified topic options during topic setup and management.

    See [Monitoring data usage in Hermes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/monitoring-data-usage-hermes.md).

-   **Enhanced Application ID filtering**

    Improve usability with full descriptive names in the Application ID drop-down instead of abbreviated codes, and enable concurrent filtering across multiple Application IDs within a single usage query.

-   **Explicit external topic labeling**

    Distinguish external topics from internal topics in the Hermes usage dashboard to eliminate confusion during usage analysis and reporting of cross-organization messaging patterns.

-   **Long-term usage data tracking**

    Enable comprehensive trend analysis and capacity planning across longer time horizons with expanded usage data collection and retention infrastructure for enterprise messaging operations.


### What's changed

-   **Empty Application ID handling**

    Topics created without an explicit Application ID are now correctly filtered and labeled in usage data queries. Previously, these topics would incorrectly appear in results when the "all values" filter selection was applied.

-   **Extended date range query processing**

    Usage data queries now return accurate results for date ranges exceeding two months. Previously, queries spanning more than two months would display incorrect or corrupted data, limiting historical analysis capabilities.

-   **Topic namespace parsing**

    Metrics collection now correctly parses Hermes topics without requiring explicit namespace definitions. This resolves parsing failures that previously occurred during topic analysis in the metrics collection pipeline.


