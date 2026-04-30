---
title: Privacy Management home page
description: The Privacy Management home page provides an overview of the complete privacy risk and compliance posture with details, such as the processing activity criticality score, privacy risk assessment status, privacy impact assessment status, control attestations, issues-specific status, and privacy cases.
locale: en-US
release: yokohama
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Reporting, Privacy Management, Governance, Risk, and Compliance]
---

# Privacy Management home page

The Privacy Management home page provides an overview of the complete privacy risk and compliance posture with details, such as the processing activity criticality score, privacy risk assessment status, privacy impact assessment status, control attestations, issues-specific status, and privacy cases.

The home page is organized into four tabs: **Processing activity**, **Risk and compliance**, **Operations**, and **Privacy cases**.

![Processing activity tab of the Privacy management dashboard.](../image/processing-activity-privacy-management-homepage.png "Privacy management home page")

## Required roles

To view the home page, you must have sn\_privacy.manager and the sn\_privacy.analyst roles.

## Use cases

For examples of how different people in your organization would use this home page, see the following use cases.

|User|Dashboard use|
|----|-------------|
|Privacy manager|The privacy manager can view and understand the privacy compliance posture considering all the processing activities and privacy assessments. They can also view the privacy team's tasks.|
|Privacy analyst|The privacy analyst can view and understand the privacy compliance posture considering only the processing activities assigned to the privacy analyst. They can also access the tasks that need their attention.|

## Processing activity reports

|Title|Description|
|-----|-----------|
|All processing activities by state|Count of processing activities in each state: New, Discover, Review, Monitor, and Retired.|
|Processing activities by criticality score|Distribution of active processing activities by criticality score.|
|Processing activities by department|Number of processing activities grouped by department.|
|Least compliant processing activities|List of processing activities with the lowest compliance scores, including the criticality score and aggregated residual risk.|
|Processing activities by data subject type|Number of processing activities grouped by data subject, such as employees, contractors, customers, and patients.|
|Processing activities by information object category|Number of processing activities grouped by information object, such as demographic data, family background, biometric data, racial or ethnic origin, medical health, and location tracking.|
|Processing activities by type|Distribution of processing activities by type, such as business process, application, business application, or business entity.|
|Processing activities by data processing role|Distribution of processing activities by data processing role, such as controller or processor.|

## Risk and compliance reports

![Reports on the Risk and compliance tab of the Privacy Management home page.](../image/risk-compliance-prm-home-page.png "Risk and compliance dashboard")

|Title|Description|
|-----|-----------|
|Processing activities by aggregated risk score|Distribution of processing activities by aggregated risk score. You can filter by risk classification.|
|Risk heatmap|Distribution of processing activities by residual/inherent risk and control effectiveness levels.|
|Compliance overview|Compliance status of controls for individual authority documents or policies, including the compliance score, related issues, and privacy cases. Toggle between **Authority documents** and **Policies** to switch views.|
|Control objectives needing attention|Control objectives that are marked as non-compliant and the number of impacted processing activities.|

## Operations reports

![Reports on the Operations tab of the Privacy Management home page.](../image/operations-prm-home-page.png "Operations dashboard")

<table id="table_df4_ccz_m3c"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Risk assessments

</td><td>

Number of risk assessments by state \(new and in progress\), including counts for open, overdue, and due in 7 days.

</td></tr><tr><td>

Privacy assessments

</td><td>

Number of privacy assessments by state \(assigned, work in progress, and draft\), including counts for open, overdue, and due in 7 days. You can filter by available assessment templates.

</td></tr><tr><td>

Issues

</td><td>

Number of issues by priority, including counts for open, overdue, and due in 7 days.

</td></tr><tr><td>

Policy exceptions

</td><td>

Number of policy exceptions by risk rating, with counts for open, overdue, and due in 7 days.

</td></tr><tr><td>

Control assurance

</td><td>

Control assurance status across three areas.-   Attestations: Number of open and overdue attestations.
-   Indicators: Number of open indicators and indicators that failed in the last 6 months.
-   Control tests: Number of open and overdue control tests.

</td></tr></tbody>
</table>## Privacy cases reports

|Title|Description|
|-----|-----------|
|Needs attention|Number of overdue cases, cases due in 7 days, and unassigned cases.|
|Case overview|Distribution of cases by state, by breach status, and by priority.|
|Cases|Number of privacy cases. You can filter the view by subtypes.|
|Cases by primary cause|Distribution of privacy cases grouped by primary cause.|
|Opened and closed cases in last 12 months|Trend of opened and closed cases over the last 12 months.|
|Issues|Number of issues by priority, with counts for open, overdue, and due in 7 days.|

**Parent Topic:**[Reporting for Privacy Management](reporting-prm.md)

