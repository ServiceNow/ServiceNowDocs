---
title: Demand Insights for Incidents dashboard
description: The Demand Insights for Incidents dashboard enables you as an incident manager to identify which incidents have no or insufficient knowledge coverage. You can then create feedback tasks for knowledge gaps to deflect such incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/knowledge-management/demand-insights-incidents-dashboard.html
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

The Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\) includes the Demand Insights for Incidents dashboard. For more information, see [Predictive Intelligence for Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/predictive-intelligence-for-km.md) and [Additional plugins for Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/additional-plugins-km.md).

\[Omitted image "demand-insights-incidents.png"\] Alt text: Demand Insights for Incidents dashboard

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

Pareto Chart \[Omitted image "pareto-sm.png"\] Alt text: Pareto report icon

</td><td>

Displays data from the Knowledge Curation Task \[kb\_curation\_task\_cluster\] table with the following conditions: Curation configuration = incident AND Solution.Active = true

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting Solutions for Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/analytics-and-reporting-solutions-for-knowlege-management.md)

**Related topics**  


[Pareto chart for Knowledge Demand Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/pareto-report-demand-insights.md)

[Knowledge demand insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/knowledge-demand-insights.md)

