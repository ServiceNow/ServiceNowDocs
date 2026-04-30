---
title: Legacy: Change Velocity dashboard
description: Use this dashboard to track the average duration of change requests in the last 30 days.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Legacy: Change Management Platform Analytics Solutions, Using Change Management, Change Management, IT Service Management]
---

# Legacy: Change Velocity dashboard

Use this dashboard to track the average duration of change requests in the last 30 days.

**Important:**

Starting in Xanadu release, the Change dashboard is deprecated. Users can use [Change dashboard](performance-analytics/change.md) to view, and track the open changes.

The Change Velocity dashboard is divided into the following tabs for effective usage. The ServiceNow® Performance Analytics capability in the Change Velocity dashboard provides the following benefits:

-   The **Current Pipeline** tab provides insights into current change activity. The **Historical Pipeline** tab provides details on trends and patterns associated with the change management process flow. The **Process KPIs** tab represents a modern set of Change KPIs that are used to evaluate the change process.

    ![Change Velocity dashboard view.](../image/change-velocity-dashboard.gif "Change Velocity dashboard view")

-   The **Process Optimization** tab provides change activity assessments that are based on the state model. This capability is available only with an ITSM Enterprise subscription. For more information, see [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    ![Process Optimization view.](../image/PO.gif "Process Optimization view")


## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Change manager - Monitors the success and velocity of change request in the organization at the organization, team, and individual level.|change\_manager|

**Note:** To access the **Process Optimization** tab, the change manager must be part of the Change Assignment group.

## Change Velocity dashboard indicators

-   **Change Velocity**

    Average amount of time that changes have been waiting for approval in the last 30 days. To generate this data on the dashboard, you must run the Change velocity historical data collection job. For information on how to run this job see, [Collect historical data](https://www.servicenow.com/docs/access?context=t_RunHistoricalDataCollection&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

-   **Top Change Success Performers**

    Performance of assignment groups in processing the change request with the highest performer on the top. For information on how the performance score is calculated, see [Success Score Calculation](../../../product/change-management/concept/change-score-calculation.md).

-   **Average age of open changes**

    Average amount of time that the change request has been open.

-   **Average close time of changes**

    Average amount of time that it has taken to close the change request.

-   **Average implementation time of closed changes**

    Average amount of time between the start and close date of the change request.


## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Awaiting Cab Approval|Single score \(![Single score icon.](../../performance-analytics/image/single-score.png)\)|Number of changes awaiting CAB approval.|
|High Risk Changes|Single score \(![Single score icon.](../../performance-analytics/image/single-score.png)\)|Number of high risk changes starting today.|
|Awaiting Approvals|Single score \(![Single score icon.](../../performance-analytics/image/single-score.png)\)|Number of changes awaiting approval.|
|Model Breakdown|Pie \(![Pie icon.](../../../reuse/reporting/image/pie-sm.svg)\)|Changes categorized based on the change model over the last 30 days.|
|Type Breakdown|Pie \(![Pie icon.](../../../reuse/reporting/image/pie-sm.svg)\)|Changes categorized based on the change type in the last 30 days.|
|Open Changes by Category|Pie \(![Pie icon.](../../../reuse/reporting/image/pie-sm.svg)\)|Number of open changes from each category.|
|Change Pipeline|Vertical bar \(![Bar report icon](../../reporting/image/icon-bar-report.png)\)|Number of changes categorized based on their state.|
|Change Success|Pie \(![Pie icon.](../../../reuse/reporting/image/pie-sm.svg)\)|Number of changes categorized based on their close code over the last 30 days.|
|Change Risk|Vertical bar \(![Bar report icon](../../reporting/image/icon-bar-report.png)\)|Number of changes categorized based on the risk values.|
|High Risk Change List|List \(![List report icon](../../reporting/image/icon-list-report.png)\) \(\)|List of high risk changes starting today.|
|Highest Change Activity|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Top 10 configuration items associated with changes in the last 3 months.|
|Change Success|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Changes that are successful, unsuccessful, and successful with issues expressed on a line chart.|
|Change Risk|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Changes categorized based on the severity of risk.|
|Change Volume|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Volume of changes in the last 6 months.|
|Unsuccessful Changes|List \(![List report icon](../../reporting/image/icon-list-report.png)\)|Number of unsuccessful changes in the last 7 days.|
|Emergency Changes|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Number of emergency changes over the last 90 days.|
|Change Related Incidents|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Number of closed incidents in last 90 days where they have related changes.|
|Unauthorized Changes|Line \(![Line icon.](../../performance-analytics/image/line-icon.png)\)|Number of unauthorized changes over the last 90 days.|
|Active Changes &gt; 7 days|Single score \(![Single score icon.](../../performance-analytics/image/single-score.png)\)|Number of active changes that were created more than seven days ago.|

**Parent Topic:**[Legacy: Change Management Platform Analytics Solutions](change-content-pack.md)

