---
title: Demand Insights for Cases dashboard
description: The Demand Insights for Cases dashboard enables you as a customer service case manager to identify which cases have no or insufficient knowledge coverage. You can then create feedback tasks for knowledge gaps to deflect such cases.
locale: en-US
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Analytics and Reporting Solutions for Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Demand Insights for Cases dashboard

The Demand Insights for Cases dashboard enables you as a customer service case manager to identify which cases have no or insufficient knowledge coverage. You can then create feedback tasks for knowledge gaps to deflect such cases.

The Predictive Intelligence for Knowledge Management plugin \(com.snc.knowledge\_ml\) includes the Demand Insights for Cases dashboard. For more information, see [Predictive Intelligence for Knowledge Management](predictive-intelligence-for-km.md) and [Additional plugins for Knowledge Management](../reference/additional-plugins-km.md). The navigation path for viewing this dashboard is **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**. Using the search field, look for the dashboard.

![Demand Insights for Cases dashboard](../image/Demand-insights-cases-db.png)

## End user and roles

|End user and goal|Required roles|
|-----------------|--------------|
|Customer service case manager: Needs to identify which cases don't have good knowledge coverage.|sn\_km\_ml.knowledge\_curation\_user and sn\_customerservice\_manager|

## Reports

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Candidate Knowledge Gaps for Case

</td><td>

Pareto Chart ![Pareto report icon](../../../reuse/reporting/image/pareto-sm.png)

</td><td>

Displays data from the Knowledge Curation Task \[kb\_curation\_task\_cluster\] table with the following conditions: Curation configuration = sn\_customerservice\_case AND Solution.Active = true

</td></tr></tbody>
</table>**Parent Topic:**[Analytics and Reporting Solutions for Knowledge Management](analytics-and-reporting-solutions-for-knowlege-management.md)

**Related topics**  


[Pareto chart for Knowledge Demand Insights](pareto-report-demand-insights.md)

[Knowledge demand insights](knowledge-demand-insights.md)

