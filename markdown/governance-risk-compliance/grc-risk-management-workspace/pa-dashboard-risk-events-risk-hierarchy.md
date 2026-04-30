---
title: Performance Analytics dashboards for risk events and risk hierarchy
description: Use the Performance Analytics \(PA\) dashboards to view the comprehensive data for risk events and risk hierarchy. Use the Analytics Hub to view data for any time period.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Performance Analytics dashboards for risk events and risk hierarchy

Use the Performance Analytics \(PA\) dashboards to view the comprehensive data for risk events and risk hierarchy. Use the Analytics Hub to view data for any time period.

By default, users with the sn\_risk.manager role can view data for six months. To view the data for different time periods, purchase and activate the Performance Analytics Premium plugin. Users with the sn\_risk.manager role can collate historical data for one year by running the ServiceNow® Governance, Risk, and Compliance \(GRC\) **Entity and risk statement historical data collection** job.

**Note:** Run the historical data collection job only once. Running this job more than once leads to inconsistent data collection and might result in a loss of previous data.

## Risk Events dashboards

The Risk Events dashboards present the following data:

-   Risk Event Overview: This dashboard shows the following trends:

    -   Gross Loss
    -   Net Loss
    -   Events
    -   Active Events
    -   Near Miss
    -   Events by Type
    -   Events by State
    -   Top 10 Net Loss Entities
    -   Top 10 Non-Financial Impact Entities
    -   Top 10 Entities with Highest No. of Losses
    **Important:** Starting with version 18.1.0 of the Risk Management and Advanced Risk applications, the Risk Event Overview dashboard is available in the Next Experience UI Framework.

    If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

    To open the dashboard, navigate to **All** &gt; **Risk Events** &gt; **Analytics Overview**.

    ![Risk Event Overview dashboard in the Next Experience.](../../../use/dashboards/image/risk-event-overview-dashboard-nextgen.gif "Risk Event Overview dashboard in the Next Experience")

-   Risk Event Overview by Entity dashboard: Entity owners with the sn.risk\_user role can view the aggregated information for gross loss, net loss, and the number of events on a monthly basis. The dashboard also shows the average gross loss per event, average net loss per event, average recovery made per event, and average additional cost per event. Entity owners with the sn.risk\_user role can also view the following risk events trends for a particular entity. Administrators with the sn.risk\_admin role can edit this dashboard.

    -   Gross Loss
    -   Net Loss
    -   Events
    -   Active Events
    -   Near Miss
    -   Risk Events
    -   Risk Events by Non-Financial Impact
    -   Annual Loss Expectancy vs Net Loss
    -   Risk Event Metrics
    **Important:** Starting with version 18.1.0 of the Risk Management and Advanced Risk applications, the Risk Event Overview by Entity dashboard is available in the Next Experience UI Framework.

    If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

    To open the dashboard, navigate to **All** &gt; **Risk Events** &gt; **Analytics Overview by Entity**.

    ![Risk Event Overview by Entity dashboard in the Next Experience.](../../../use/dashboards/image/risk-event-overview-by-entity-nextgen.jpg "Risk Event Overview by Entity dashboard in the Next Experience")

-   Risk Event Overview by Risk Class dashboard: Users with the sn\_risk.manager role can view level 1 risk event trends. Users can understand the aggregated gross losses, net loss, number of events created, number of active events, and the total number of near-miss events. This dashboard also shows the following trends:
    -   Gross Loss
    -   Net Loss
    -   Events
    -   Active Events
    -   Near Miss
    -   Top 10 Net Loss Risk Events
    -   Annual Loss expectancy vs Net Loss

**Important:** Starting with version 18.1.0 of the Risk Management and Advanced Risk applications, the Risk Event Overview by Risk Class dashboard is available in the Next Experience UI Framework.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

To open the dashboard, navigate to **All** &gt; **Risk Events** &gt; **Analytics Overview by Risk Class**.

![Risk Event Overview by Risk Class dashboard in the Next Experience.](../../../use/dashboards/image/risk-event-overview-by-risk-class-nextgen.jpg "Risk Event Overview by Risk Class dashboard in the Next Experience")

## Exposure by Risk Statements dashboard

To view the Exposure by Risk Statements dashboard, navigate to **Risk** &gt; **Exposure by Risk Statements**. This dashboard is useful for users with the sn\_risk.manager role. This dashboard is similar to the Exposure by Entity dashboard, except that the dashboard also displays the risks by risk statement. This dashboard provides the distribution of entities based on tolerance status and calculated scores, as well as annual loss expectancy trends. A heatmap of the risk ratings by tolerance status is included. The Exposure by Risk Statements dashboard displays the following trends:

-   Risk Statements per Tolerance Status
-   Risk Statements per Rating
-   Annual Loss Expectancy
-   Risk Ratings by Tolerance Status

**Important:** Starting with version 18.1.0 of the Advanced Risk and Risk Management applications, the Exposure by Risk Statements dashboard is deprecated. If you're on a legacy release or already using the dashboard, you can continue to use it.

## Exposure by Entity dashboard

To view the Exposure by Risk Statements dashboard, navigate to **Risk** &gt; **Exposure by Entity**. This dashboard is useful for entity owners responsible for a particular entity class. The dashboard also shows the entity health by displaying the statuses: Unacceptable, needs attention, and acceptable. Use this dashboard to compare trends across quarters based on annual loss expectancy \(ALE\). This dashboard displays risk ratings by tolerance status in the form of a heatmap. The heatmap helps you identify the entities that need attention. Annual loss expectancy trends and a heatmap of the risk ratings by tolerance status are also shown. The Exposure by Risk Statements dashboard displays the following trends:

-   Entities per Tolerance Status
-   Entities per Rating
-   Entity Annual Loss Expectancy
-   Risk Ratings by Tolerance Status

**Important:** Starting with version 18.1.0 of the Advanced Risk and Risk Management applications, the Exposure by Entity dashboard is deprecated. If you're on a legacy release or already using the dashboard, you can continue to use it.

**Parent Topic:**[Analytics and reporting solutions for Risk Management](../../../use/dashboards/application-content-packs/grc-risk-mgmt-content-pack.md)

