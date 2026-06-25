---
title: Legacy: Change Velocity dashboard
description: Use this dashboard to track the average duration of change requests in the last 30 days.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/change-velocity-dashboard.html
release: australia
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Legacy: Change Management Platform Analytics Solutions, Use, Change Management, IT Service Management]
---

# Legacy: Change Velocity dashboard

Use this dashboard to track the average duration of change requests in the last 30 days.

**Important:**

Starting in Xanadu release, the Change dashboard is deprecated. Users can use [Change dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change.md) to view, and track the open changes.

The Change Velocity dashboard is divided into the following tabs for effective usage. The ServiceNow® Performance Analytics capability in the Change Velocity dashboard provides the following benefits:

-   The **Current Pipeline** tab provides insights into current change activity. The **Historical Pipeline** tab provides details on trends and patterns associated with the change management process flow. The **Process KPIs** tab represents a modern set of Change KPIs that are used to evaluate the change process.

    \[Omitted image "change-velocity-dashboard.gif"\] Alt text: Change Velocity dashboard view.

-   The **Process Optimization** tab provides change activity assessments that are based on the state model. This capability is available only with an ITSM Enterprise subscription. For more information, see [Process Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/process-mining.md).

    \[Omitted image "PO.gif"\] Alt text: Process Optimization view.


## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Change manager - Monitors the success and velocity of change request in the organization at the organization, team, and individual level.|change\_manager|

**Note:** To access the **Process Optimization** tab, the change manager must be part of the Change Assignment group.

## Change Velocity dashboard indicators

-   **Change Velocity**

    Average amount of time that changes have been waiting for approval in the last 30 days. To generate this data on the dashboard, you must run the Change velocity historical data collection job. For information on how to run this job see, [Collect historical data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/t_RunHistoricalDataCollection.md).

-   **Top Change Success Performers**

    Performance of assignment groups in processing the change request with the highest performer on the top. For information on how the performance score is calculated, see [Success Score Calculation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-score-calculation.md).

-   **Average age of open changes**

    Average amount of time that the change request has been open.

-   **Average close time of changes**

    Average amount of time that it has taken to close the change request.

-   **Average implementation time of closed changes**

    Average amount of time between the start and close date of the change request.


## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Awaiting Cab Approval|Single score \(\[Omitted image "single-score.png"\] Alt text: Single score icon.\)|Number of changes awaiting CAB approval.|
|High Risk Changes|Single score \(\[Omitted image "single-score.png"\] Alt text: Single score icon.\)|Number of high risk changes starting today.|
|Awaiting Approvals|Single score \(\[Omitted image "single-score.png"\] Alt text: Single score icon.\)|Number of changes awaiting approval.|
|Model Breakdown|Pie \(\[Omitted image "pie-sm.svg"\] Alt text: Pie icon.\)|Changes categorized based on the change model over the last 30 days.|
|Type Breakdown|Pie \(\[Omitted image "pie-sm.svg"\] Alt text: Pie icon.\)|Changes categorized based on the change type in the last 30 days.|
|Open Changes by Category|Pie \(\[Omitted image "pie-sm.svg"\] Alt text: Pie icon.\)|Number of open changes from each category.|
|Change Pipeline|Vertical bar \(\[Omitted image "icon-bar-report.png"\] Alt text: Bar report icon\)|Number of changes categorized based on their state.|
|Change Success|Pie \(\[Omitted image "pie-sm.svg"\] Alt text: Pie icon.\)|Number of changes categorized based on their close code over the last 30 days.|
|Change Risk|Vertical bar \(\[Omitted image "icon-bar-report.png"\] Alt text: Bar report icon\)|Number of changes categorized based on the risk values.|
|High Risk Change List|List \(\[Omitted image "icon-list-report.png"\] Alt text: List report icon\) \(\)|List of high risk changes starting today.|
|Highest Change Activity|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Top 10 configuration items associated with changes in the last 3 months.|
|Change Success|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Changes that are successful, unsuccessful, and successful with issues expressed on a line chart.|
|Change Risk|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Changes categorized based on the severity of risk.|
|Change Volume|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Volume of changes in the last 6 months.|
|Unsuccessful Changes|List \(\[Omitted image "icon-list-report.png"\] Alt text: List report icon\)|Number of unsuccessful changes in the last 7 days.|
|Emergency Changes|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Number of emergency changes over the last 90 days.|
|Change Related Incidents|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Number of closed incidents in last 90 days where they have related changes.|
|Unauthorized Changes|Line \(\[Omitted image "line-icon.png"\] Alt text: Line icon.\)|Number of unauthorized changes over the last 90 days.|
|Active Changes &gt; 7 days|Single score \(\[Omitted image "single-score.png"\] Alt text: Single score icon.\)|Number of active changes that were created more than seven days ago.|

**Parent Topic:**[Legacy: Change Management Platform Analytics Solutions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/change-content-pack.md)

