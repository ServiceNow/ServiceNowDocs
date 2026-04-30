---
title: CAM Overview dashboard
description: The CAM Overview dashboard provides multiple tabs with reports on critical aspects of your CAM security posture.
locale: en-US
release: zurich
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Analytics and Reporting, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM Overview dashboard

The CAM Overview dashboard provides multiple tabs with reports on critical aspects of your CAM security posture.

## Accessing the dashboard

Users with the CAM Administrator \[sn\_irm\_cont\_auth.admin\] or Executive Reader \(sn\_irm\_cont\_auth.executive\_read\) role can view the tabs on the CAM Overview dashboard.

Users with the following roles can access the dashboard:

-   CAM Administrator \(sn\_irm\_cont\_auth.admin\)
-   Executive Reader \(sn\_irm\_cont\_auth.executive\_read\)
-   System Owner \(sn\_irm\_cont\_auth.system\_owner\)
-   Information System Security Manager \(sn\_irm\_cont\_auth.info\_system\_sec\_manager\)
-   Information System Security Officer \(sn\_irm\_cont\_auth.info\_system\_sec\_officer\)

To open the dashboard, navigate to **All** &gt; **Continuous Authorization &amp; Monitoring** &gt; **Analytics Dashboards** &gt; **CAM Overview**.

## Tabs on the dashboard

![Tabs on the CAM overview dashboard.](../../../product/grc-cam/image/cam-ovrvw-dashboard-washingtondc.gif)

|Title|Type|Source table|Description|
|-----|----|------------|-----------|
|Authorization boundary tab|
|Boundaries connected to CMDB|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)|System elements \[sn\_irm\_cont\_auth\_boundary\_element\]|The number of authorization boundaries defined to work with your CMDB.|
|Mission critical boundaries|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization boundaries defined as being mission critical. For more information, see [Define the authorization boundary](../../../product/grc-cam/task/define-auth-boundaries.md).|
|Orphan authorization boundaries|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization boundaries not related to an authorization package.|
|Boundaries status|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of authorization boundaries in each state.|
|Authorization packages tab|
|Packages with overridden impact|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization packages with an impact that have been overridden. For more information, see [Risk Management Framework \(RMF\) step 1 - Categorize the authorization package](../../../product/grc-cam/task/categorize.md).|
|Packages pending approval|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization packages for which approval has been requested, but that haven’t yet received approval.|
|Packages by impact|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of authorization packages categorized by impact levels.|
|Packages by step|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of authorization packages categorized by steps \(for example, Monitor, Access, Select, and so on\).|
|Baseline controls tab|
|Packages with inherited controls|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization packages that contain baseline controls inherited from a common control.|
|Packages with common controls|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization packages for which common controls were created and implemented.|
|Packages with unimplemented controls|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of authorization packages for which common controls were created, but haven’t yet been implemented.|
|POA&amp;M tab|
|Pending POA&amp;Ms|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of Plans of Action and Milestones \(POA&amp;M\) that are pending authorization.|
|POA&amp;Ms with milestones|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of POA&amp;Ms that contain milestones.|
|POA&amp;Ms with acceptance tasks|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of POA&amp;Ms that contain acceptance tasks.|
|Overdue POA&amp;Ms|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of POA&amp;Ms that have overdue milestones or acceptance tasks.|
|POA&amp;Ms by state|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of POA&amp;Ms categorized by state.|
|Packages with POA&amp;Ms|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of authorization packages that contain POA&amp;Ms.|
|POA&amp;Ms by priority|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of POA&amp;Ms categorized by priority.|
|POA&amp;Ms by response|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of POA&amp;Ms categorized by responses.|
|Assess activity tab|
|Inadequate engagements|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of engagements closed with an inadequate result.|
|Satisfactory engagements|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of engagements closed with a satisfactory result.|
|Adequate engagements|Single Score ![Single-score icon.](../../performance-analytics/image/single-score.png)| |The number of engagements closed with an adequate result.|
|Controls by engagement|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |The number of controls categorized by engagements.|
|Audit task breakdown|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |Audit tasks grouped or stacked, or both, by task type, assigned user, top task, or state.|
|POA&amp;M breakdown|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |POA&amp;Ms grouped or stacked, or both, by engagement, state, or response.|
|Control test results|Donut chart![Donut icon.](../../performance-analytics/image/donut-icon.png)| |The number of completed control tests, broken down by overall control effectiveness rating.|
|Engagement results|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)| |An overall count of audit engagements conducted for each entity. The chart is stacked to display the overall audit results for each entity.|
|Overdue audit tasks|List ![List icon.](../../performance-analytics/image/scorecard-icon.png)| |List of open audit tasks that have exceeded the planned end date.|

