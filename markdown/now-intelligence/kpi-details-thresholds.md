---
title: Indicator thresholds in KPI Details
description: Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.Add, modify, or delete personal thresholds. With the required roles, you can also add, modify, and delete thresholds for all users.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [KPI Details, Platform Analytics]
---

# Indicator thresholds in KPI Details

Thresholds define a normal range of scores for an indicator and alert you when certain events occurs, like when a score reaches an all-time high.

When a threshold is triggered, the instance generates an email notification. This message is associated with the indicator and the message is directly available via KPI Details.

A threshold can be personal or global. A personal threshold is visible only to the user that created it. It appears as a light grey dotted line. A global threshold is visible to all users and appears as a dark grey dotted line. Because you cannot share a personal threshold, it appears only in KPI Details and the Analytics Hub. Global thresholds can also appear in time series data visualizations. Dashboards can alert viewers to events related to thresholds through [proactive analytics insights cards](proactive-analytics.md).

**Parent Topic:**[KPI Details](kpi-details.md)

## Add, modify, or delete a threshold in KPI Details

Add, modify, or delete personal thresholds. With the required roles, you can also add, modify, and delete thresholds for all users.

### Before you begin

Role required: Any role for your own personal thresholds. The pa\_threshold\_admin role or a role containing it \(pa\_power\_user, pa\_admin, or admin\) for global thresholds and for personal thresholds created by other users.

### About this task

**Note:** Thresholds are not available when multiple breakdown elements are selected.

### Procedure

1.  Navigate to the workspace with the indicator you want to work with.

2.  Click the Analytics Center icon \(![](../image/analytics-center-icon.png)\) and navigate to the KPIs tab.

3.  Click the threshold icon \(![](../image/thresh-icon.png)\).

4.  Select either Global or Personal thresholds.

    You see all the existing Global or Personal thresholds on this indicator.

5.  Click the Create Threshold icon \(![](../image/add-target-thresh-icon.png)\) or select an existing target to edit it.

6.  Choose the visibility of the threshold, either **Global** or **Personal**.

7.  Select or change the **Threshold Type**:

    -   All time high
    -   All time low
    -   Less than

        Enter a threshold value to trigger a message if the value of the indicator drops below the threshold.

    -   More than

        Enter a threshold value to trigger a message if the value of the indicator exceeds the threshold.

8.  Click **Save** if you are creating a threshold or **Update** if you are modifying a threshold.


