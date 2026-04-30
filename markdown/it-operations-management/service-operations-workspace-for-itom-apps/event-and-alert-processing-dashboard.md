---
title: Event and Alert dashboard
description: The Event and Alert dashboard uses Performance Analytics to provide real-time visibility into events and alerts in Event Management, showcasing key trends, outcomes, and the most impacted configuration items. It highlights metrics such as noise reduction, alert grouping coverage, and top alert sources.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [AIOps Dashboards in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Event and Alert dashboard

The Event and Alert dashboard uses Performance Analytics to provide real-time visibility into events and alerts in Event Management, showcasing key trends, outcomes, and the most impacted configuration items. It highlights metrics such as noise reduction, alert grouping coverage, and top alert sources.

![Events and Alerts dashboard.](../image/aiops-events-and-alerts-dashboard.png)

Run the \[PA EM\] Historic Data Collection job once to enable the partial collection of historical Event Management data:

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Data Collector** &gt; **Jobs**.
2.  Select \[PA EM\] Historic Data Collection.
3.  Select **Execute Now**.

## Prerequisites

Ensure that the Event Management application is installed.

## Required ServiceNow AI Platform roles

-   evt\_mgmt\_admin
-   evt\_mgmt\_operator

## Access the Events and alerts dashboard

To open the dashboard, use one of the following methods:

-   Navigate to **All** &gt; **AIOps Dashboards** &gt; **AIOps Operational** &gt; **Events and Alerts**.
-   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the AIOps Dashboards icon \(![AIOps Dashboards icon.](../../health-log-analytics-admin/image/aiops-operational-icon.png)\).

    By default, the **Events and Alerts** tab is selected.


## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|evt\_mgmt\_admin or admin|Edit the dashboard and grant view and share permissions.|
|evt\_mgmt\_operator or admin|View the dashboard and details of the records contained in it to visualize and track events, alerts, trends, outcomes, and the most impacted Configuration Items in your organization.|

## Breakdowns

Breakdowns available in the Event and Alert dashboard are:

-   Trends
-   Outcomes

## Reports

<table id="table_yyl_b4z_xxb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Noise reduction \(events to alerts compression\)

</td><td>

Line graph

</td><td>

The compression rate from events to alert creation. The higher the number, the fewer alerts are being created.

</td></tr><tr><td>

Alerts grouping coverage

</td><td>

Line graph

</td><td>

The percentage of alerts aggregated into grouped alerts over time.

</td></tr><tr><td>

Incident compression rate

</td><td>

Line graph

</td><td>

The percentage of alerts that did not result in incident creation. A higher percentage means more alerts were resolved without generating incidents.

</td></tr><tr><td>

Top 20 alert sources \(last 7 days\)

</td><td>

Bar chart

</td><td>

The number of alerts per source categorized by severity over the last 7 days.

</td></tr><tr><td>

Top 20 event sources \(last 5 days\)

</td><td>

Bar chart

</td><td>

The number of events per source categorized by severity over the last 5 days.

</td></tr><tr><td>

Alerts without CI \(created on last 7 days\)

</td><td>

Line graph

</td><td>

The number of alerts without CI binding created over the last 7 days.

</td></tr><tr><td>

Alerts grouping \(last 7 days\)

</td><td>

Bar chart

</td><td>

The distribution of grouped alerts over the last 7 days.

</td></tr></tbody>
</table>## Most impacted Configuration Items

The Most Impacted Configuration Items section of the Event and Alert dashboard provides a comprehensive overview of the configuration items \(CIs\) that are most impacted by the issue. This section lists key details such as the name of each CI, the number of associated alerts, their classification \(such as application service\), and location. Additionally, it identifies the owner and support group responsible for each CI, facilitating targeted and efficient incident resolution. By highlighting the most impacted CIs, this section helps prioritize critical assets and resources, ensuring that the most significant issues are addressed promptly to maintain system stability and performance.

