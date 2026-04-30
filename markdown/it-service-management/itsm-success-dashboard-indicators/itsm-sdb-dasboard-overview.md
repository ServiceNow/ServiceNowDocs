---
title: ITSM Success Dashboard indicators components
description: Analyze the performance and self-solve data visually and drive business outcomes with the help of the dashboard components.
locale: en-US
release: yokohama
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Exploring ITSM Success Dashboard indicators, ITSM Success Dashboard indicators, IT Service Management]
---

# ITSM Success Dashboard indicators components

Analyze the performance and self-solve data visually and drive business outcomes with the help of the dashboard components.

## Now Assist for ITSM Success Dashboard

With the Now Assist for Success Dashboard, you can summarize the chat conversations and incident details, generate the incident resolution notes to share with other agents, and wrap up incidents faster.

The **Self-solved using QnA** KPI in the ITSM Success Dashboard uses Now Assist and AI search QnA as contributing indicators. You can interact with a Virtual Agent, read the Knowledge base article, get a summarized/succinct response by Now LLM in Virtual Agent or on the portal. This interaction, subsequently does not create an incident, access any knowledge base article, or interact with a live agent in the next 24 hours.

To update the live agent script include see, [Update the live agent script include](../task/update-live-agent-script-include.md).

## Proactive Engagement for DEX

The **Self-solved using Proactive Engagement for DEX** KPI listed under the self-solved percentage, helps the users resolve their digital experience issues. It proactively suggests the resolutions and resolves the issue.

## Getting started with the Admin Console

With the Admin Console, you can access the ITSM Success Dashboard, Operational Success, and Benchmarks dashboard. The Admin Console displays all the admin-related work at a glance and tasks that need attention, including installation of the related application and configuration settings.

As an admin, you see the role-specific variant of the landing page. Admin landing pages include the following items:

-   Related applications that have a latest update available.
-   Related applications that aren't activated or installed.
-   Configurations for all the installed applications.
-   Common questions and more information related to the applications.

## Performance overview in the ITSM Success Dashboard indicators

Measure the key performance indicators \(KPIs\) like Self-solved percentage, Call deflection percentage, Requests completed, and Successful predictions on the **Performance overview** tab. For more information, see [ITSM Success Dashboard KPI definitions and formulas](sd-kpi-formulae.md).

![Success Dashboard showing the Performance overview tab.](../image/itsm-sd-landing-page-nov23.png)

## Service quality in the ITSM Success Dashboard indicators

Measure the key performance indicators \(KPIs\) like Customer satisfaction score, Mean time to resolve, % Breached SLA, and % First assignment resolution on the **Service quality** tab. For more information, see [ITSM Success Dashboard KPI definitions and formulas](sd-kpi-formulae.md).

![Success Dashboard showing the Service quality tab.](../image/service-quality-nov23.png)

## Cost savings in the ITSM Success Dashboard indicators

View the overall estimated cost saved by using the ITSM Success Dashboard capabilities for Knowledge articles, Predictive Intelligence, Virtual Agent conversations, and Catalog submissions.

![Cost savings displayed on the Performance overview tab.](../image/cost-savings-nov23.png)

## Scorecards in the ITSM Success Dashboard indicators

View the aggregation of the daily values for KPIs in the selected period in the scorecards with the following information.

![Scorecards for Self solved percentage.](../image/sdb-widgets.png "Scorecard widget")

-   **Current period score**: View the aggregated score for the current time period. Select one of the following options:
    -   **Monthly:** View the data aggregated monthly. For counts, this data is the monthly sum of the daily values. For percentages, this data is the monthly average of the daily percentages.
    -   **Quarterly:** View the data aggregated quarterly. For counts, this data is the quarterly sum of the daily values. For percentages, this data is the quarterly average of the daily percentages.
    -   **Yearly:** View the data aggregated yearly. For counts, this data is the yearly sum of the daily values. For percentages, this data is the yearly average of the daily percentages.
-   **Comparison with previous period**: View the percentage change compared to the previous period aggregation. Data is displayed in a month-over-month, quarter-over-quarter, and year-over-year comparison based on the availability of the data.

## Info icons in the ITSM Success Dashboard indicators

Use the info icons to view the short description of the indicator and understand how the indicator value is calculated.

![Details of info icon](../image/sdb-widget-info.png "Info icon")

## Trends in the ITSM Success Dashboard indicators

View the trend of the aggregated scores for the selected metric scorecard.

![Call deflection percentage trend example.](../image/sdb-trend-1.png "Call deflection trend")

![structured tickets completed trend.](../image/sdb-structured-trend.png "Structured tickets completed trend")

## View details in the ITSM Success Dashboard indicators

See the constituent drill-down views and their contextual descriptions for KPIs. The detailed information can be viewed by selecting **View details**.

-   View the primary indicators.

    ![Information on view details breakdown.](../image/sdb-view-details.png "Top-level primary indicators")

    You can replace or add new indicators to suit your implementation in addition to the base system indicators. See [Configure Success Dashboard indicators KPIs](../task/config-kpis-sdb.md) for more details.

-   View the contributing indicators.

    ![Second-level contributing indicators.](../image/second-level-kpis-sdb.png "Second-level contributing indicators")

    You can view a graph of the contributing indicators scores over time along with the KPI value.

-   View the record-level breakdown.

    ![Record-level information on view details breakdown.](../image/view-record-level-sdb.png "Record-level breakdown indicators")


This level of drill down helps you view the record-level details of the indicator when you have the `sn_sd.success_dashboard_details_read` user permissions. See [KPI details](https://www.servicenow.com/docs/access?context=kpi-details&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

## View cost saving details in the ITSM Success Dashboard indicators

Enable Cost savings and view the drill-down views and their contextual descriptions for KPIs. The detailed information can be viewed by selecting **View Details**.

-   View the primary indicators:![First-level cost savings indicators.](../image/cost-savings-first-level.png)
-   Second-level contributing indicators ![Contributing indicators impacting cost savings.](../image/second-level-cost-savings.png)

## Contextual side panel in the ITSM Success Dashboard indicators

View the contextual formula and definitions, insights, and cost savings in the **More information**, **Insights**, and **Cost Savings** side panel respectively for the selected metric or KPI.

More Information side panel.

![Side panel with more information.](../image/more-info.png)

## Insights side panel

View the insights of the KPIs.

![Insights side panel displaying the Self solved percentage.](../image/more-info-insights.png)

## Cost Savings side panel

View the amount saved for the KPI.

![Cost Savings panel displaying the KPI details.](../image/more-info-cost-savings.png)

## View process insights on the ITSM Success Dashboard

View the process insights on the ITSM Success Dashboard to analyze the process bottlenecks and take steps from the analyst workbench to improve the metrics.

On the **Service Quality** tab, select **Insights** on the contextual side panel, then select **View in Analyst Workbench**.

Only the top two insights that are the least efficient are displayed in the contextual side panel. The process insights are executed in the incident table only in the base system.

## Operational Success dashboard in the ITSM Success Dashboard indicators

The Operational Success dashboard provides a consolidated view of the end-to-end performance of the IT processes that are implemented in your organization.

The dashboard showcases a snapshot of the performances for the Incident, Major Incident, Change, Request, Service Catalog, Interaction, Problem, and On-Call Scheduling applications. These indicators help teams and the leadership focus on areas that have an impact on business outcomes.

![Operational Success dashboard showing the Service Catalog tab.](../image/operational-success.png)

**Parent Topic:**[Exploring ITSM Success Dashboard indicators](explore-success-dashboard-indicators.md)

