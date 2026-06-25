---
title: Create, modify, or delete a threshold in KPI Details
description: Add, modify, or delete personal thresholds. With the required roles, you can also add, modify, and delete thresholds for all users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/add-mod-pers-tar-thresh-kpi-details.html
release: australia
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 2
breadcrumb: [Targets and thresholds, KPI Details, Platform Analytics experience, Platform Analytics]
---

# Create, modify, or delete a threshold in KPI Details

Add, modify, or delete personal thresholds. With the required roles, you can also add, modify, and delete thresholds for all users.

## Before you begin

Role required: Any role for your own personal thresholds. The pa\_threshold\_admin role or a role containing it \(pa\_power\_user, pa\_admin, or admin\) for global thresholds and for personal thresholds created by other users.

## About this task

**Note:** Thresholds are not available when multiple breakdown elements are selected.

## Procedure

1.  Navigate to the workspace with the indicator you want to work with.

2.  Click the Analytics Center icon \(\[Omitted image "analytics-center-icon.png"\] Alt text: Analytics center icon\) and navigate to the KPIs tab.

3.  Click the threshold icon \(\[Omitted image "thresh-icon.png"\] Alt text: Threshold icon\).

4.  Select either For everyone or For me.

5.  Click the Create Threshold icon \(\[Omitted image "add-target-thresh-icon.png"\] Alt text: Create threshold icon\) or select an existing target to edit it.

6.  Choose the visibility of the threshold, either **For everyone** or **For me**.

7.  Select or change the **Threshold Type**:

    -   All time high
    -   All time low
    -   Less than

        Enter a threshold value to trigger a message if the value of the indicator drops below the threshold.

    -   More than

        Enter a threshold value to trigger a message if the value of the indicator exceeds the threshold.

8.  For a native Data snapshots indicator, you can select **Users to notify** by email when the threshold is broached.

9.  Click **Save** if you are creating a threshold or **Update** if you are modifying a threshold.


**Parent Topic:**[Indicator targets and thresholds in KPI Details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/kpi-details-targets.md)

**Related topics**  


[Create a target in KPI Details]()

[Edit multiple targets in KPI Details]()

[Subscribe users to Data snapshots indicator target]()

[Add a target to multiple breakdown elements in KPI Details]()

[Responsibility for indicator targets]()

