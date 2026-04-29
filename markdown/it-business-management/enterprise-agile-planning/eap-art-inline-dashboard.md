---
title: EAP ART dashboard
description: The ART dashboard provides a snapshot of the overall progress of your Planning Interval \(PI\).
locale: en-US
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reports and dashboards, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# EAP ART dashboard

The ART dashboard provides a snapshot of the overall progress of your Planning Interval \(PI\).

![ART Inline dashboard](../images/eap-art-inline-dashboard.png)

You can use a default dashboard or you can configure a custom dashboard and associate it with your Agile configuration. For more information, see [Configuring custom dashboards in EAP](configuring-eap-dashboard.md).

## Required EAP roles

The EAP read-only \(sn\_apw\_advanced.eap\_read\_only\) role is required to view the dashboard.

## Access the ART dashboard

1.  Navigate to **Workspaces** &gt; **Strategic Planning Workspace** &gt; **Enterprise Agile Planning**.
2.  From the Agile structure section of the navigation panel, choose your EAP ART.
3.  Select the **Home** tab.

## Use cases

<table id="table_wxy_x1r_gbc"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

-   Portfolio Manager
-   Product Manager
-   Team Lead
-   Team Member

</td><td>

View the progress and status of your Planning Interval's goals, features, overall progress, and team performance.

</td></tr></tbody>
</table>## Reports and data visualizations

<table id="table_dw3_bj5_gbc"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PI progress

</td><td>

Gauge

![PI progress.](../../../use/reporting/image/inline-data-vis-96px-speedometer.png)

</td><td>

sn\_apw\_advanced\_eap\_iteration

</td><td>

Percentage of points completed out of the total scope for this Planning Interval.

</td></tr><tr><td>

Total features

</td><td>

Single Score

![Total features.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

sn\_align\_core\_feature

</td><td>

The total number of features scheduled for this Planning Interval.

</td></tr><tr><td>

Blocked features

</td><td>

Single Score

![Blocked features.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

sn\_align\_core\_feature

</td><td>

Number of features scheduled for this PI that are blocked.

</td></tr><tr><td>

Total story points

</td><td>

Single Score

![Total story points.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

sn\_align\_core\_feature

</td><td>

Total story points for all the features scheduled for this Planning Interval.

</td></tr><tr><td>

Features missing estimates

</td><td>

Single Score

![Features missing estimates.](../../../use/reporting/image/inline-data-vis-96px-single-score.png)

</td><td>

sn\_align\_core\_feature

</td><td>

Number of features, scheduled for this iteration, that have child stories without estimates.

</td></tr><tr><td>

Features by state

</td><td>

Bar graph

![Features by state.](../../../use/reporting/image/inline-data-vis-bar-column.png)

</td><td>

sn\_align\_core\_feature

</td><td>

Features scheduled for this PI, grouped by their current state.

</td></tr><tr><td>

Work item distribution

</td><td>

Donut

![Distribution of work items.](../../../use/reporting/image/inline-data-vis-96px-donut.png)

</td><td>

sn\_align\_core\_feature

</td><td>

Distribution of work items for the selected attribute. You can group the data using one of the following options:

 -   Primary goal
-   Primary goal &gt; Category
-   Strategic program
-   Owner
-   Department

</td></tr><tr><td>

What does the team plan to achieve in this iteration?

</td><td>

List

![Goals list.](../../../use/reporting/image/inline-data-vis-list.png)

</td><td>

sn\_gf\_goal

</td><td>

Status and progress of your Planning Interval's goals.

</td></tr><tr><td>

Team performance

</td><td>

List

![Team list.](../../../use/reporting/image/inline-data-vis-list.png)

</td><td>

sn\_apw\_advanced\_eap\_iteration

</td><td>

Evaluate child teams progress and help them enhance their performance.

 You can choose and rearrange the columns of the report by selecting the ![Settings icon.](../../../reuse/icons/product-icons/gear-outline-24.svg) icon.

</td></tr></tbody>
</table>