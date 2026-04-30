---
title: Processing activity overview page
description: The processing activity overview page provides the privacy risk and compliance posture for a processing activity. This page contains details such the overall compliance score, and trends, privacy criticality assessment scores and risk heatmap based on privacy risk assessments, privacy assessment status, control attestations and issues-specific status.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reporting, Privacy Management, Governance, Risk, and Compliance]
---

# Processing activity overview page

The processing activity overview page provides the privacy risk and compliance posture for a processing activity. This page contains details such the overall compliance score, and trends, privacy criticality assessment scores and risk heatmap based on privacy risk assessments, privacy assessment status, control attestations and issues-specific status.

The vertical layout of a processing activity provides a structured, top-down view that presents information in a clear and sequential manner. This design facilitates an intuitive understanding of the data processing lifecycle by visually representing each step of the workflow in a linear progression. You can easily trace the flow of information from initiation through to completion, enabling better insight into how personal data is collected, used, shared, and retained. This layout supports streamlined navigation and improves the ability to identify key elements and dependencies within the processing activity, enhancing both usability and compliance oversight.

![Reports on the processing activity overview page.](../image/processing-activity-overview.png "Processing activity overview page")

## Required roles

To view the home page, you must have sn\_privacy.manager and the sn\_privacy.analyst roles.

## Use cases

For examples of how different people in your organization would use this home page, see the following use cases.

|User|Dashboard use|
|----|-------------|
|Privacy manager and Privacy analyst|The privacy manager and the privacy analyst can view and understand the privacy compliance posture of the given processing activity.|

## Indicators

**Processing activity compliance score percentage**: Compliance score percentage of processing activity.

## Breakdowns

-   Processing activity
-   Privacy analyst

## Risk overview

The risk overview section displays the processing activity criticality score, the number of high risks with no controls, the details of the on-going risk assessments, and the risk heatmap.

## Reports

This dashboard displays the following reports:

|Title|Type|Description|
|-----|----|-----------|
|Compliance posture by month|Trend chart ![Line chart.](../../../use/performance-analytics/image/line-icon.png)|Compliance posture by month is plotted by referring to the processing activity compliance score.|
|Compliance status|Donut ![Donut chart.](../../../use/reporting/image/icon-donut-report.png)|This report provides the compliance status of all the controls for the processing activity.|
|Controls \(by authority documents or by policies\)|Bar chart ![Bar chart.](../../../use/reporting/image/BarChart.png)|This report provides the compliance status of the controls that are associated with the authority documents or policies.|
|Privacy assessments status|Single score ![Single score.](../../../use/reporting/image/icon-single-score-report.png)|Shows the number of assessments that are open, overdue, and approaching due date.|
|Recently completed privacy assessments|List report ![List report.](../../../use/reporting/image/icon-list-report.png)|Shows the list of recently completed privacy assessments.|
|Issues|Single score ![Single score.](../../../use/reporting/image/icon-single-score-report.png)|Shows the number of issues that are open, overdue, and approaching due date.|
|Issues by priority|Donut![Donut chart.](../../../use/reporting/image/icon-donut-report.png)|Shows the issues by their priority.|
|Policy exceptions|Single score ![Single score.](../../../use/reporting/image/icon-single-score-report.png)|Shows the number of policy exceptions that are active, expiring, and requested.|
|By risk rating|Donut![Donut chart.](../../../use/reporting/image/icon-donut-report.png)|Shows the policy exceptions by their risk ratings.|

**Parent Topic:**[Reporting for Privacy Management](reporting-prm.md)

