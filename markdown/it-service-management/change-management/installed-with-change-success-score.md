---
title: Components installed with Change Management - Change Success Score
description: Several types of components are installed with activation of the Change Management - Change Success Score \(com.snc.change\_management.change\_success\_score\) plugin, including tables and scheduled jobs.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activate Change Management - Change Success Score, Plugins, Configure, Change Management, IT Service Management]
---

# Components installed with Change Management - Change Success Score

Several types of components are installed with activation of the Change Management - Change Success Score \(com.snc.change\_management.change\_success\_score\) plugin, including tables and scheduled jobs.

## Scheduled jobs installed

|Scheduled job|Description|
|-------------|-----------|
|Change success score metrics \(Daily\)|Collects individual metrics for changes completed and incidents raised the previous day. This job runs on a daily basis at 02.00 UTC. When this job is completed, the Daily change success score script action is executed. This action triggers the calculation of the adjustment formula indicators, and store the new score in the metric table.|
|Change success score for today|Reads scores from metric table and calculates the daily averages for the past 30 days.|
|Change success score metrics \(Historical data\)|Gathers individual metrics daily for the past 30 days. This result overrides what is already stored in PA, that is not more than 30 days old. When this job is completed, the Historical change success scores script action is executed. The functionality of this script action is similar to that of the Daily change success score. Additionally, creating a new historic metric record for each day of the past 30 days.|
|Change success score \(Historical data\)|Reads scores from the metric table and calculates the daily average for the past 30 days≥|

**Note:**

Historical calculations are useful you decide to change the overall formula or multipliers for individual metrics later on. You can run Change success score metrics \(Historical data\) to recalculate metrics and score for the past 30 days creating a new history record.

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Change Success Score Rating \[chg\_success\_score\_rating\]

</td><td>

Defines the record that associates a rating choice and color with a Change Success Score range, such as, 0 to 499.

</td></tr></tbody>
</table>**Parent Topic:**[Activate Change Management - Change Success Score](../task/activate-change-success-score.md)

