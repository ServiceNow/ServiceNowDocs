---
title: Migrate event data to new summary tables
description: You can migrate old sensor event data from the existing tables to the new summary data tables using the OnDemandDataMigration scheduled job. This job summarizes daily aggregated data based on specified criteria such as day-wise, location hierarchy-wise, and business entity-wise for occupancy, environment, badging, and Wi-Fi data. The summarized data is stored in the new Space Occupancy Daily Summary Data, Wi-Fi Daily Summary Data, Environmental Daily Summary Data, and Environmental Hourly Summary Data tables.
locale: en-US
release: xanadu
product: Workplace Connectors
classification: workplace-connectors
topic_type: task
last_updated: "2025-03-06"
reading_time_minutes: 1
breadcrumb: [Workplace Connectors Data Summarization, Workplace Connectors references, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Migrate event data to new summary tables

You can migrate old sensor event data from the existing tables to the new summary data tables using the OnDemandDataMigration scheduled job. This job summarizes daily aggregated data based on specified criteria such as day-wise, location hierarchy-wise, and business entity-wise for occupancy, environment, badging, and Wi-Fi data. The summarized data is stored in the new Space Occupancy Daily Summary Data, Wi-Fi Daily Summary Data, Environmental Daily Summary Data, and Environmental Hourly Summary Data tables.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the Application Search field, enter Workplace Connectors.

3.  From the filtered search results, select and open the OnDemandDataMigration scheduled job.

4.  Select **Execute Now**.


**Parent Topic:**[Workplace Connectors Data Summarization](../concept/data-summarization.md)

