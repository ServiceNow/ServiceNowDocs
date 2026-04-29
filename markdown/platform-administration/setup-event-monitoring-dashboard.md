---
title: Understand your System Events Dashboard
description: Use the System Event Processing dashboard to set the filters to display information about events and queues.The Scores and tab shows what's going on in the event processing system.Use the Current Scores section to have a direct check on the sysevent table and shows the current states of the events.Use the Trends section to have a metric-based graphical understanding of the activities in the event processing system.Review the details of an alert set every 15 minutes mostly on an instance level. By default, five alerts are provided along with the application. The alerts are setup based on a set of conditions, including what queue it applies to.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Monitor System Events and Scheduled Jobs dashboard, Maintain and monitor, Administer the ServiceNow AI Platform]
---

# Understand your System Events Dashboard

Use the System Event Processing dashboard to set the filters to display information about events and queues.

## Before you begin

Role required: events\_scheduler\_dashboard\_viewer and scheduler\_dasboard\_viewer

## Procedure

1.  Go to **All** &gt; **System Diagnostics** &gt; **System Events Dashboard**.

    ![Image showing System Event Monitoring dashboard](../image/system-events-dashboard.png)

    The System Event Monitoring dashboard shows up.

2.  Select the Queue and Event you want to view the information about.

    **Note:** By default, the default queue is selected. You can also select other queue and event types.

3.  Set the Start and the End dates for which you want to view the queues and events information.

4.  Select Apply to apply the filter set using the above steps.

    **Note:** You can also clear the filter using Clear and make new selections.

    The Scores and Details sections show up based on your selections.


## Scores-System Event processing health checks

The Scores and tab shows what's going on in the event processing system.

<table id="table_wwg_yvf_nxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active Delegators

</td><td>

Indicates whether there is an event delegator enabled. The event delegator is responsible for delegating out events to queues that use the delegated event functionality. Clicking on the card will take you to the list of delegators. Number of delegators in green is positive.**Note:** This card shows up only if the **Queue** uses the delegator model. If this card shows up, the **Active Jobs** card doesn't show up. If no queue is selected, **Active Delegators**, **Active Processors**, and **Active Jobs** cards show up simultaneously.

</td></tr><tr><td>

Active Processors

</td><td>

The number of active event processors in the event system. Click on the card to take you to the list of active processors \(if any\). Number in red indicates that the processor needs to be configured.**Note:** This card shows up only if the **Queue** uses the delegator model. If this card shows up, the **Active Jobs** card doesn't show up. If no queue is selected, **Active Delegators**, **Active Processors**, and **Active Jobs** cards show up simultaneously.

</td></tr><tr><td>

Active Jobs

</td><td>

Number of jobs associated for a queue in processing framework. These jobs are different than the earlier jobs used in the delegator model. In processing framework based on the configuration and checks, the processing jobs are created automatically.

 **Note:** This card shows up only if the **Queue** doesn't use the delegator/dedicated model and is backed by processing framework. If this card shows up, the **Active Delegators** and **Active Processors** cards don't show up. If no queue is selected, **Active Delegators**, **Active Processors**, and **Active Jobs** cards show up simultaneously.

</td></tr><tr><td>

Event Processing Alerts

</td><td>

The number of event processing alerts in the last 5 hour. Clicking on the card takes you to the Events Alerts table that has all the corresponding alerts.

</td></tr><tr><td>

Event Jobs on Schedule

</td><td>

Number of scheduled jobs events that are on schedule.

</td></tr></tbody>
</table>## Scores-Current Scores

Use the Current Scores section to have a direct check on the sysevent table and shows the current states of the events.

|Field|Description|
|-----|-----------|
|Total Events|Total events in the system within the set time period|
|Total Ready|Total events that are ready to be processed|
|Total Processing|Total events that are processing|
|Total Processed|Total events that are already processed|
|Total Error|Total errors in the events|
|Total Transferred|Total events that have been transferred from one chart to the next|

## Scores-Trends

Use the Trends section to have a metric-based graphical understanding of the activities in the event processing system.

**Note:** By default, the trends are set to 24 hours. You can set it up to 15 days.

|Field|Description|
|-----|-----------|
|Event Delegation Trend|Metric collected related to the delegation of events|
|Event Processor Trend|Metric collected for the various events processor|
|Event Trend|Metric for specific events|
|Email/Script action Handler Trend|Metric collected for event handlers|

## Details-Configure an alert

Review the details of an alert set every 15 minutes mostly on an instance level. By default, five alerts are provided along with the application. The alerts are setup based on a set of conditions, including what queue it applies to.

### Before you begin

Role required: events\_scheduler\_dashboard\_viewer and scheduler\_dasboard\_viewer

### Procedure

1.  Go to **All** &gt; **System Policy** &gt; **Events** &gt; **Configure Alerts**.

    The Events Alert Configurations list shows up.

2.  Select one of the available alerts to make changes to the conditions that will trigger an alert.

    **Note:** You receive a notification in the notification icon when the alert is created.

3.  Go to **All** &gt; **System Policy** &gt; **Events** &gt; **Alerts**.

    The Event Alerts list shows up.

    **Note:** The alert conditions are validated every 15 mins approximately.

4.  Select the alert you just updated.

    **Note:** You can open the Event Alert form for the selected alert by selecting the Created column. If you select the Alert Configuration column, the Event Alert Configuration form for the selected alert shows up. You can also open the Event Alert form by selecting the 'i' icon.![Event Alert form.](../image/events-alert-form.png)

5.  Select **Reset alert** if the alert notification is no longer required.


