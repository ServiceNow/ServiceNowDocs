---
title: Agile 2.0 Prior Release Dashboard
description: Prior Release Dashboard provides data visualization on scope, actual burnup and burndown, and forecast trends of previous releases. Analyze the data and plan the work for upcoming releases.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Performance Analytics Content Pack for Agile 2.0, Agile Development 2.0, Strategic Portfolio Management]
---

# Agile 2.0 Prior Release Dashboard

Prior Release Dashboard provides data visualization on scope, actual burnup and burndown, and forecast trends of previous releases. Analyze the data and plan the work for upcoming releases.

Navigate to **All** &gt; **Agile Development** &gt; **Dashboards** and select **Agile 2.0 Prior Release Dashboard**.

![Agile 2.0 prior release burndown report.](../image/agile-prior-release-burndown.png "Agile 2.0 prior release burndown report")

![Agile 2.0 prior release burnup report.](../image/agile-prior-release-burnup.png "Agile 2.0 prior release burnup report")

**Note:** Canceled stories are not included in any of this data.

## End user and roles

<table id="table_ov2_tj4_2fb"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

Product owner: Needs visibility into actual changes in scope and forecast trends of the previous releases.

</td><td>

scrum\_user

</td><td>

Analyze trends for the following:

-   Scope changes
-   Previous releases

</td></tr></tbody>
</table>## Indicators

-   **Scrum: Sum of story points of completed stories in the active releases**

    Generates the actual burndown series in the Release Burndown report, and the completed series in the Release Burnup report.

-   **Scrum: Sum of story points of all stories in active releases**

    Generates the scope series in the Release Burndown and Release Burnup reports.


## Breakdowns

-   Scrum: Release
-   Scrum: Prior release

## Widgets

-   **Stories Completed**

    Indicates the total number of stories that were completed in the previous release.

-   **Completed**

    Indicates the amount of work \(in story points\) that was completed in the previous release.

-   **Missing Estimates**

    Indicates the total number of stories in the release that are missing estimates.


## Data visualizations

<table id="table_enf_b2k_k3b"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Release Burnup

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Analyze the burnup trends of a previous release.

 The prior release burnup report comprises the following series that can be hidden or displayed based on your preference:

 -   **Scope**: Indicates the amount of work that was planned for the release.
-   **Completed**: Indicates the amount of release work that is complete for this release.

</td></tr><tr><td>

Release Burndown

</td><td>

Line chart![Line chart](../../performance-analytics/image/line-icon.png)

</td><td>

Shows the scope and rate of scope change, the ideal rate for work completion, and the actual rate of work completion. Analyze the burndown trends and accordingly plan the workload for an upcoming release.

 The prior release burnup report comprises the following series that can be hidden or displayed based on your preference:

-   **Scope**: Indicates the amount of work that was planned for the release.
-   **Ideal Burndown**: Indicates how the team had to progress on stories to deliver the release on time.
-   **Remaining**: Indicates the amount of work that is completed.

If the actual burndown \(Remaining\) is above the ideal burndown, it implies that the team was running behind the schedule of the release. If the actual burndown \(Remaining\) is below the ideal burndown, it implies that the team was running ahead of the schedule of the release.


</td></tr></tbody>
</table>You can customize the Burnup and Burndown reports. For more information, see [Customizing Agile 2.0 dashboard reports](../concept/customizing-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Agile 2.0](pa-content-pack-for-agile-2.0.md)

