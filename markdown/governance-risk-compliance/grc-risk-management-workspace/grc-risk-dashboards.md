---
title: GRC Risk Overview dashboard
description: The Risk Overview dashboard provides an executive view into the status and workflows of inherent and residual enterprise and IT risks. The user can drill down into risks by framework, response, and exception.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/governance-risk-compliance/grc-risk-management-workspace/grc-risk-dashboards.html
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting solutions for Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# GRC Risk Overview dashboard

The Risk Overview dashboard provides an executive view into the status and workflows of inherent and residual enterprise and IT risks. The user can drill down into risks by framework, response, and exception.

There are two versions of this dashboard. The Premium version utilizes interactive filters and requires the licensed version of Performance Analytics.

The Risk Overview dashboard has two views, one with inherent risk reports and one with residual risk reports. The Premium version of the dashboard, which uses interactive filters, is shown. The other version of the dashboard has a third tab with static filtered reports instead of the interactive filters.\[Omitted image "risk-overview-dashbrd.png"\] Alt text: Upper area of the Inherent Risk Reports tab of the Risk Overview dashboard

**Important:** Starting with version 18.1.0 of the Risk Management and Advanced Risk applications, the Risk Overview PA Premium dashboard is available in the Next Experience UI Framework and renamed as Risk Overview dashboard.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

To open the dashboard, navigate to **All** &gt; **Risk** &gt; **Analytics Overview**.

\[Omitted image "risk-overview-dashboard-nextgen.gif"\] Alt text: Risk Overview dashboard in the Next Experience

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
|High Inherent Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of risks with High Inherent Risk status|
|High Residual Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Number of risks with High Residual Risk status|
|Inherent Annual Loss Exposures|Box \[Omitted image "box.png"\] Alt text: Box icon|Calculation of the inherent Annualized Loss Expectancy \(ALE\)|
|Inherent Risk|Bubble \[Omitted image "bubble-icon.png"\] Alt text: Bubble icon|Calculation of the inherent risk score from the likelihood and significance of a risk.|
|Inherent Risk Heatmap|Heatmap \[Omitted image "heatmap.png"\] Alt text: Heatmap icon|Inherent risk heatmap providing total number of risks by very high risk, high risk, moderate risk, low risk and very low risk|
|Low Inherent Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of low inherent risks.|
|Low Residual Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of low residual risks.|
|Moderate Inherent Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of moderate inherent risks.|
|Moderate Residual Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of moderate residual risks.|
|Residual Annual Loss Exposures|Box \[Omitted image "box.png"\] Alt text: Box icon|Calculation of the residual Annualized Loss Expectancy \(ALE\)|
|Residual Risk|Bubble\[Omitted image "bubble-icon.png"\] Alt text: Bubble icon|Calculation of the residual risk score from the likelihood and significance of a risk.|
|Residual Risk Heatmap|Heatmap\[Omitted image "heatmap.png"\] Alt text: Heatmap icon|Total number of residual risks by very high risk, high risk, moderate risk, low risk, very low risk|
|Risk by Entity|Bar\[Omitted image "column-icon.png"\] Alt text: Bar icon|Number of total active risks broken down by profile.|
|Risk Exceptions|List\[Omitted image "scorecard-icon.png"\] Alt text: List icon3|Listing of all risk exceptions|
|Risk Issues by Framework \(Opened Date\)|Line\[Omitted image "line-icon.png"\] Alt text: Line icon|Total number of open risks over time broken down by framework|
|Risks by Category|Horizontal bar \[Omitted image "horizontal-bar.png"\] Alt text: Horizontal bar icon|Total number of open risks broken down by category|
|Risks by Response|Horizontal bar \[Omitted image "horizontal-bar.png"\] Alt text: Horizontal bar icon|Total number of open risks broken down by response|
|Very High Inherent Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of very high inherent risks.|
|Very High Residual Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of very high residual risks.|
|Very Low Inherent Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number \(count\) of very low inherent risks.|
|Very Low Residual Risk|Single Score \[Omitted image "single-score.png"\] Alt text: Single-score icon|Displays the number of very low residual risks.|

**Parent Topic:**[Analytics and reporting solutions for Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/governance-risk-compliance/grc-risk-management-workspace/grc-risk-mgmt-content-pack.md)

