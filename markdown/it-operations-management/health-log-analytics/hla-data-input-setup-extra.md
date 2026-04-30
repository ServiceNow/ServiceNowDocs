---
title: Additional data input setup tasks in Health Log Analytics
description: After performing the initial data input setup and configuration in Health Log Analytics, continue with the remaining data input setup tasks.
locale: en-US
release: zurich
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up data inputs manually, Set up HLA on your instance, Configuring, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Additional data input setup tasks in Health Log Analytics

After performing the initial data input setup and configuration in Health Log Analytics, continue with the remaining data input setup tasks.

-   **[Add a timestamp format in Health Log Analytics](../task/hla-timestamp-formats-add.md)**  
Define any timestamp format that does not appear in the list of defined formats. Health Log Analytics must be able to read timestamps of any format contained in your log files.
-   **[Add a source type manually in Health Log Analytics](../task/hla-source-types-manual.md)**  
Create a source type manually before you configure a data input if you want to stream log data to a specific source type rather than to the source type automatically extracted by Health Log Analytics during the mapping process.
-   **[Configure source type capabilities in Health Log Analytics](../task/hla-source-types.md)**  
Health Log Analytics extracts source types automatically in the mapping process. You can add timestamp formats and specify, delete, or exclude keywords for individual source types.
-   **[Verify your log sources in Health Log Analytics](../task/hla-log-sources-review.md)**  
Verify that all your log sources are present and active after Health Log Analytics tagging has assigned a log to a service instance and components, and has automatically mapped the log to a source.
-   **[Delete a log source in Health Log Analytics](../task/hla-log-source-delete.md)**  
Delete a log source with or without its associated log data in Health Log Analytics.
-   **[Review properties extracted from a source type in Health Log Analytics](../task/hla-sts-properties-table.md)**  
Inspect the properties that were extracted from all the source types in a source type structure in a single table to identify any setup issues.
-   **[Review patterns extracted from a source type in Health Log Analytics](../task/hla-view-source-type-patterns.md)**  
Inspect all learned patterns extracted from a source type in a source type structure, together with the log sources in which these patterns appeared. Reviewing these patterns can provide valuable insights into the log message patterns that Health Log Analytics tracks for each source type and log source.
-   **[Modify a data input configuration in Health Log Analytics](../task/hla-data-input-modify.md)**  
Change the configuration of a data input for Health Log Analytics by adding a new path to an existing data input configuration or modifying the data input's MID Server destination and port.

**Parent Topic:**[Set up data inputs in Health Log Analytics manually](../task/hla-data-input-setup-manual.md)

