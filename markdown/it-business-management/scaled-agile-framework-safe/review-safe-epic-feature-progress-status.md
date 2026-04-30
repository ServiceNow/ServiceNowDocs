---
title: Reviewing progress status for SAFe features and epics
description: Understand if your work would be completed by the planned end dates by reviewing progress status of your SAFe features and epics.
locale: en-US
release: zurich
product: Scaled Agile Framework \(SAFe\)
classification: scaled-agile-framework-safe
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work Progress Status for SAFe, Scaled Agile Framework \(SAFe\), Strategic Portfolio Management]
---

# Reviewing progress status for SAFe features and epics

Understand if your work would be completed by the planned end dates by reviewing progress status of your SAFe features and epics.

Navigate to **Scaled Agile Framework \(SAFe\)** &gt; **Epics** or **Scaled Agile Framework \(SAFe\)** &gt; **Features** and filter the records for your team.

The Status column of the list shows a Green, Yellow, or Red indicator for each record to indicate the following:

-   Green: Your work is on track to be complete by the planned end date.
-   Yellow: Your work is off track and your plan of execution must be reviewed.
-   Red: Your epic or feature is not progressing well and might be at risk of not being complete by the planned end date.

The estimated completion date displays a date with the likelihood of the epic's or feature's completion.

![A screenshot showing the progress status indicators of SAFe epics](../images/epics-progress-status.png "SAFe epic progress status")

The [\[SAFe\] daily data collection job](../../../use/dashboards/task/enable-safe-daily-data-collection-job.md) helps generate the burnup report for your epics and features. Using the data generated for these epic burnup reports, an estimated completion date is determined. You can see that this date is the intersection of Completed and Scope forecast series in the respective burnup reports.

Based on this estimated completion date, the progress status for your SAFe epics and features is determined. Progress status is calculated only under the following conditions:

-   Planned end date is populated for the SAFe epic and feature.
-   Percentage completion of the epic is a value greater than 0.

The color of the progress status indicator is determined using the following conditions:

-   Green: Estimated completion date is on or before the planned end date.
-   Yellow: Estimated completion date is beyond the planned end date by a deviation of 1% to 14%.
-   Red: Estimated completion date is beyond the planned end date by a deviation of 15% or more.

**Parent Topic:**[Work Progress Status for SAFe](work-progress-status-safe-overview.md)

**Related topics**  


[SAFe Feature Dashboard](../../../use/dashboards/application-content-packs/safe-feature-dashboard.md)

[SAFe Epic Dashboard](../../../use/dashboards/application-content-packs/safe-epic-dashboard.md)

