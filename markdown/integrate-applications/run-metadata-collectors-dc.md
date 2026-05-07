---
title: Running metadata collectors
description: A metadata collector run harvests technical metadata from the connected data platform and updates the Data Catalog. Collectors can run on demand or on a defined schedule. Runtime logs record the status and details of each run.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Data Catalog, Workflow Data Fabric]
---

# Running metadata collectors

A metadata collector run harvests technical metadata from the connected data platform and updates the Data Catalog. Collectors can run on demand or on a defined schedule. Runtime logs record the status and details of each run.

A metadata collector run harvests technical metadata from the connected data platform and updates the Data Catalog. Collectors can run on demand or on a defined schedule. Runtime logs record the status and details of each run.

Collectors support two run modes:

-   Manual: An immediate, on-demand run. Use this after initial setup to verify that the collector connects and collects expected metadata
-   Scheduled: A recurring run at a defined interval. Use this to keep catalog metadata current as the source system changes

![Metadata collector interface showing schedule configuration options and run summary with manual run button highlighted.](../image/dc-mcollector-run-sch.png)

-   **[Run metadata collectors manually](../task/run_metadata-collectors-manually.md)**  
Execute a metadata collector on-demand to import metadata immediately.
-   **[Schedule metadata collector runs](../task/schedule-metadata-collector-runs.md)**  
Schedule a metadata collector to run automatically at a specified frequency.
-   **[View runtime logs for collector runs](../task/view-runtime-logs-for-collector-runs.md)**  
Access execution logs and download detailed log files for metadata collector runs.

**Parent Topic:**[Data Catalog](data-catalog.md)

