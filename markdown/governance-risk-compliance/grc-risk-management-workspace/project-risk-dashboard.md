---
title: Project Risk Overview dashboard
description: The project risk dashboard is useful for project managers and the enterprise risk managers. Using this dashboard, the project managers and enterprise risk managers can view the risk performance and the overall risk posture. This dashboard helps risk managers to reduce the overall risks in an organization.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Project Risk Overview dashboard

The project risk dashboard is useful for project managers and the enterprise risk managers. Using this dashboard, the project managers and enterprise risk managers can view the risk performance and the overall risk posture. This dashboard helps risk managers to reduce the overall risks in an organization.

**Important:** Starting with version 18.1.0 of the Advanced Risk and Risk Management applications, the Project Risk Overview dashboard is deprecated. If you're on a legacy release or already using the dashboard, you can continue to use it.

![A comprehensive dashboard to view project and enterprise risks](../image/project-risk-dashboard.gif "Project Risk Overview dashboard")

## Required roles

-   To edit the dashboard, users must have it\_pps\_admin or sn\_risk.admin roles.
-   To view the dashboard, users must have sn\_risk.reader role or it\_project\_manager, or sn\_ppm.read roles.
-   To view the details of the records, users must have the sn\_grc.business\_user role.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|Enterprise risk manager|The enterprise risk manager can view the different enterprise risks and understand how many risks are critical, high, moderate, low, and very low. This dashboard provides an understanding of the overall enterprise risk posture.|
|Project manager|The project manager can select the project for which they want to view the risks. They can view the trend of the risks on a quarter-by-quarter basis, the number of risks assessed, the number of risks that affect the enterprise, and so on. The heatmap aggregates all the project risks that are assessed. It helps to keep a track of the bad risks and helps to manage them. This reduces the overall risk exposure for an organization.|

## Indicators

-   **PPM-Total Risks**

    Count of all risks with a parent project.

-   **PPM-Enterprise Risk Assessments**

    Count of all risk assessments with risk assessment methodology as Enterprise Assessment for Projects and the entity class as Project.

-   **PPM- Project Risk Enterprise**

    Count of all risk assessments with risk assessment methodology as Project Risk Assessment and with table as risk.

-   **PPM-Risks Assessed**

    Count of all risks with project risk assessment in the Monitor state.

-   **PPM-Risks with Enterprise Impact**

    Count of all risks with enterprise risk assessment in the Monitor state.


## Breakdowns

-   Project
-   Project and Enterprise Risk Assessment States
-   Qualitative Rating Criteria - Enterprise Inherent Assessment
-   Qualitative Rating Criteria - Enterprise Residual Assessment
-   Qualitative Rating Criteria - Project Inherent Assessment
-   Qualitative Rating Criteria - Project Residual Assessment

## Data visualizations

This dashboard displays the following visualizations:

|Title|Type|Description|
|-----|----|-----------|
|Total risks|Single score![Single score icon.](../../reporting/image/icon-single-score-report.png)|Total number of project risks identified.|
|Risks assessed|Single score![Single score icon.](../../reporting/image/icon-single-score-report.png)|Total number of project risks assessed.|
|Risks with enterprise impact|Single score![Single score icon.](../../reporting/image/icon-single-score-report.png)|Total number of risks with enterprise impact.|
|Enterprise impact- inherent risk|Bar graph![Bar graph icon.](../../reporting/image/icon-bar-report.png)|Number of inherent risks with enterprise impact.|
|Enterprise impact- residual risk|Bar graph![Bar graph icon.](../../reporting/image/icon-bar-report.png)|Number of residual risks with enterprise impact.|
|Enterprise risk assessments by state|Pie chart![Pie chart icon.](../../reporting/image/icon-pie-report.png)|Number of enterprise risk assessments by states.|
|Inherent risk|Bar graph![Bar graph icon.](../../reporting/image/icon-bar-report.png)|Number of inherent project risks.|
|Residual risk|Bar graph![Bar graph icon.](../../reporting/image/icon-bar-report.png)|Number of residual project risks.|
|Risk assessment by state|Pie chart![Pie chart icon.](../../reporting/image/icon-pie-report.png)|Number of project risk assessments by states.|
|Inherent risk by likelihood and impact|Heatmap ![Heatmap icon.](../../reporting/image/icon-heatmap-report.png)|Aggregation of all the inherent project risks and their impact.|
|Residual risk by likelihood and impact|Heatmap ![Heatmap icon.](../../reporting/image/icon-heatmap-report.png)|Aggregation of all the residual project risks and their impact.|

**Parent Topic:**[Analytics and reporting solutions for Risk Management](grc-risk-mgmt-content-pack.md)

