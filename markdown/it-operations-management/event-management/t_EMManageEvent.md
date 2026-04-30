---
title: View events
description: Event Management tracks individual events to manage external systems. These events are notifications from monitoring tools indicating occurrences of interest, like log messages, warnings, or errors. Event Management gathers events from external sources and stores them in the Event \[em\_event\] table, offering a list of raw incoming events.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View events

Event Management tracks individual events to manage external systems. These events are notifications from monitoring tools indicating occurrences of interest, like log messages, warnings, or errors. Event Management gathers events from external sources and stores them in the Event \[em\_event\] table, offering a list of raw incoming events.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, evt\_mgmt\_user, or evt\_mgmt\_integration

**Note:** Ensure that you do not change the **Classification** field value in event \[em\_event\] tables, either manually, by script, or by event rule.

## About this task

The event monitoring tool generates the values of the source and resource fields. Event Management implementers can define event types and register nodes to help uniquely identify incoming events and create alerts for the specific needs of the enterprise. Event Management uses this information to determine whether to create an alert or update an existing one.

An event source may generate duplicate events with the same identifying information. For events with the same identifying information, Event Management uses the time interval between events to determine whether the events represent an existing issue or new issue.

Additional fields should be included in the **Additional information** field of the event. Do not add additional fields to an event by adding a custom field to the event \[em\_event\] table. For more information about how to include additional fields in events, see [Custom alert fields](../concept/populate-custom-alert-fields.md).

**Note:** Avoid writing business rules for event \[em\_event\] tables, as they can result in performance degradation.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

    The All Events list displays the following columns.

<table id="table_vww_5yl_ss"><thead><tr><th>

Column

</th><th>

Description

</th><th>

Populated by

</th></tr></thead><tbody><tr><td>

Time of event

</td><td>

The time that the event occurred, in the network node time zone. The system supports time resolution in seconds.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Source

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Description

</td><td>

Reason for event generation. Shows extra details about an issue. For example, a server stack trace or details from a monitoring tool. Maximum length: 4000 characters.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Node

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Type

</td><td>

The metric type to which the event is related, such as Disk or CPU, which is used to identify an event record from which alerts are created. Maximum length: 100 characters.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Resource

</td><td>

Node resource that is relevant to the event. For example, Disk C, CPU-1, the name of a process, or service. Maximum length: 100 characters.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Metric Name

</td><td>

Unique name that describes which metrics are collected and for which this alert has been created.

</td><td>

External event monitoring tool

</td></tr><tr><td>

Message Key

</td><td>

Unique event identifier to identify multiple events that relate to the same alert. If this value is empty, it is generated from the **Source**, **Node**, **Type**, **Resource**, and **Metric Name** field values. Maximum length: 1024 characters.

</td><td>

External event monitoring tool

</td></tr><tr><td>

State

</td><td>

The status of the event:

-   **Ready**: Event has been received and is waiting to be processed.
-   **Queued**: Event is queued by the event processor job.
-   **Processed**: Event was successfully processed.
-   **Error**: Failure occurred while processing the event. For example, the event collection method or event **Severity** is blank.
-   **Ignored**: Value is not in use.


</td><td>

Event

</td></tr><tr><td>

Severity

</td><td>

Mandatory. The options are typically interpreted as follows:

-   **Critical**: Immediate action is required. The resource is either not functional or critical problems are imminent.
-   **Major**: Major functionality is severely impaired or performance has degraded.
-   **Minor**: Partial, non-critical loss of functionality or performance degradation occurred.
-   **Warning**: Attention is required, even though the resource is still functional.
-   **OK**: An alert is created. The resource is still functional.
-   **Clear**: No action is required. An alert is not created from this event. Existing alerts are closed.


</td><td>

Event

</td></tr><tr><td>

Alert

</td><td>

If an alert was created as a result of the event, this field contains the unique ID that Event Management generates to identify the alert.

</td><td>

A matching event rule or event field mapping

</td></tr></tbody>
</table>2.  To review a single event, click the required row in the **Time of event** column.

3.  To review the event rules that processed the event, in the **Related Links** section click **Check process of event**.

    For further ways to see which event rules were applied to the event, you can display the `Event rule` and `Processing Notes` fields in the Events list.

    ![Optional event rule columns to show event rules](../image/event-rule-column.png)

<table id="table_yjc_jtn_jcb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Matching Event rule

</td><td>

The event rule that matches the current event rule definitions. This information is primarily used to create event rule recommendations for events that currently are not covered by rules. If event rules have been modified, this information can be retrieved from the Processing Notes field, described below. **Note:** This field does not show the history of event rules that were applied to the event.

</td></tr><tr><td>

Processing Notes

</td><td>

Information related to the binding to CI type and the event rules that were applied to the event.

</td></tr></tbody>
</table>4.  To create an event rule for an event that is not associated with an event rule:

    1.  Click the event.

        The event opens in the Event form.

        ![Event Management manage event](../image/all-events-create-event-rule.png)

    2.  Click **Create Event Rule**.

        The fields of the new Event rule are populated with data from the event. You can use the event information, for example, when composing fields for alerts.


