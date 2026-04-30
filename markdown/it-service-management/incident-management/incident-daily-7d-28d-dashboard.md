---
title: Legacy: Incident Daily 7d - 28d dashboard
description: View the last 28 days of incidents as raw trends, as a 7-day running average, or as a 28-day running average. Filter the scores by assignment groups or by the category of incident.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Legacy: Incident Management Platform Analytics Solutions, Analytics and reporting, Incident Management, IT Service Management]
---

# Legacy: Incident Daily 7d - 28d dashboard

View the last 28 days of incidents as raw trends, as a 7-day running average, or as a 28-day running average. Filter the scores by assignment groups or by the category of incident.

**Important:**

Starting in Xanadu release, the Incident Daily 7d - 28d dashboard is deprecated. Users can use [Incident management dashboard](performance-analytics/incident.md) to view the last 28 days of incidents as raw trends, as a 7-day running average, or as a 28-day running average and filter the scores by assignment groups or incident.

![Incident Daily tab of the Incident daily 7d-28d breakdown dashboard](../image/incident-7d-28d-daily.png "Incident Daily tab")

![Incident 7 day tab of the Incident daily 7d-28d breakdown dashboard](../image/incident-7d.png "Incident 7d tab")

![Incident 28 day tab of the Incident daily 7d-28d breakdown dashboard](../image/incident-28d.png "Incident 28d (lower part)")

|End user and goal|Required role|
|-----------------|-------------|
|Incident Manager: Needs to know how the incident management process is doing so they can plan for the future.|itil|

## Indicators

-   **Number of open incidents**

    Daily count of the number of incidents that do not have a resolution date. This indicator is used as the basis of several other indicators on this dashboard.

-   **Number of resolved incidents**

    Daily count of indicators with State = Resolved.

-   **Average resolution time of resolved incidents**

    The average number of days it takes to resolve an incident, provided it is resolved. The score is calculated according to the formula \[\[Summed duration of resolved incidents\]\] / \(\[\[Number of resolved incidents\]\] \* 24\).

-   **Number of open incidents not updated in last 5 days**

    Daily count of the number of incidents last updated more than five days ago.

-   **Number of open incidents not updated in last 30 days**

    Daily count of the number of incidents last updated more than 30 days ago.


## Breakdowns

You can apply breakdown elements on this dashboard to all widgets simultaneously. Above the chart in the upper left, select either Groups or Incident.Category. You can then select one or more elements and they will apply to all widgets.![Selecting the breakdown source and breakdown elements on the dashboard](../image/incident-daily-select-bkdn-elemnt.png)

**Parent Topic:**[Legacy: Incident Management Platform Analytics Solutions](incident-content-pack.md)

