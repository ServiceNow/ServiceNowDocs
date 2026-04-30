---
title: SAFe Prior PI Dashboard
description: The SAFe Prior PI Dashboard provides data visualization on scope, actual burndown, and forecast trends of previous program increments \(PI\). Analyze the data and plan the work for upcoming PIs.
locale: en-US
release: xanadu
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Performance Analytics Content Pack for Essential SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# SAFe Prior PI Dashboard

The SAFe Prior PI Dashboard provides data visualization on scope, actual burndown, and forecast trends of previous program increments \(PI\). Analyze the data and plan the work for upcoming PIs.

![SAFe Prior PI dashboard widgets.](../image/safe-prior-sprint-widgets.png "SAFe Prior PI dashboard widgets")

![SAFe Prior PI burnup report.](../image/safe-prior-pi-burndown.png "SAFe Prior PI burnup report")

![SAFe Prior PI burnup report.](../image/safe-prior-pi-burnup.png "SAFe Prior PI burnup report")

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|SAFe ART user: Analyze the scope, burndown, and forecast trends of previous program increments.|safe\_scrum\_user|

## Indicators

-   **SAFe: Sum of story points of completed stories in the active PIs**

    Generates the actual burndown series in the PI Burndown report, and the completed series in the PI Burnup report.

-   **SAFe: Sum of story points of all stories in active PIs**

    Generates the scope series in the PI Burndown and PI Burnup reports.


## Breakdowns

SAFe: Prior PI.

## Widgets

-   **Features**

    Indicates the total number of features that were planned for completion in the previous PI.

-   **Completed**

    Indicates the total number of features that were completed in the previous PI.

-   **Stories Missing Estimates**

    Indicates the total number of stories in the previous PI that were missing estimates.


## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|PI Burnup|Line chart ![Line chart](../../performance-analytics/image/line-icon.png)|Analyze the burnup trends of the previous PI.|
|PI Burndown|Line chart![Line chart](../../performance-analytics/image/line-icon.png)|View the scope and rate of scope change, the ideal rate for work completion, and the actual rate of work completion. Analyze the burndown trends and accordingly plan the workload for an upcoming PI.|
|PI Velocity Chart|Bar chart![Bar chart](../../performance-analytics/image/column-icon.png)|View the velocity of the ART members for the previous PI and plan the workload for an upcoming PI.|

You can customize the Burnup and Burndown reports. For more information, see [Customizing Essential SAFe dashboard reports](../concept/customizing-safe-dashboard-reports.md).

**Parent Topic:**[Performance Analytics Content Pack for Essential SAFe](pa-content-pack-essential-safe.md)

