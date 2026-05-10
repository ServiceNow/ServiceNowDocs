---
title: Monitoring and analyzing safety incident metrics
description: The Incident Management tab of the Health and Safety dashboard provides a comprehensive view for monitoring and analyzing safety incident metrics, including incident counts, injury data, observation trends, and action tracking across various organizational levels.
locale: en-US
release: australia
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Monitoring and analyzing safety incident metrics

The **Incident Management** tab of the Health and Safety dashboard provides a comprehensive view for monitoring and analyzing safety incident metrics, including incident counts, injury data, observation trends, and action tracking across various organizational levels.

For any selected period and location, you can drill down into detailed data, empowering your teams to respond faster, improve conditions, and build a safer workplace.

When you have the Generative AI plugin installed, you can view the incident pattern analysis tab on the dashboard. For more information, see [Incident pattern analysis](../../now-assist-health-safety/concept/hs-incident-pattern-analysis.md).

![Incident Management tab showing safety incidents metrics in the Health and Safety dashboard.](../image/hs-incident-mgmt-dashboard.gif)

## Prerequisites

-   Ensure that the Health and Safety Incident Management application is installed. For more information, see [Install Health and Safety Incident Management](../task/install-hs-incident-mgmt.md).
-   Configure total annual hours for an establishment. For more information, see [Add total hours worked for an establishment](../task/add-hs-total-hours-worked-establishment.md).
-   Run the **\[OHS\] Safety Metrics** scheduled job to update the safety metrics on demand. For more information, see [Configure scheduled job to generate frequency rates](../task/configure-job-generate-frequency-rates.md).

    **Note:** The **\[OHS\] Safety Metrics** job is set to run daily by default.


## Required roles

-   sn\_ohs\_im.manager, sn\_ohs\_im.agent, or sn\_ohs\_im.compliance\_manager, needed to see dashboard home page. The metrics on each tab are dependent on the user's access to that table.
-   sn\_ohs\_im.admin and the following roles, to edit the dashboard:
    -   pa\_admin, to edit the Performance Analytics \(PA\) components used in the dashboard.
    -   ui\_builder\_admin, to edit the dashboard visualizations that are built using the UI Builder.

## Access the Health and Safety Incident Management metrics

Navigate to **Workspaces** &gt; **Health and Safety Workspace** and select the **Incident Management** tab on the Health and Safety dashboard.

**Note:**

-   To view a high-level summary of key incident metrics such as the total incidents and recordable injuries, select the **Highlights** tab.
-   To view top incident metrics with data broken down by each establishment for localized analysis, select the **Establishment Metrics** tab. Use the **Establishment** filter in this tab to show the data by establishment.

## Metrics on Incident Management tab

The availability of cards and metrics in this tab depends on the user's access to the table where the data comes from.

<table id="table_dcz_r2l_wfc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

PA indicators

</th></tr></thead><tbody><tr><td>

Number of incidents

</td><td>

Count of open safety incidents and a one-week trend.Select the card to further drill down and visualize data, for example, see trend over different time aggregation of data.

</td><td>

Health &amp; Safety - Open Incidents

</td></tr><tr><td>

Incidents by type

</td><td>

Breakdown of active safety incidents filtered by incident category, for example, injury/illness and near miss, to help identify common risks.Select a category in the bar graph to view a complete list of active safety incidents of that type.

</td><td>

None

</td></tr><tr><td>

Incidents by severity

</td><td>

Breakdown of active safety incidents filtered by severity level, for example, major or minor.Select a severity level in the column chart to view a complete list of active safety incidents of that type.

</td><td>

None

</td></tr><tr><td>

TCIR \(Total case incident rate\)

</td><td>

Number of recordable workplace injuries and illnesses per 100 full-time employees over a one-year period, with the `Location` and `Establishment` breakdowns.The score is calculated according to this formula: `[OHS Total number of Injuries or Illness reported last year from Jan to the end of Dec] * 200000) / [OHS Total Hours Worked Establishment]`

</td><td>

-   OHS - TCIR \(Total Case Incident Rate\)
-   OHS - Total number of Injuries or Illness reported last year - from Jan to the end of Dec
-   OHS - Total Hours Worked Establishment

</td></tr><tr><td>

% Change in open incidents

</td><td>

Line graph highlighting how the number of open incidents has changed \(in percentage\) over time, helping identify increase or reduction in reporting or resolution.Select the card to further drill down and visualize data.

</td><td>

-   Health &amp; Safety - Open Incidents - % Change
-   Health &amp; Safety - Open Incidents

</td></tr><tr><td>

Incident near miss ratio

</td><td>

Ratio of safety incidents reported for the **Near miss** category vs total actual incidents \(example, ones with injury/illness records\) in a calendar year. This metric is useful for assessing proactive safety culture. The score is calculated according to this formula: `[(Health & Safety Near Miss Incidents) / (Health & Safety All Incidents)] * 100`.

</td><td>

-   Health &amp; Safety - Near Miss %
-   Health &amp; Safety - All Incidents
-   Health &amp; Safety - Near Miss Incidents

</td></tr><tr><td>

Active incidents map

</td><td>

Visual geographic spread on a global map showing where active incidents are occurring across regions or sites. It also shows a count of active incidents on the map at each location. You can zoom into locations within a country \(example, state or county\) and drill down to a list of incidents at the lowest level.

</td><td>

None

</td></tr><tr><td>

Incidents by state

</td><td>

Breakdown of active safety incidents by state, that helps track incident resolution progress.Select a state in the graph to view a complete list of active incidents in that state.

</td><td>

None

</td></tr></tbody>
</table><table id="table_cnz_czt_wfc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Recordable injuries this year

</td><td>

Count of injuries deemed recordable that happened in the current year.Select the card to view a complete list of recordable incidents in the year.

</td><td>

None

</td></tr><tr><td>

Days since last injury

</td><td>

Number of days passed since the last injury recorded in the last 12 months, with the `Location` and `Establishment` breakdowns.Select the card to further drill down and visualize data.

</td><td>

-   OHS - Days since last injury and illness report opened
-   OHS - Days since last injury and illness report opened - longest streak
-   OHS - Days since last injury and illness report opened - average streak
-   OHS - Total number of lost work days and transferred or restricted days due to injury or illness

</td></tr><tr><td>

Lost days from injury

</td><td>

Line graph showing the count of lost work days and transferred or restricted days due to injury or illness over last 12 months, with the `OHS.Injury.Illness.Classification` and `Establishment` breakdowns.

</td><td>

-   OHS - Total number of lost work days and transferred or restricted days due to injury or illness
-   OHS - Days since last injury and illness report opened
-   OHS - Days since last injury and illness report opened - longest streak
-   OHS - Days since last injury and illness report opened - average streak

</td></tr><tr><td>

Injury by category

</td><td>

Breakdown of injuries by category per column to help identify common risks.Select a category in the graph to view a complete list of injuries of that type.

</td><td>

None

</td></tr><tr><td>

Injury by severity

</td><td>

Breakdown of active injuries by severity level per column.Select a severity level in the graph to view a complete list of injuries of that type.

</td><td>

None

</td></tr><tr><td>

LTIR \(Lost time case rate\)

</td><td>

Number of incidents involving lost work time per 100 full-time workers. This safety metric is used to measure the frequency and severity of workplace injuries/illnesses resulting in employees missing work.The score is calculated according to this formula: `[OHS Total number of Injuries or Illnesses that resulted in days away from work] * 200000) / [OHS Total Hours Worked Establishment]`

</td><td>

-   OHS - LTIR \(Lost Time Case Rate\)
-   OHS - Total number of Injuries or Illnesses that resulted in days away from work
-   OHS - Total Hours Worked Establishment

</td></tr><tr><td>

LTIFR \(Lost time injury frequency rate\)

</td><td>

How often lost-time injuries occur, usually per one million hours worked.The score is calculated according to this formula: `[OHS Total number of Injuries or Illnesses that resulted in days away from work] * 1000000) / [OHS Total Hours Worked Establishment]`

</td><td>

-   OHS - LTIFR \(Lost Time Injury Frequency Rate\)
-   OHS - Total number of Injuries or Illnesses that resulted in days away from work
-   OHS - Total Hours Worked Establishment

</td></tr><tr><td>

TRIFR \(Total recordable injury frequency rate\)

</td><td>

Number of recordable injury/illness \(needed more than just first-aid\) per a fixed number of hours worked. The score is calculated according to this formula: `[OHS Total number of Injuries or Illnesses that required professional medical treatment] * 1000000) / [OHS Total Hours Worked Establishment]]`

</td><td>

-   OHS - TRIFR \(Total Recordable Injury Frequency Rate\)
-   OHS - Total number of Injuries or Illnesses that required professional medical treatment
-   OHS - Total Hours Worked Establishment

</td></tr><tr><td>

TRSR \(Severity rate\)

</td><td>

Seriousness of incidents, typically based on lost workdays. This metric measures the severity on injury/illness by calculating the average number of lost workdays and restricted workdays per recordable incident, helping to assess the seriousness of incidents in the given period.The score is calculated according to this formula: `[OHS Total number of lost work days and transferred or restricted days due to injury or illness] * 200000) / [OHS Total Hours Worked Establishment]`

</td><td>

-   OHS - TRSR \(Severity Rate\)
-   OHS - Total number of lost work days and transferred or restricted days due to injury or illness
-   OHS - Total Hours Worked Establishment

</td></tr><tr><td>

TRIR \(Total recordable incident rate\)

</td><td>

Number of recordable injuries and illnesses per 100 full-time employees over a one-year period. It's a standardized metric used to measure safety through recordable incidents.The score is calculated according to this formula: `[OHS Total number of Injuries or Illnesses that required professional medical treatment] * 200000) / [OHS Total Hours Worked Establishment]`

</td><td>

-   OHS - TRIR \(Total recordable incident rate\)
-   OHS - Total number of Injuries or Illnesses that required professional medical treatment
-   OHS - Total Hours Worked Establishment

</td></tr><tr><td>

DART \(Days away/restricted or job transfer rate\)

</td><td>

Rate of serious incidents resulting in time away from work, restricted duties, or job transfers. It's a standardized metric used to track incidents that resulted in workers being unable to perform their usual duties and needing to take time off or be transferred to lower impact work duties.The score is calculated according to this formula: `([OHS Total number of Injuries or Illnesses that resulted in days away from work] + [OHS Total number of Injuries or Illnesses that resulted in transferred or restricted days]) * 200000) / [OHS Total Hours Worked Establishment]`

</td><td>

-   OHS - DART \(Days Away/Restricted or Job Transfer Rate\)
-   OHS - Total number of Injuries or Illnesses that resulted in transferred or restricted days
-   OHS - Total number of Injuries or Illnesses that resulted in days away from work
-   OHS - Total Hours Worked Establishment

</td></tr></tbody>
</table><table id="table_gtc_dzt_wfc"><thead><tr><th>

Card

</th><th>

Description

</th><th>

Indicators

</th></tr></thead><tbody><tr><td>

Number of observations

</td><td>

Count of open safety observations including a trend line, with the `Location` breakdown.Select the card to further drill down and visualize data, for example, see trend over different time aggregation of data.

</td><td>

Health &amp; Safety - Open Observations

</td></tr><tr><td>

Overdue corrective actions

</td><td>

Number of corrective type actions that are past their due dates.Select the card to view a complete list of overdue corrective actions.

</td><td>

None

</td></tr><tr><td>

Overdue preventive actions

</td><td>

Number of preventive type actions that are past their due dates.Select the card to view a complete list of overdue preventive actions.

</td><td>

None

</td></tr><tr><td>

Observation status by state

</td><td>

Breakdown of active safety observations by state.Select a state in the graph to view a complete list of active observations in that state.

</td><td>

None

</td></tr><tr><td>

Positive observations reported

</td><td>

Count of positive safety observations that reinforce good practices.Select the card to view a complete list of positive observations.

</td><td>

None

</td></tr><tr><td>

Open corrective and preventive actions

</td><td>

Count of ongoing actions \(both corrective and preventive\) over time. The line graph includes a line for each action type showing a count of each over time.The score is calculated according to this formula: `[Health & Safety Open Actions] - [Health & Safety Open Corrective Actions]`

Select the card to further drill down and visualize its data.

</td><td>

-   Health &amp; Safety - Corrective Actions \#
-   Health &amp; Safety - Open Actions
-   Health &amp; Safety - Open Corrective Actions
-   Health &amp; Safety - Open Preventative Actions

</td></tr><tr><td>

Actions by state

</td><td>

Breakdown of active Health and Safety actions \(created for safety incidents and observations\) by their current state.Select a state column in the graph to view a complete list of active actions in that state.

</td><td>

None

</td></tr></tbody>
</table>## Customizing widgets

You can customize the widgets in the dashboard to display relevant metrics by using the UI Builder. For more information, see [UI Builder tutorial](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/uib-tutorial.md).

