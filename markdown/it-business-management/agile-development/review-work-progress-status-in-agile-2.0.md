---
title: Reviewing progress status for Agile Development 2.0 epics
description: Understand if your work would be completed by the planned end dates by reviewing progress status of your Agile Development 2.0 epics.
locale: en-US
release: xanadu
product: Agile Development
classification: agile-development
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Work progress status, Agile Development 2.0, Strategic Portfolio Management]
---

# Reviewing progress status for Agile Development 2.0 epics

Understand if your work would be completed by the planned end dates by reviewing progress status of your Agile Development 2.0 epics.

Navigate to **Agile Development 2.0** &gt; **Epics** and filter the epics for your team.

The Status column of the epics list shows a Green, Yellow, or Red indicator for each epic to indicate the following:

-   Green: Your epic is on track to be complete by the planned end date.
-   Yellow: Your epic is off track and your plan of execution must be reviewed.
-   Red: Your epic is not progressing well and might be at risk of not being complete by the planned end date,

The estimated completion date displays a date with the likelihood of the epic's completion.

![work progress status for epics in Agile 2.0](../images/epic-progress-status.png "Wok progress of Epics")

The [\[Scrum\] daily data collection job](../../../use/dashboards/application-content-packs/enable-daily-data-collection.md) helps generate the burnup report for your epics. Using the data generated for these epic burnup reports, an estimated completion date is determined for each of your epics. You can see that this date is the intersection of Completed and Scope forecast series in the respective epic burnup reports.

Based on this estimated completion date, the progress status for your epics is determined. Progress status for an epic is calculated only under the following conditions:

-   Planned end date is populated in the epic.
-   Percentage completion of the epic is a value greater than 0.

The color of the progress status indicator is determined using the following conditions:

-   Green: Estimated completion date is on or before the planned end date.
-   Yellow: Estimated completion date is beyond the planned end date by a deviation of 1% to 14%.
-   Red: Estimated completion date is beyond the planned end date by a deviation of 15% or more.

**Parent Topic:**[Work Progress Status for Agile Teams](work-progress-status-for-agile-teams.md)

**Related topics**  


[Agile 2.0 Epic Dashboard](../../../use/dashboards/application-content-packs/agile-development-epic-dashboard.md)

