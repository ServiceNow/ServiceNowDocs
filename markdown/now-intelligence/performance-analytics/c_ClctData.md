---
title: Collecting indicator scores
description: Performance Analytics uses data collection jobs to collect and clean scores and snapshots. You can also set indicator scores manually.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configure Performance Analytics advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Collecting indicator scores

Performance Analytics uses data collection jobs to collect and clean scores and snapshots. You can also set indicator scores manually.

To collect data immediately for existing records, run a historical data collection job.

For ongoing data collection, choose one of the following methods to collect indicator scores and snapshots based on the frequency and integrity of your data.

-   If you need to measure an indicator once a month, quarter, or year, enter scores manually or import scores.
-   If you need to measure indicators more frequently, or you want to eliminate any human involvement, use a scheduled data collection job.

**Note:** Performance Analytics snapshots are the lists of records \(sys\_ids\) that are collected at the time that the scores for those records are collected. A snapshot is made only for automated indicators with **Collect records** selected.

Performance Analytics data collection jobs do not collect scores older than specified in the property **com.snc.pa.dc.keep\_snapshots\_for**. Scores or snapshots older than this value are not collected during data collection.

-   **[Collect historical data](../task/t_RunHistoricalDataCollection.md)**  
Run a historical data collection job to collect scores and snapshots for existing records. When collecting data for the first time, such as for a new indicator, run historical data collection once to generate scores and snapshots for existing records.
-   **[Create or schedule a data collection job](../task/t_CreatASchedDataCollJob.md)**  
Schedule a data collection job to regularly collect Performance Analytics indicator scores and snapshots.
-   **[Configure a job indicator](../task/configure-job-indicator.md)**  
Increase the efficiency of data collection by configuring job indicators to collect only necessary and sensible data.
-   **[Cancel a data collection job](../task/cancel-pa-dc-job.md)**  
Cancel an active data collection job to stop the job from collecting scores.
-   **[Add or edit indicator scores manually](../task/t_ManuallyAddingScoresForIndicators.md)**  
You can manually enter score data for automated and manual indicators. Exercise care when editing scores for automated indicators.

**Parent Topic:**[Configure Performance Analytics advanced features](c_PADataArchitecture.md)

