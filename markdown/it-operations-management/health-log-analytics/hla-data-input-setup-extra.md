---
title: Additional data input setup tasks
description: After performing the initial data input setup and configuration, continue with the remaining data input setup tasks.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Health Log Analytics on your ServiceNow instance, Configuring Health Log Analytics, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Additional data input setup tasks

After performing the initial data input setup and configuration, continue with the remaining data input setup tasks.

-   **[Add timestamp formats](../task/hla-timestamp-formats-add.md)**  
Define any timestamp format that does not appear in the list of defined formats. Health Log Analytics must be able to read timestamps of any format contained in your log files.
-   **[Add source types manually](../task/hla-source-types-manual.md)**  
Create a source type manually before you configure a data input if you want to stream log data to a specific source type rather than to the source type automatically extracted by Health Log Analytics during the mapping process.
-   **[Configure source type capabilities](../task/hla-source-types.md)**  
Health Log Analytics extracts source types automatically in the mapping process. You can add timestamp formats and specify, delete, or exclude keywords for individual source types.
-   **[Verify your log sources](../task/hla-log-sources-review.md)**  
Verify that all your log sources are present and active after Health Log Analytics tagging has assigned a log to a service instance and components, and has automatically mapped the log to a source.
-   **[Review the properties extracted from a source type in Health Log Analytics](../task/hla-sts-properties-table.md)**  
View the properties that were extracted from all the source types in a source type structure in a single table to identify any setup issues.
-   **[Review the patterns extracted from a source type in Health Log Analytics](../task/hla-view-source-type-patterns.md)**  
View all learned patterns extracted from a source type in a source type structure, together with the log sources in which these patterns appeared. Reviewing these patterns can provide valuable insights into the log message patterns that Health Log Analytics tracks for each source type and log source.
-   **[Delete a log source](../task/hla-log-source-delete.md)**  
Delete a log source with or without its associated log data in Health Log Analytics.
-   **[Modify data input configurations](../task/hla-data-input-modify.md)**  
Modify the configuration of a data input for Health Log Analytics by adding a new path to an existing data input configuration or changing the data input's MID Server destination and port.

**Parent Topic:**[Setting up Health Log Analytics on your ServiceNow instance](hla-implement.md)

