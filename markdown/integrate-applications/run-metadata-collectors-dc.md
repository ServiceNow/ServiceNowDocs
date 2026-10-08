---
title: Running metadata collectors
description: A metadata collector run harvests technical metadata from the connected data platform and updates the Data Catalog. Collectors can run on demand or on a defined schedule. Runtime logs record the status and details of each run.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/run-metadata-collectors-dc.html
release: australia
topic_type: concept
last_updated: "2026-09-25"
reading_time_minutes: 1
keywords: [metadata collector notifications, collector run notification, run completed, run failed]
breadcrumb: [Data Catalog, Workflow Data Fabric]
---

# Running metadata collectors

A metadata collector run harvests technical metadata from the connected data platform and updates the Data Catalog. Collectors can run on demand or on a defined schedule. Runtime logs record the status and details of each run.

Collectors support two run modes:

-   Manual: An immediate, on-demand run. Use this after initial setup to verify that the collector connects and collects expected metadata.
-   Scheduled: A recurring run at a defined interval. Use this to keep catalog metadata current as the source system changes.

\[Omitted image "dc-mcollector-run-sch.png"\] Alt text: Metadata collector interface showing schedule configuration options and run summary with manual run button highlighted.

## Run notifications

When a collector run completes or fails, the platform sends an email notification to the collector owner and any subscribers. Notifications use the ServiceNow Notification framework — no custom setup is required.

Notifications appear under the **Collector Run Notification** category in **Preferences** &gt; **System notifications**, alongside other platform categories such as Connect. Two notifications are available:

-   **DCG Metadata Collector Run Completed**: Sent when a collector run succeeds.
-   **DCG Metadata Collector Run Failed**: Sent when a collector run fails.

Email is the only supported delivery channel. Opt in or out and manage your subscription through the standard Notification preferences UI. For steps, see [Subscribe to metadata collector run notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/subscribe-to-collector-run-notifications.md).

-   **[Run metadata collectors manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/run_metadata-collectors-manually.md)**  
Execute a metadata collector on-demand to import metadata immediately.
-   **[Schedule metadata collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/schedule-metadata-collector-runs.md)**  
Schedule a metadata collector to run automatically at a specified frequency.
-   **[View runtime logs for collector runs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/view-runtime-logs-for-collector-runs.md)**  
Access execution logs and download detailed log files for metadata collector runs.
-   **[Subscribe to metadata collector run notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/subscribe-to-collector-run-notifications.md)**  
Opt in to email notifications for metadata collector run completion and failure through Notification preferences.

**Parent Topic:**[Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/data-catalog.md)

