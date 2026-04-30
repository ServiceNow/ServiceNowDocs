---
title: Teams components in Workforce Optimization for ITSM
description: Workforce Optimization for ITSM uses roles to administer teams and properties to modify default behavior.
locale: en-US
release: zurich
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Teams, Workforce Optimization for ITSM, IT Service Management]
---

# Teams components in Workforce Optimization for ITSM

Workforce Optimization for ITSM uses roles to administer teams and properties to modify default behavior.

## Roles

<table id="table_lcw_kwc_llb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Teams User \[sn\_team\_perf.team\_performance\_user\]

</td><td>

Grants access to read KPI tables.

</td></tr><tr><td>

Teams Admin \[sn\_team\_perf.team\_performance\_admin\]

</td><td>

Grants access to create and configure KPIs, KPI groups, and assignment groups in the Teams module.

</td></tr><tr><td>

Teams Manager \[sn\_team\_perf.team\_performance\_manager\]

</td><td>

Grants access to Team Performance module in Manager Workspace.

</td></tr></tbody>
</table>## Properties

<table id="table_ojw_fby_llb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_team\_perf.kpi\_group.max\_parent\_kpis

</td><td>

The maximum number of parent indicators that you can add to one KPI group.-   **Type:**Integer
-   **Default value:**5

</td></tr><tr><td>

sn\_team\_perf.kpi\_group.max\_supporting\_kpis

</td><td>

The maximum number of supporting KPIs you can define for a parent KPI.-   **Type:**Integer
-   **Default value:**10

</td></tr><tr><td>

sn\_team\_perf.ws.max\_assignment\_groups

</td><td>

The maximum number of assignment groups prioritized by order number to display on the Teams application in Manager Workspace.-   **Type:**Integer
-   **Default value:**15

</td></tr><tr><td>

sn\_optimize.default\_date\_range

</td><td>

The default date range set in the date range picker.-   **Type:**Integer
-   **Default value:**30

</td></tr></tbody>
</table>## Indicators

|Indicator Name|Description|
|--------------|-----------|
|Closed Incidents|Number of incidents closed.|
|Customer Satisfaction|Average customer satisfaction for incidents based on CSAT survey results. This indicator is associated with agent and assignment group breakdowns. It provides the customer satisfaction survey results for each agent and the agent's team.|
|Quality|Provides calculated assessment feedback score.|
|Average Handling Time \(MTTR\)|Mean time taken to resolve an incident.|
|First Call Resolution|Percentage of incidents resolved on first call.|
|Trainee Quality Rating|Average score, in percentage, of all surveys taken by the coach to assess the trainee.|
|Incidents triaged by VA|The number of incidents automatically created by the Virtual Agent for your team when tasks are deflected. You must have ITSM Virtual Agent Conversations \(com.snc.itsm.virtualagent\) installed on your system to analyze this KPI.|

