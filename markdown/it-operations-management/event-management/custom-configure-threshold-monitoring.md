---
title: Create a self-health monitor to use custom health monitor script
description: You can create a self-health monitor to use custom health monitor script to monitor specified Event Management components.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Self-health monitors for Event Management, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Create a self-health monitor to use custom health monitor script

You can create a self-health monitor to use custom health monitor script to monitor specified Event Management components.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

To augment the self-health monitors that are provided with the base system, you can create a self-health monitor to monitor the components that you specify. The health monitor scripts that are provided with the base system are listed in the following table.

<table id="table_d5c_tz4_4cb"><thead><tr><th>

Health monitor script

</th><th>

Used by a monitor to:

</th></tr></thead><tbody><tr><td>

Check delay in event processing

</td><td>

Monitor the duration of events \[in minutes\] that remain in Ready state and are not processed.

</td></tr><tr><td>

Connectors Monitor

</td><td>

Monitor:-   Whether the time that a connector in idle state surpassed the threshold \[in minutes\] configured.
-   The active status of connectors.

</td></tr><tr><td>

Get Event Processing state

</td><td>

Monitor the time that events are in Ready state. Alerts are sent when this time exceeds the threshold.

</td></tr><tr><td>

MID Server Threshold Alerts

</td><td>

Monitor MID Server health. Events are sent when changes in MID Server state are detected.

</td></tr></tbody>
</table>You can create alert management rules to respond to and remediate the issues detected by self-health. Alerts are generated based on the specified severity and threshold. Navigate to **Event Management** &gt; **Administration** &gt; **Self-Health Monitoring** for the monitors that are provided with the base instance to monitor the issues detected by self-health, which are:

<table id="table_z5y_qkq_1fb"><thead><tr><th>

Monitor

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connector's idle state monitoring

</td><td>

Monitor to verify whether any of the connectors were in idle state that surpassed the threshold \[in minutes\] that was configured.Health Monitor script selected: `Connectors Monitor`.

</td></tr><tr><td>

Connectors Status

</td><td>

Monitor to track the active status of the connectors. Select only one threshold to configure which severity to invoke using 1 to select the threshold field or 0 to ignore the threshold field. For more information, see [Connector status example](configure-threshold-monitoring.md#threshold-example). Health Monitor script selected: `Connectors Monitor`.

</td></tr><tr><td>

Delay in event processing

</td><td>

Monitor to track the duration of events \[in minutes\] that remain in Ready state and were not processed. This duration period initiates an alert for the event processing CI with severity according to the configured thresholds \[minutes\].Health Monitor script selected: `Check delay in event processing`.

</td></tr><tr><td>

Event Processing job

</td><td>

Monitor the state of the event processing jobs. An alert is generated when the idle time of a job exceeds the configured threshold.Health Monitor script selected: `Get Event Processing state`.

</td></tr><tr><td>

MID Server MID Server Threshold Alerts

</td><td>

Monitor MID Server MID Server health. Events are sent when issues with MID Server availability and resource thresholds are detected.Health Monitor script selected: `MID Server Threshold Alerts`.

</td></tr></tbody>
</table>**Note:** To prevent a self-health monitor from detecting the connector status, at any time you can clear the **Active** check box of the monitor and then click **Update**.

## Procedure

1.  Navigate to **Event Management** &gt; **Administration** &gt; **Self-Health Monitoring**, and click **New**.

2.  On the form, fill in the fields.

<table id="table_xms_j2p_4cb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Descriptive and meaningful name for the monitor.

</td></tr><tr><td>

Description

</td><td>

Text narrative that describes the monitor.

</td></tr><tr><td>

Active

</td><td>

Check box to enable the monitor.

</td></tr><tr><td>

Monitoring job frequency \[seconds\]

</td><td>

Frequency that the monitoring job should run. Default: `120` seconds.

</td></tr><tr><td>

Last Run

</td><td>

Last run date and time. These values are automatically updated.

</td></tr><tr><td>

Script

</td><td>

Monitoring script. Click the search icon. The existing scripts are listed in the Health Monitor Scripts screen, or click **New** to create a custom health monitor script. For more information about creating a custom health monitor script, see step [3](custom-configure-threshold-monitoring.md#step_4_custom).

</td></tr><tr><td colspan="2">

**Note:** Regarding all the following threshold configuration fields: All monitored values are compared against the thresholds. If a monitored value exceeds a threshold, an alert with the appropriate severity is issued.

</td></tr><tr><td>

Critical Threshold

</td><td>

Any point above the value is considered a critical consequence.

</td></tr><tr><td>

Major Threshold

</td><td>

Any point above the value, but below the value of the Critical Threshold, is considered a major consequence.

</td></tr><tr><td>

Minor Threshold

</td><td>

If exceeded, the value is considered a minor consequence.

</td></tr><tr><td>

Warning Threshold

</td><td>

If the value is exceeded, a warning is issued.

</td></tr><tr><td>

Additional information

</td><td>

Further information about the monitor.

</td></tr></tbody>
</table>3.  To create a custom health monitor script, on the Monitoring Configuration form, next to the **Script** field, click the search icon to open the Health Monitor Scripts form, and click **New**.

4.  On the form, fill in the fields.

<table id="table_w34_sg2_2fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check box to enable the monitor.

</td></tr><tr><td>

Description

</td><td>

Text narrative that describes the custom script.

</td></tr><tr><td>

Name

</td><td>

Descriptive and meaningful name for the custom script.

</td></tr><tr><td>

Script

</td><td>

Custom script to run when called from a monitor. A script template is provided as a guide. You can use the [Health monitor scripts provided with the base system](custom-configure-threshold-monitoring.md#table_d5c_tz4_4cb) as examples of how to author the script, and use the script editor tools.

Ensure that the custom script includes:Run the monitor function, which is called according to the "monitoring job frequency” setting **runUpdateHealthMonitorScripts\(scriptId\)**. Add this function to run the monitoring logic.

 Specify the configuration function that is called every hour **runInsertHealthMonitorScripts\(scriptId\)**. Add the configuration logic and add a CI if needed. In the navigation pane search field, enter `em_monitor_state.list`. In the Monitoring States \[em\_monitor\_state\] table, specify the initialization of the monitor record in the required record.

 Use the helper functions defined in **EvtMgmtHealthMonitorCommon** and **EvtMgmtEventAlertGenerator** script includes:

 -   EvtMgmtHealthMonitorCommon
-   healthMonitorCommon.shouldRun
-   healthMonitorCommon.calculateSeverity
-   EvtMgmtEventAlertGenerato
-   openAlert
-   closeAlert


</td></tr></tbody>
</table>    You can use the Monitoring Configurations \[em\_monitor\_conf\] table for self-health monitoring configuration, the Health Monitor Scripts \[em\_monitor\_scripts\] table for scripts, and Monitoring States \[em\_monitor\_state\] table for displaying the results of the monitor, as initialized inside **runInsertHealthMonitorScripts**.

    For more information about script includes and APIs, see:Script includes that are [installed with Event Management](../reference/r_InstalledWithEventManagement.md#)

5.  Click **Submit**.


## Result

To monitor the Event Management components that you specify, you can configure a self-health monitor that uses the custom health monitor script that you created.

**Parent Topic:**[Self-health monitors for Event Management](../concept/self-monitoring.md)

