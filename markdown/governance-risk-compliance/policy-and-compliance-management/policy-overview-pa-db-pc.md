---
title: Policy Overview Performance Analytics dashboard
description: Policies Overview dashboard provides an executive view into compliance requirements, overall compliance, and compliance breakdowns so areas of concern can be identified quickly. Users with the compliance administrator and compliance manager roles view the Policies Overview dashboard.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting solutions for GRC: Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Policy Overview Performance Analytics dashboard

Policies Overview dashboard provides an executive view into compliance requirements, overall compliance, and compliance breakdowns so areas of concern can be identified quickly. Users with the compliance administrator and compliance manager roles view the Policies Overview dashboard.

**Important:** Starting with version 18.1.1 of the Policy and Compliance Management application, the Policy Overview dashboard is available in the Next Experience UI Framework.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

![A short video featuring the different tabs in the Policy Overview dashboard.](../image/policy-overview-pa-db-pc.gif "Policy Overview dashboard")

## Required ServiceNow AI Platform roles

-   Compliance administrator \(sn\_compliance.admin\): To view and edit the details in the Policy Overview dashboard.
-   Compliance reader \(sn\_compliance.reader\): To view the compliance requirements, overall compliance, and compliance breakdowns.

## Access the Policy Overview dashboard

To open the dashboard, navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Analytics Overview**.

## Reports

**Important:** Starting with version 18.1.1 of the Policy and Compliance Management application,the following Policy Overview dashboard reports can be viewed in the Next Experience UI Framework.

|Title|Type|Description|
|-----|----|-----------|
|Control compliance|Donut chart![Donut icon](../../performance-analytics/image/donut-icon.png)|Displays the overall compliance of all the controls in the system.|
|Control details|Donut chart![Donut icon](../../performance-analytics/image/donut-icon.png)|Displays a breakdown of controls grouped by owner, category, or type.|
|Compliance score by department|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)|Overall \(average\) compliance score by assignment group/department|
|Control Overview|Bar chart![Column icon](../../performance-analytics/image/column-icon.png)|Displays control counts exempted by entities.|
|Exempted controls by policy|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)|Displays the number of controls exempted by policies.|
|Exempted controls by entity|Bar chart ![Bar icon.](../../performance-analytics/image/column-icon.png)|Displays a list of control issues that have been closed with a response value of accept, meaning the issue was not remediated.|
|Control Issues by Policy \(Opened Date\)|Line chart![Line icon](../../performance-analytics/image/line-icon.png)|Displays the number of control issues opened each week, grouped by policy.|
|Total Control Objectives by Policy|Bar chart![Bar icon.](../../performance-analytics/image/column-icon.png)|Displays a count of the overall number of control objectives in each policy. The chart is stacked to display control objectives by type.|

**Parent Topic:**[Analytics and Reporting solutions for GRC: Policy and Compliance Management](grc-policy-compliance-content-pack.md)

