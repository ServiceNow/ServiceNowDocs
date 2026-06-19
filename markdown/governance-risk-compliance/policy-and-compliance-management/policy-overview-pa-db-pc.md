---
title: Policy Overview Performance Analytics dashboard
description: Policies Overview dashboard provides an executive view into compliance requirements, overall compliance, and compliance breakdowns so areas of concern can be identified quickly. Users with the compliance administrator and compliance manager roles view the Policies Overview dashboard.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/policy-overview-pa-db-pc.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting solutions for GRC: Policy and Compliance Management, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Policy Overview Performance Analytics dashboard

Policies Overview dashboard provides an executive view into compliance requirements, overall compliance, and compliance breakdowns so areas of concern can be identified quickly. Users with the compliance administrator and compliance manager roles view the Policies Overview dashboard.

**Important:** Starting with version 18.1.1 of the Policy and Compliance Management application, the Policy Overview dashboard is available in the Next Experience UI Framework.

If you are on Vancouver or Washington DC, you can view the dashboard in the Next Experience UI Framework.

\[Omitted image "policy-overview-pa-db-pc.gif"\] Alt text: A short video featuring the different tabs in the Policy Overview dashboard.

## Required ServiceNow AI Platform roles

-   Compliance administrator \(sn\_compliance.admin\): To view and edit the details in the Policy Overview dashboard.
-   Compliance reader \(sn\_compliance.reader\): To view the compliance requirements, overall compliance, and compliance breakdowns.

## Access the Policy Overview dashboard

To open the dashboard, navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Analytics Overview**.

## Reports

**Important:** Starting with version 18.1.1 of the Policy and Compliance Management application,the following Policy Overview dashboard reports can be viewed in the Next Experience UI Framework.

|Title|Type|Description|
|-----|----|-----------|
|Control compliance|Donut chart\[Omitted image "donut-icon.png"\] Alt text: Donut icon|Displays the overall compliance of all the controls in the system.|
|Control details|Donut chart\[Omitted image "donut-icon.png"\] Alt text: Donut icon|Displays a breakdown of controls grouped by owner, category, or type.|
|Compliance score by department|Bar chart \[Omitted image "column-icon.png"\] Alt text: Bar icon.|Overall \(average\) compliance score by assignment group/department|
|Control Overview|Bar chart\[Omitted image "column-icon.png"\] Alt text: Column icon|Displays control counts exempted by entities.|
|Exempted controls by policy|Bar chart \[Omitted image "column-icon.png"\] Alt text: Bar icon.|Displays the number of controls exempted by policies.|
|Exempted controls by entity|Bar chart \[Omitted image "column-icon.png"\] Alt text: Bar icon.|Displays a list of control issues that have been closed with a response value of accept, meaning the issue was not remediated.|
|Control Issues by Policy \(Opened Date\)|Line chart\[Omitted image "line-icon.png"\] Alt text: Line icon|Displays the number of control issues opened each week, grouped by policy.|
|Total Control Objectives by Policy|Bar chart\[Omitted image "column-icon.png"\] Alt text: Bar icon.|Displays a count of the overall number of control objectives in each policy. The chart is stacked to display control objectives by type.|

**Note:** You can view this dashboard directly from the Compliance Workspace as well. For more information, see [View dashboards in Compliance Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-compliance-management-workspace/view-dashboards-in-compliance-workspace.md)

**Parent Topic:**[Analytics and Reporting solutions for GRC: Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/grc-policy-compliance-content-pack.md)

