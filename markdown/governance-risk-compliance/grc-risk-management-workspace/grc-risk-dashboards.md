---
title: GRC Risk Overview dashboard
description: The Risk Overview dashboard provides an executive view into the status and workflows of inherent and residual enterprise and IT risks. The user can drill down into risks by framework, response, and exception.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# GRC Risk Overview dashboard

The Risk Overview dashboard provides an executive view into the status and workflows of inherent and residual enterprise and IT risks. The user can drill down into risks by framework, response, and exception.

There are two versions of this dashboard. The Premium version utilizes interactive filters and requires the licensed version of Performance Analytics.

The Risk Overview dashboard has two views, one with inherent risk reports and one with residual risk reports. The Premium version of the dashboard, which uses interactive filters, is shown. The other version of the dashboard has a third tab with static filtered reports instead of the interactive filters.![Upper area of the Inherent Risk Reports tab of the Risk Overview dashboard](../../../product/grc-risk/image/risk-overview-dashbrd.png)

**Important:** Starting with version 18.1.0 of the Risk Management and Advanced Risk applications, the Risk Overview PA Premium dashboard is available in the Next Experience UI Framework and renamed as Risk Overview dashboard.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

To open the dashboard, navigate to **All** &gt; **Risk** &gt; **Analytics Overview**.

![Risk Overview dashboard in the Next Experience](../image/risk-overview-dashboard-nextgen.gif "Risk Overview dashboard in the Next Experience")

## End users

|End user and goal|Required role|
|-----------------|-------------|
|Audit Manager: Needs clear visibility into the overall state and volume of vulnerabilities within the organization.|sn\_risk.manager|
|Audit Administrator: Needs to pinpoint areas of concern quickly|sn\_risk.admin|
|Audit Analyst: Needs to quickly prioritize which risks/tasks to focus on based upon criticality to the organization.|sn\_risk.user|

## Data visualizations

The Risk Overview dashboard contains the following visualizations:

|Name|Type|Description|
|----|----|-----------|
|High Inherent Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of risks with High Inherent Risk status|
|High Residual Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of risks with High Residual Risk status|
|Inherent Annual Loss Exposures|Box ![Box icon](../../performance-analytics/image/box.png)|Calculation of the inherent Annualized Loss Expectancy \(ALE\)|
|Inherent Risk|Bubble ![Bubble icon](../../performance-analytics/image/bubble-icon.png)|Calculation of the inherent risk score from the likelihood and significance of a risk.|
|Inherent Risk Heatmap|Heatmap ![Heatmap icon](../../performance-analytics/image/heatmap.png)|Inherent risk heatmap providing total number of risks by very high risk, high risk, moderate risk, low risk and very low risk|
|Low Inherent Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of low inherent risks.|
|Low Residual Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of low residual risks.|
|Moderate Inherent Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of moderate inherent risks.|
|Moderate Residual Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of moderate residual risks.|
|Residual Annual Loss Exposures|Box ![Box icon](../../performance-analytics/image/box.png)|Calculation of the residual Annualized Loss Expectancy \(ALE\)|
|Residual Risk|Bubble![Bubble icon](../../performance-analytics/image/bubble-icon.png)|Calculation of the residual risk score from the likelihood and significance of a risk.|
|Residual Risk Heatmap|Heatmap![Heatmap icon](../../performance-analytics/image/heatmap.png)|Total number of residual risks by very high risk, high risk, moderate risk, low risk, very low risk|
|Risk by Entity|Bar![Bar icon](../../performance-analytics/image/column-icon.png)|Number of total active risks broken down by profile.|
|Risk Exceptions|List![List icon3](../../performance-analytics/image/scorecard-icon.png)|Listing of all risk exceptions|
|Risk Issues by Framework \(Opened Date\)|Line![Line icon](../../performance-analytics/image/line-icon.png)|Total number of open risks over time broken down by framework|
|Risks by Category|Horizontal bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Total number of open risks broken down by category|
|Risks by Response|Horizontal bar ![Horizontal bar icon](../../performance-analytics/image/horizontal-bar.png)|Total number of open risks broken down by response|
|Very High Inherent Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of very high inherent risks.|
|Very High Residual Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of very high residual risks.|
|Very Low Inherent Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number \(count\) of very low inherent risks.|
|Very Low Residual Risk|Single Score ![Single-score icon](../../performance-analytics/image/single-score.png)|Displays the number of very low residual risks.|

**Parent Topic:**[Analytics and reporting solutions for Risk Management](grc-risk-mgmt-content-pack.md)

