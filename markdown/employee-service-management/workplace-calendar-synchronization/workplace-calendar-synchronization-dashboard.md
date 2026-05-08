---
title: Synchronization Health Dashboard
description: Use this dashboard to track the reservation synchronization. Monitor number of events and calendar items created in the application and other details related to them.
locale: en-US
release: australia
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Analytics and Reporting Solutions for Workplace Calendar Synchronization, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Synchronization Health Dashboard

Use this dashboard to track the reservation synchronization. Monitor number of events and calendar items created in the application and other details related to them.

**Note:** The Workplace Calendar Synchronization dashboard is migrated to Workplace Central. You can start using the migrated dashboards from Workplace Central. The out-of-the-box dashboards are also migrated to Workplace Central. Old dashboards are not supported for new Workplace Service Delivery customers. For existing customers, old dashboards are currently available but will be deprecated soon.

For more information about the migrated dashboard, see [Reservation Management dashboard](reservation-management-dashboard.md).

![Synchronization health dashboard](../image/workplace-calendar-synchornization-dashboard.png "Synchronization health dashboard")

To access the Synchronization health dashboard, navigate to **All** &gt; **Workplace Central** &gt; **Workplace Dashboards**.

## End user and roles

<table id="table_igp_q51_c4b"><thead><tr><th>

End user and goal

</th><th>

Required role

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

System administrator and Workplace Calendar Synchronization admin: Needs visibility into the real-time status of the events and calendar items created in the application.

</td><td>

sn\_wsd\_rsvsync.admin

</td><td>

-   View Connection configuration.
-   View Calendar providers.
-   Create, manage, and edit a Reservable Sync Configuration.

</td></tr></tbody>
</table>## Data visualizations

|Title|Type|Description|
|-----|----|-----------|
|Total events today|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of events created on the current day.|
|Calendar items generated today|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of calendar items generated in the current day.|
|Breakdown calendar items by type|Pie breakdown ![pie breakdown icon](../../performance-analytics/image/pie-breakdown-wthoutlabel.png)|Breakdown of the calendar items based on their type|
|Calendar items generated over last 7 days|Step time series![step time series icon](../../performance-analytics/image/step-time-series-small.png)|Number of calendar items generated in the last 7 days.|
|Events processed over last 7 days|Step time series![step time series icon](../../performance-analytics/image/step-time-series-small.png)|Number of events processed in the last 7 days.|
|Events that are yet to be processed|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of events that are yet to be processed.|
|Events in error in last 24 hours|Single score ![Single-score icon](../../performance-analytics/image/single-score.png)|Number of events generated with errors in the last 24 hours.|
|Breakdown events in error over the last 30 days|Pie breakdown ![pie breakdown icon](../../performance-analytics/image/pie-breakdown-wthoutlabel.png)|Breakdown of events generated with errors over the last 30 days.|
|Events in error, unable to be processed by provider over last 30 days|Step time series![step time series icon](../../performance-analytics/image/step-time-series-small.png)|Number of events generated with errors that could not be processed by provider over the last 30 days.|
|Events in error not sent to provider over last 30 days|Step time series![step time series icon](../../performance-analytics/image/step-time-series-small.png)|Number of events generated with errors that were not sent to the provider over the last 30 days.|
|List of all events in error state over last 30 days|List|List of all the events that have been in the error state over the last 30 days.|

**Parent Topic:**[Manage Workplace Dashboards](../../../product/workplace-central/task/workplace-dashboards-wsd-central.md)

