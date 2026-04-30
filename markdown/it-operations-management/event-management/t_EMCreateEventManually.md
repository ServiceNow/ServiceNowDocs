---
title: Testing and sending events
description: You can manually test and send events to confirm that Event Management properly manages events and generates alerts.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Testing and sending events

You can manually test and send events to confirm that Event Management properly manages events and generates alerts.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

For example, you can manually send events to:

-   Confirm that the MID Server is using an event connector definition and instance to send events.
-   Confirm that event rules, event field mapping, and other configurations do generate alerts.
-   Track an operation or action that did not generate an event.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **All Events**.

2.  Click **New** and then fill in the fields.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Source

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Node

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td></tr><tr><td>

Type

</td><td>

The metric type to which the event is related, such as Disk or CPU, which is used to identify an event record from which alerts are created. Maximum length: 100 characters.

</td></tr><tr><td>

Resource

</td><td>

Unique event identifier to identify multiple events that relate to the same alert. If this value is empty, it is generated from the **Source**, **Node**, **Type**, **Resource**, and **Metric Name** field values. Maximum length: 1024 characters.

</td></tr><tr id="row_cmf_1t4_fz"><td>

Metric Name

</td><td>

The name of the metric that has been measured, such as `DB Disk Free Space (MB)`, `Disk Writes/sec`, or `Disk Write Bytes/sec`.

</td></tr><tr><td>

Source instance

</td><td>

Name of the machine or software that generated the event. For example, SolarWinds on 10.22.33.44. Corresponding field display name is **Source Instance**.

</td></tr><tr><td>

Message key

</td><td>

Unique event identifier to identify multiple events that relate to the same alert. If this value is empty, it is generated from the **Source**, **Node**, **Type**, **Resource**, and **Metric Name** field values. Maximum length: 1024 characters.

</td></tr><tr><td>

Severity

</td><td>

The severity of the event. The options are typically interpreted as follows: -   **Critical**: Immediate action is required. The resource is either not functional or critical problems are imminent.
-   **Major**: Major functionality is severely impaired or performance has degraded.
-   **Minor**: Partial, non-critical loss of functionality or performance degradation occurred.
-   **Warning**: Attention is required, even though the resource is still functional.
-   **Clear**: No action is required. An alert is not created from this event. Existing alerts are closed.
-   **OK**: An alert is created. The resource is still functional.


</td></tr><tr><td>

Resolution state

</td><td>

Optional. If the field is empty, the resolution on corresponding alerts is still pending. Event state from the event source is either **New** or **Closing**. -   **New**, the resolution on corresponding alerts is open.
-   **Closing** event state closes corresponding alerts.


</td></tr><tr><td>

Time of event

</td><td>

Time that the event occurred in the source system. This field is a GlideDateTime field in UTC or GMT format. Maximum length: 40 characters.

</td></tr><tr><td>

State

</td><td>

The current processing state of the event: -   **Ready**: Event has been received and is waiting to be processed.
-   **Processed**: Event was successfully processed.
-   **Ignored**: Value is not in use.
-   **Error**: Failure occurred while processing the event. For example, the event collection method or event **Severity** is blank.


</td></tr><tr><td>

Alert

</td><td>

If an alert was created as a result of the event, this field contains the unique ID that Event Management generates to identify the alert.

</td></tr><tr><td>

Description

</td><td>

Reason for event generation. Shows extra details about an issue. For example, a server stack trace or details from a monitoring tool. Maximum length: 4000 characters.

</td></tr><tr><td>

Additional information

</td><td>

A JSON string that gives more information about the event. The JSON data is supported for String values only, other value types are not supported. You must convert numbers to String values by enclosing them in double quotes. For example, this value is not supported: \{"CPU":100 \} while this value is supported: \{"CPU":"100"\}. Another example of a valid JSON string is: \{"evtComponent":"Microsoft-Windows-WindowsUpdateClient","evtMessage":"Installation Failure: Windows failed. Error 0x80070490"\}. This information can be used for third-party integration or other post-alert processing. Values in the **Additional information** field of an Event that are not in JSON key/value format are normalized to JSON key/value format when the event is processed. For example, assume that the following plain text is in the **Additional information** field “Connection instance is successful”. When the event is processed, all this plain text becomes one JSON string and might not be useful within an alert. In the resultant alert, this string is in the **Additional information** field in JSON key/value format, containing the data: \{“additional\_content”: “Connection instance is successful"\}.

</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Processing Events](../concept/processing-events.md)

