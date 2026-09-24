---
title: Log Export Service release notes
description: The ServiceNow Log Export Service application provides scalable, near real-time integration with analytic tools for security threat detection, performance optimization, and user experience monitoring. See the following sections for release notes by version.This release expands the security and compliance data you can export and makes setup verification safer by adding on-demand historical log back-fill for Kafka destinations, four new log source tables, a read-only sn\_logstoanalytics.auditor role, and a Test MID Connection step in guided setup that confirms Kafka connectivity before exporting logs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/log-export-service-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Log Export Service release notes

The ServiceNow® Log Export Service application provides scalable, near real-time integration with analytic tools for security threat detection, performance optimization, and user experience monitoring. See the following sections for release notes by version.

## About Log Export Service

-   Detect security threats and analyze security incidents by exporting your instance system and application logs into your enterprise security analytics tools.
-   Troubleshoot and optimize application performance and user experience by forwarding your instance log events in near real-time to your analytics solutions.
-   Manage and export large volumes of log events through highly scalable integration that's quick to set up with guided setup.
-   Connect to your analytics tools using a dedicated MID Server, a Kafka connector from your analytics solution, or a direct Kafka connection.

See [Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-intro.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Log Export Service by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[ServiceNow AI Platform security release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-security-rn-landing.md)

## Version 3.6

This release expands the security and compliance data you can export and makes setup verification safer by adding on-demand historical log back-fill for Kafka destinations, four new log source tables, a read-only sn\_logstoanalytics.auditor role, and a Test MID Connection step in guided setup that confirms Kafka connectivity before exporting logs.

### What's new

-   **[Historical log back-fill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-export-existing-logs-on-demand.md)**

    You can now replay historical log data to your Kafka destination, in addition to live logs. A new setup screen lets you select the log table, date range, target topic, batch size, and throttling. Backfill settings are locked once a run begins to prevent accidental changes mid-run, and a live run status is displayed while the backfill is in progress.

-   **Broader log coverage**

    LES now supports the following additional log source tables:

    -   sys\_flow\_log: Captures execution details and status of flow engine processes, for both live and historical export
    -   sys\_user\_login\_history: Captures user login attempts and authentication events
    -   Delete and relationship audit records \(sys\_audit\_delete and sys\_audit\_relation\) - so your compliance trail now includes record deletions and reference-field changes, not just regular field changes

### What's changed

-   **[Enhanced guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-configure.md)**
    -   Guided setup now includes a Test MID Connection step, so you can verify connectivity to the Kafka cluster before exporting logs catching configuration problems earlier.

