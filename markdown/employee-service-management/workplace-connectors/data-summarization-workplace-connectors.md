---
title: Data summarization
description: Execute the DataSummarization scheduled job to retrieve the daily aggregate summary data. When the scheduled job runs, it collects the data from the target table and MetricBase and stores the daily aggregate data into the respective summary table.
locale: en-US
release: zurich
product: Workplace Connectors
classification: workplace-connectors
topic_type: concept
last_updated: "2025-09-02"
reading_time_minutes: 2
breadcrumb: [Reference, Workplace Connectors, Workplace Service Delivery, Employee Service Management]
---

# Data summarization

Execute the **DataSummarization** scheduled job to retrieve the daily aggregate summary data. When the scheduled job runs, it collects the data from the target table and MetricBase and stores the daily aggregate data into the respective summary table.

The MetricBase application stores time series data, which is data that is sampled at regular intervals. The administrator specifies a metric to store and how often to collect it by creating a time-series definition in MetricBase. The time-series data is sent from instance to the MetricBase server using the MetricBase API**.**For more information about MetricBase, see [Defining and collecting MetricBase data](https://www.servicenow.com/docs/access?context=collecting-metricbase-data&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

Workplace Connectors supports retrieving the time series data from the MetricBase and populates the data into the following summary tables:

Navigate to **All** &gt; **Workplace Connectors** &gt; **Summary** to view the summary tables.

|Table Name|Description|
|----------|-----------|
|Space Occupancy Daily Summary Data|The Space Occupancy Daily Summary Data \(sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data\) table displays aggregate data retrieved from the Occupancy and Environment Data target table and MetricBase. The **DataSummarization** scheduled job runs daily and loads the daily aggregate summary data into the table. It collects the metric data \(Space Occupancy Value\) from the target table \(Occupancy and Environment data\) and MetricBase and populates the data in the summary table \(Space Occupancy Daily Summary Data\).|
|Wi-Fi Daily Summary Data|In the Wi-Fi Daily Summary Data table \(sn\_wsd\_wc\_wifi\_daily\_summary\_data\), you can view aggregate data from Wi-Fi providers to determine employee attendance in the office. The **DataSummarization** scheduled job runs daily and retrieves the summary data based on the Wi-Fi time-series data stored in the Wi-Fi Data target table and MetricBase database.|
|Environmental Daily Summary Data|The Environmental Daily Summary Data table \(sn\_wsd\_wc\_environmental\_daily\_summary\_data\) displays daily aggregate environment data, including air quality and temperature for a workplace. The **DataSummarization** scheduled job runs daily and loads the daily aggregate summary data into the Environmental Daily Summary Data table. It collects metric data from the target table \(Occupancy and Environment data\) and MetricBase and populates the summary table data.|
|Environmental Hourly Summary Data|The Environmental Daily Summary Data table \(sn\_wsd\_wc\_environmental\_hourly\_summary\_data\) displays hourly aggregate environment data, including air quality and temperature data for a workplace. The **DataSummarization** scheduled job runs daily and loads the hourly aggregate summary data into the Environmental Hourly Summary Data table. It collects metric data from the target table \(Occupancy and Environment data\) and MetricBase and populates the summary table data.|

-   **[Archive and purge summary data tables](../task/archive-and-purge-summary-data-tables.md)**  
Use the archive rules and destroy rules to archive and purge the summary data. Archive and purge the Space Occupancy Daily Summary Data \(sn\_wsd\_wc\_space\_occupancy\_daily\_summary\_data\), Environmental Daily Summary Data \(sn\_wsd\_wc\_environmental\_daily\_summary\_data\), Environmental Hourly Summary Data \(sn\_wsd\_wc\_environmental\_hourly\_summary\_data\), and Wi-Fi Daily Summary Data \(sn\_wsd\_wc\_wifi\_daily\_summary\_data\) table records.
-   **[Run the DataSummarization on-demand job](../task/run-datasummarization-on-demand-job.md)**  
Use the on-demand OnDemandDataSummarization scheduled job to retrieve summary data for the required connector type if the DataSummarization scheduled job fails to populate the occupancy, environmental, or Wi-Fi summary reports.
-   **[Migrate event data to new summary tables](../task/migrate-event-data-to-new-summary-tables.md)**  
Migrate old sensor event data from the existing tables to the new summary data tables using the OnDemandDataMigration scheduled job.

**Parent Topic:**[Workplace Connectors references](../concept/workplace-connectors-references.md)

**Previous topic:**[Environmental data form for Workplace Connectors](wsd-environmental-data-form-fields.md)

**Next topic:**[Archive and purge summary data tables](../task/archive-and-purge-summary-data-tables.md)

