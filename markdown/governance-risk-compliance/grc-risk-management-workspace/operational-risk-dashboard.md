---
title: Operational Risk Management dashboard
description: The Operational Risk Management dashboard enables an entity owner, with the role sn\_risk.user, to view the complete risk posture for the enterprise in a single consolidated report. This dashboard makes it easy to analyze the risk posture efficiently and take necessary corrective actions to ensure that there are no losses.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Operational Risk Management dashboard

The Operational Risk Management dashboard enables an entity owner, with the role sn\_risk.user, to view the complete risk posture for the enterprise in a single consolidated report. This dashboard makes it easy to analyze the risk posture efficiently and take necessary corrective actions to ensure that there are no losses.

![Tabs of the operational risk dashboard](../../../product/grc-risk/image/operational-risk-dashboard.png "Operational risk dashboard")

**Important:** Starting with version 18.1.0 of the Advanced Risk application, the Operational Risk Management dashboard is available in the Next Experience UI Framework.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

To open the dashboard, navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Analytics Operational Risk Dashboard**.

![Operational Risk Management dashboard in the Next Experience](../image/operational-risk-management-dashboard-nextgen.gif "Operational Risk Management dashboard in the Next Experience")

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Risk user: Operational risk captures business continuity plans, environmental risk, process systems, operations risk, and people-related risks.

</td><td>

sn\_risk.user

</td><td>

-   Improves the reliability of business operations.
-   Improves the effectiveness of risk management operations.
-   Strengthens the decision-making process.
-   Reduces losses caused by unidentified or poorly-identified risks.
-   Detects unlawful activities early.
-   Lowers compliance costs.
-   Reduces potential damage from future risks.

</td></tr></tbody>
</table>Operational risk is the risk of loss that is incurred from inadequate or inefficient internal processes, people, and systems, or from external events. Operational risk captures the following to provide the complete risk posture of an organization:

-   Risk identification and assessment
-   Risk events data
-   Identifying and assessing internal controls
-   Monitoring and reporting of risks

## Indicators

Indicators define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time. To view this dashboard, users must have Advanced Risk and Policy and Compliance Management plugins activated

To view the list of all indicators for all the associated plugins, see the following:

-   [GRC Advanced Risk plugin indicators](indicators-advanced-risk.md)
-   [GRC Policy and Compliance Management plugin indicators](indicators-policy-compliance.md)
-   [GRC Audit Management plugin indicators](indicators-audit-mgmt.md)
-   [GRC Risk Management plugin Performance Analytics indicators](indicators-risk-mgmt.md)
-   [GRC Profiles plugin indicators](indicators-grc-profiles.md)

**Note:** There are two jobs that you must run to collect data for this dashboard.

-   **Daily Data Collector job**: This job is used to collect data for the Indicators. This jobs runs daily. To run this job, you must fill the **Run as** field with an appropriate value. This job is preconfigured.
-   **Historical Data Collector job**: This job is used to collect data over a period of time. This job is generally preconfigured with the demo data. Therefore, if you enable demo data, while activating the plugin, then you can view this job. To run this job, you must fill the **Run as** field with an appropriate value.

## Breakdowns

Organization \(Entity\)

## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Risk Response by Residual Risk Rating|Heatmap ![Heatmap icon](../../reporting/image/icon-heatmap-report.png)|Heatmap which shows the number of different risk response tasks for each residual risks.|
|Controls by owner|Horizontal bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Controls distributed on the basis of their owners.|
|Risks by owner|Horizontal bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Risks distributed on the basis of their owners.|
|Inherent risks by category|Horizontal bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Number of risk assessments with different inherent risk levels grouped by risk statement categories such as credit, market and so on.|
|Residual risks by category|Horizontal bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Number of risk assessments with different residual risk levels grouped by risk statement categories such as credit, market, and so on.|
|Control Test|List ![Score card icon](../../performance-analytics/image/scorecard-icon.png)|List of all controls.|
|Control Indicators|List ![Score card icon](../../performance-analytics/image/scorecard-icon.png)|Indicators associated with each control.|
|Risk Indicators|List ![Score card icon](../../performance-analytics/image/scorecard-icon.png)|Indicators associated with each risk.|
|Controls by classifications|Pie chart ![Pie icon](../../performance-analytics/image/pie-icon.png)|Controls distribution on the basis of its classification like preventive or detective.|
|Controls by attestation frequency|Pie chart ![Pie icon](../../performance-analytics/image/pie-icon.png)|Controls distributed on the basis of attestation frequency.|
|Risks by category|Pie chart ![Pie icon](../../performance-analytics/image/pie-icon.png)|Risk distribution on the basis of category.|
|Overdue issues|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of open issues that are past their planned end date.|
|Active risk events|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of active risk events.|
|Pending attestations|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of controls awaiting attestation.|
|Overdue assessment task|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of risk assessments with the substate as Overdue.|
|Upcoming acceptance expiry|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of risk acceptance tasks with acceptance end date in next 10 days.|
|Open mitigation tasks|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of open mitigation tasks.|
|Open indicator tasks|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of open indicator tasks.|
|Overdue control tests|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of open control tests that are past their planned end date.|

-   **[GRC Advanced Risk plugin indicators](indicators-advanced-risk.md)**  
The GRC Advanced Risk plugin contains various indicators.
-   **[GRC Audit Management plugin indicators](indicators-audit-mgmt.md)**  
The GRC Audit Management plugin contains various indicators.
-   **[GRC Policy and Compliance Management plugin indicators](indicators-policy-compliance.md)**  
The GRC Policy and Compliance Management plugin contains various indicators.
-   **[GRC Risk Management plugin Performance Analytics indicators](indicators-risk-mgmt.md)**  
The GRC Risk Management plugin contains various Performance Analytics indicators.
-   **[GRC Profiles plugin indicators](indicators-grc-profiles.md)**  
The GRC Profiles plugin contains various indicators.
-   **[Risk register in the Risk Workspace](../../../product/grc-workspace-risk/concept/risk-register-workspace.md)**  
The risk register contains the information about identified risks, results of risk analysis such as risk scores, and risk response plans. The risk register enables you to monitor and control the risks of your organization.

**Parent Topic:**[Analytics and reporting solutions for Risk Management](grc-risk-mgmt-content-pack.md)

