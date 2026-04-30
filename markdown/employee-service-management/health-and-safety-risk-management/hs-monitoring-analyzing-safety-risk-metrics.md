---
title: Monitoring and analyzing safety risk metrics
description: The Risk Management tab of the Health and Safety dashboard provides a comprehensive and interactive view for monitoring and analyzing safety risk metrics. By providing real-time insights into inspections, job safety analyses \(JSAs\), and various hazard and risk categories, it enables you to proactively identify trends, respond swiftly to emerging issues, and continuously enhance workplace safety across all organizational levels.
locale: en-US
release: xanadu
product: Health and Safety Risk Management
classification: health-and-safety-risk-management
topic_type: concept
last_updated: "2025-07-06"
reading_time_minutes: 3
breadcrumb: [Health and Safety Risk Management, Health and Safety, Employee Service Management]
---

# Monitoring and analyzing safety risk metrics

The **Risk Management** tab of the Health and Safety dashboard provides a comprehensive and interactive view for monitoring and analyzing safety risk metrics. By providing real-time insights into inspections, job safety analyses \(JSAs\), and various hazard and risk categories, it enables you to proactively identify trends, respond swiftly to emerging issues, and continuously enhance workplace safety across all organizational levels.

For any selected period and location, you can drill down into detailed data for granular visibility for risk mitigation strategies.

![Risk Management tab showing safety risk metrics in the Health and Safety dashboard.](../image/hs-risk-mgmt-dashboard.png)

## Prerequisites

-   Ensure that Health and Safety Risk Management and Health and Safety Incident Management applications are installed. For more information, see [Install Health and Safety Risk Management](../task/install-hs-risk-mgmt.md).
-   Run the **\[OHS\] Safety Metrics** scheduled job to update the safety metrics on demand. For more information, see [Configure scheduled job to generate frequency rates](../../ohs-incident-management/task/configure-job-generate-frequency-rates.md).

    **Note:** The **\[OHS\] Safety Metrics** job is set to run daily by default.


## Required roles

-   sn\_ohs\_im.manager or sn\_ohs\_im.agent, needed to see dashboard home page. The metrics on the **Risk Management** tab are dependent on the user's access to that table.
-   sn\_ohs\_im.admin and the following roles, to edit the dashboard:
    -   pa\_admin, to edit the Performance Analytics \(PA\) components used in the dashboard.
    -   ui\_builder\_admin, to edit the dashboard visualizations that are built using the UI Builder.

## Access the Health and Safety Incident Management metrics

Navigate to **Workspaces** &gt; **Health and Safety Workspace** and select the **Risk Management** tab on the Health and Safety dashboard.

**Note:** To view only a high-level summary of key risk metrics such as the open risk assessments or overdue inspections, select the **Highlights** tab.

## Metrics on Risk Management tab

The availability of cards and metrics in this tab depends on the user's access to the table where the data comes from.

<table><thead><tr><th>

Card

</th><th>

Description

</th><th>

PA indicators

</th></tr></thead><tbody><tr><td>

Overdue inspections

</td><td>

Count of safety inspections that are open past their survey due dates.Select the card to view a complete list of these open inspections.

</td><td>

None

</td></tr><tr><td>

Upcoming inspections

</td><td>

Count of open safety inspections that day and a one-week trend.Select the card to further drill down and visualize data, for example, see trend over different time aggregation of data.

</td><td>

Health &amp; Safety - Open Inspections

</td></tr><tr><td>

Inspection types

</td><td>

Number of active safety inspections with bars counting digital and paper type inspections.Select an inspection format in the graph to view a complete list of active inspections of that type.

</td><td>

None

</td></tr><tr><td>

Inspection findings

</td><td>

Count of open safety inspections' findings that day including a trend line.Select the card to further drill down and visualize data, for example, see trend over different time aggregation of data.

</td><td>

Health &amp; Safety - Inspection Findings

</td></tr></tbody>
</table><table><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Completed JSAs

</td><td>

Count of completed JSAs and a trend line.Select the card to further drill down and visualize data.

</td><td>

Health &amp; Safety - Completed JSAs

</td></tr><tr><td>

Most common JSA selected hazards

</td><td>

Chart of the most common hazards that are selected on JSAs.

</td><td>

None

</td></tr><tr><td>

JSA job types

</td><td>

Number of JSA jobs with bars of counts of multi-step and single step jobs.Select a job type in the graph to view a complete list of jobs of that type.

</td><td>

None

</td></tr></tbody>
</table><table><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Hazards by risk category

</td><td>

Count of active hazards in the system grouped by their risk category.Select a hazard in the bar graph to view a complete list of active hazards of that type.

</td><td>

None

</td></tr><tr><td>

Open risk assessments

</td><td>

Count of open safety risk assessments that day with a trend line.Select the card to further drill down and visualize data.

</td><td>

Health &amp; Safety - Open Risk Assessments

</td></tr><tr><td>

Chemicals by consequence

</td><td>

Count of chemicals based on the **Consequence** level in the chemical record.Select a consequence type column in the bar graph to view a list of active chemicals of that type.

</td><td>

None

</td></tr></tbody>
</table>## Customizing widgets

You can customize the widgets in the dashboard to display relevant metrics by using the UI Builder. For more information, see [UI Builder tutorial](https://www.servicenow.com/docs/access?context=uib-tutorial&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

