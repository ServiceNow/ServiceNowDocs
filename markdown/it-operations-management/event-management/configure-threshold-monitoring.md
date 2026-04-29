---
title: Configure a self-health monitor
description: You can configure a self-health monitor to track Event Management components and see that they do not exceed the specified threshold.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Self-health monitors for Event Management, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure a self-health monitor

You can configure a self-health monitor to track Event Management components and see that they do not exceed the specified threshold.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The Monitoring Configurations \[em\_monitor\_conf\] table lists the records that determine which Event Management components are being monitored. Each record contains the health monitor script that is relevant to what you are monitoring. If you intend to create a new health monitor script, you must configure a monitor to match the purpose of the custom script. You can configure the monitoring configuration records to track the items that are important to you. For example, you can modify the threshold aspect in the **Connector's Idle state monitoring** record, by specifying that the monitoring job frequency is 90 seconds instead of 120 seconds.

**Note:** Each of the monitoring configuration records can be disabled.

If a monitoring configuration specifies a threshold, the configuration value determines what alert severity to display. Threshold values specify the delay time values in units of minutes.

After the **Event Management - self-health monitoring** property is enabled, these jobs are automatically scheduled to run scripts that configure what must be monitored:

-   The `Event Management - Insert Health Monitor` scheduled job runs the scripts. Determine what must be monitored by adding or modifying the script in this job, which runs once every hour.
-   The `Event Management - Update Health Monitor` scheduled job runs the update scripts. This job runs once every minute.

Use the following procedure to configure whether a monitoring configuration can run and set the frequency of the monitoring job. You can specify the threshold values that, if exceeded, trigger an alert.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Self-Health Monitoring**.

2.  From the Monitoring Configurations list, select a monitoring configuration record and modify the required field.

    On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Active|Check box for enabling the monitoring configuration to be active.|
    |Monitoring job frequency \[seconds\]|Frequency that the monitoring job is run.|
    |Critical Threshold|Any point above the value is considered a critical consequence.|
    |Major Threshold|Any point above the value, but below the value of the **Critical Threshold**, is considered a major consequence.|
    |Minor Threshold|If exceeded, the value is considered a minor consequence.|
    |Warning Threshold|If the value is exceeded, a warning is issued.|

3.  Click **Update**.


## Result

The values in the modified monitoring configuration record are compared to the actual values as they occur in events that are received. Alerts are created according to the configuration settings.

## Example

**Example 1:** Use the following procedure to modify the **Critical Threshold** field of the **Connector's Idle state monitoring** monitor from 30 seconds to 35 seconds. This field determines the number of seconds that pass before an alert is generated when the **Critical Threshold** idle state value of a connector is exceeded. In this example, the **Critical Threshold** field is modified from 30 seconds to 35 seconds.

1.  Navigate to **Event Management** &gt; **Settings** &gt; **Self-Health configuration**.
2.  From the Monitoring Configurations list, select **Connector's Idle state monitoring**.
3.  In the **Critical Threshold** field, modify the value to `35`.
4.  Click **Update**.

**Result** The threshold value of the **Critical Threshold** field is increased from `30` to `35`, thereby increasing the number of seconds that pass before an alert is generated for this threshold.

**Example 2:** This example describes the configuration of the severity threshold when using the **Connectors Status** monitor. The **Connector Status** monitor has a true \(= value 1\) or false \(= value 0\) configuration for the severity threshold. For this monitor, where a threshold has the value `1`, then that severity is displayed. Only one severity threshold can have the value`1`. This example assumes that the required severity displayed is `Minor`.

1.  Navigate to **Event Management** &gt; **Settings** &gt; **Self-Health configuration**.
2.  From the Monitoring Configurations list, select **Connectors Status**.
3.  In the **Minor Threshold** field, specify the value `1`.
4.  Click **Update**.

**Result** The monitor issues an alert if the threshold value of the **Minor Threshold** field is exceeded.

## What to do next

Create a customized monitor. A template is provided to assist you to create script that can monitor the specified components. For more information, see [Create a self-health monitor to use custom health monitor script](custom-configure-threshold-monitoring.md).

**Parent Topic:**[Self-health monitors for Event Management](../concept/self-monitoring.md)

