---
title: Demand Insights for Incidents dashboard
description: The Demand Insights for Incidents dashboard enables you as an incident manager to identify which incidents have no or insufficient knowledge coverage. You can then create feedback tasks for knowledge gaps to deflect such incidents.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Analytics and Reporting Solutions for Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Demand Insights for Incidents dashboard

The Demand Insights for Incidents dashboard enables you as an incident manager to identify which incidents have no or insufficient knowledge coverage. You can then create feedback tasks for knowledge gaps to deflect such incidents.

The Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\) includes the Demand Insights for Incidents dashboard. For more information, see [Predictive Intelligence for Knowledge Management](predictive-intelligence-for-km.md) and [Additional plugins for Knowledge Management](../reference/additional-plugins-km.md).

![Demand Insights for Incidents dashboard](../image/demand-insights-incidents.png "Demand Insights for Incidents dashboard")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Incident manager: Needs to identify which incidents don't have good knowledge coverage.|sn\_km\_ml.knowledge\_curation\_user and incident\_manager|

## Reports

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Candidate Knowledge Gaps for Incident

</td><td>

Pareto Chart ![Pareto report icon](../../../reuse/reporting/image/pareto-sm.png)

</td><td>

Displays data from the Knowledge Curation Task \[kb\_curation\_task\_cluster\] table with the following conditions: Curation configuration = incident AND Solution.Active = true

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting Solutions for Knowledge Management](analytics-and-reporting-solutions-for-knowlege-management.md)

**Related topics**  


[Pareto chart for Knowledge Demand Insights](pareto-report-demand-insights.md)

[Knowledge demand insights](knowledge-demand-insights.md)

