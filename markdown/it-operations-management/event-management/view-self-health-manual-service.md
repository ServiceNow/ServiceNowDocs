---
title: View the Event Management self-health application services map
description: You can view Event Management application services maps to have a visualization of the data on configuration items \(CIs\) that comprise this service, and the relations and connections between these CIs.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Self-health monitors for Event Management, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View the Event Management self-health application services map

You can view Event Management application services maps to have a visualization of the data on configuration items \(CIs\) that comprise this service, and the relations and connections between these CIs.

## Before you begin

Role required: evt\_mgmt\_admin

The Event Management application services topology map only displays MID Servers that have passed validation and connectors that are active.

## About this task

The Event Management components that are monitored by the self-health application services are listed in the following table:

<table id="table_znl_gzs_ncb"><thead><tr><th>

Component

</th><th>

What is monitored

</th></tr></thead><tbody><tr><td>

Event connectors

</td><td>

For each connector:-   Status: Success or Error
-   Delay: Elapsed time from ‘last run time’ \(above threshold\)

</td></tr><tr><td>

Event processing jobs

</td><td>

For each event processing job:-   Number of actual jobs executed compared to the number of jobs configured to run.
-   Delay of any of the event processing jobs above the time set as threshold.
-   Duration of events in Ready state compared to the specified threshold.
-   Delay of event rule processing above the set threshold. If there is a delay, an alert is generated and the event rule is disabled.

</td></tr><tr><td>

MID Servers

</td><td>

MID Servers that have been validated are displayed. The MID Server status and the `Ecc_agent_issue` table are monitored. An event is triggered whenever this table is updated. The MID Server status is displayed, either **Up** or **Down**.For information about MID Server health, see [MID Server heartbeat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/r_MIDServerHeartbeat.md)

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Application Services**.

2.  Click the **ServiceNow Event Management** application services.

3.  On the **Application Services** page, locate **ServiceNow Event Management** and click **View Service**.

    ![Event Management health — application service](../image/application-service.png)

    Displayed on the map are the related MID Servers and the Event Management object, as depicted in the following image; these MID Servers have an **UP** status. MID Servers are updated when they are created or deactivated.

    ![Event Management application service map](../image/view-map.png)

    Under the Event Management object is Event Processing, Alert Processing, and Event Sources \(for example, connectors\). Only **Active** connectors are shown; when a connector is created, the connector is displayed only after it has been activated. The status of active connectors is updated and the status of non-active connectors is not displayed.

    In the preceding image, the health of Event Management components is displayed. The omniConnector component has a red bar, indicating that a critical alert has occurred that affects this connector. In addition, this critical alert impacts the parent Alert Processing object, which as a result, has a red bar.


## Result

You can select the configuration item that has a critical alert and change the impact from parent to application service.

**Parent Topic:**[Self-health monitors for Event Management](../concept/self-monitoring.md)

