---
title: Migrate event data to new summary tables
description: Migrate old sensor event data from the existing tables to the new summary data tables using the OnDemandDataMigration scheduled job.
locale: en-US
release: yokohama
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Workplace Connectors data summarization, Reference, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Migrate event data to new summary tables

Migrate old sensor event data from the existing tables to the new summary data tables using the OnDemandDataMigration scheduled job.

## Before you begin

Role required: admin

## About this task

This job summarizes daily aggregated data based on specified criteria such as day-wise, location hierarchy-wise, and business entity-wise for occupancy, environment, badging, and Wi-Fi data. The summarized data is stored in the new Space Occupancy Daily Summary Data, Wi-Fi Daily Summary Data, Environmental Daily Summary Data, and Environmental Hourly Summary Data tables.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Application Search** field, enter `Workplace Connectors`.

3.  From the filtered search results, select and open the OnDemandDataMigration scheduled job.

4.  Select **Execute Now**.


**Parent Topic:**[Workplace Connectors data summarization](../concept/data-summarization.md)

**Previous topic:**[Run the DataSummarization on-demand job](run-the-datasummarization-on-demand-job.md)

**Next topic:**[Emergency Response Management](../../business-continuity/concept/emergency-response-management.md)

