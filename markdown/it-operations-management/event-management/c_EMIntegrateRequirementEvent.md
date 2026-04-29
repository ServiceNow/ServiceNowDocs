---
title: Event field format for event collection
description: Event Management requires all events to use a standard form, regardless of how they arrive at the instance.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event field format for event collection

Event Management requires all events to use a standard form, regardless of how they arrive at the instance.

In the application navigation filter, enter `em_event.list`.

<table id="table_vy2_525_jq" class="parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

em\_event.source \[Source\]

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

em\_event.node \[Node\]

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td></tr><tr><td>

em\_event.type\[Type\]

</td><td>

Optional. The metric type to which the event is related, such as Disk or CPU, which is used to identify an event record from which alerts are created. Maximum length: 100 characters.

</td></tr><tr><td>

em\_event.resource \[Resource\]

</td><td>

Node resource that is relevant to the event. For example, Disk C, CPU-1, the name of a process, or service. Maximum length: 100 characters.

</td></tr><tr id="row_cmf_1t4_fz"><td>

metric\_name\[Metric Name\]

</td><td>

The name of the metric that has been measured, such as `DB Disk Free Space (MB)`, `Disk Writes/sec`, or `Disk Write Bytes/sec`.

</td></tr><tr><td>

em\_event.event\_class \[Source instance\]

</td><td>

If the em\_event.node field is not specified, it is mandatory for alerts to be created automatically. Values for the em\_event.event\_class field originate from either the source generating the events or by event rule. Name of the machine or software that generated the event. For example, SolarWinds on 10.22.33.44. Corresponding field display name is **Source Instance**.

</td></tr><tr><td>

em\_event.message\_key\[Message key\]

</td><td>

Unique event identifier to identify multiple events that relate to the same alert. If this value is empty, it is generated from the **Source**, **Node**, **Type**, **Resource**, and **Metric Name** field values. Maximum length: 1024 characters.

</td></tr><tr><td>

em\_event.ci\_type\[CI type\]

</td><td>

String containing information about CI type. Maximum length: 100 characters.

</td></tr><tr><td>

em\_event.severity\[Severity\]

</td><td>

Event severity options are: -   **Critical**: Immediate action is required. The resource is either not functional or critical problems are imminent.
-   **Major**: Major functionality is severely impaired or performance has degraded.
-   **Minor**: Partial, non-critical loss of functionality or performance degradation occurred.
-   **Warning**: Attention is required, even though the resource is still functional.
-   **OK**: An alert is created. The resource is still functional.
-   **Clear**: No action is required. An alert is not created from this event. Existing alerts are closed.

</td></tr><tr><td>

em\_event.resolution\_state\[Resolution state\]

</td><td>

Optional. If the field is empty, the resolution on corresponding alerts is still pending. Event state from the event source is either **New** or **Closing**. -   **New**, the resolution on corresponding alerts is open.
-   **Closing** event state closes corresponding alerts.

</td></tr><tr><td>

em\_event.time\_of\_event\[Time of event\]

</td><td>

Time that the event occurred in the source system. This field is a GlideDateTime field in UTC or GMT format. Maximum length: 40 characters.

</td></tr><tr><td>

em\_event.state\[State\]

</td><td>

Current processing state of the event: -   **Ready**: Event has been received and is waiting to be processed.
-   **Processed**: Event was successfully processed.
-   **Ignored**: Value is not in use.
-   **Error**: Failure occurred while processing the event. For example, the event collection method or event **Severity** is blank.

</td></tr><tr><td>

em\_event.alert\[Alert\]

</td><td>

If an alert was created as a result of the event, this field contains the unique ID that Event Management generates to identify the alert.

</td></tr><tr><td>

em\_event.description\[Description\]

</td><td>

Reason for event generation. Shows extra details about an issue. For example, a server stack trace or details from a monitoring tool. Maximum length: 4000 characters.

</td></tr><tr><td>

em\_event.additional\_info\[Additional information\]

</td><td>

Optional. A JSON string that gives more information about the event. The JSON data is supported for String values only, other value types are not supported. You must convert numbers to String values by enclosing them in double quotes. For example, this value is not supported: \{"CPU":100 \} while this value is supported: \{"CPU":"100"\}. Another example of a valid JSON string is: \{"evtComponent":"Microsoft-Windows-WindowsUpdateClient","evtMessage":"Installation Failure: Windows failed. Error 0x80070490"\}. This information can be used for third-party integration or other post-alert processing. Values in the **Additional information** field of an Event that are not in JSON key/value format are normalized to JSON key/value format when the event is processed. For example, assume that the following plain text is in the **Additional information** field “Connection instance is successful”. When the event is processed, all this plain text becomes one JSON string and might not be useful within an alert. In the resultant alert, this string is in the **Additional information** field in JSON key/value format, containing the data: \{“additional\_content”: “Connection instance is successful"\}.

</td></tr><tr><td>

processing\_notes\[Processing Notes\]

</td><td>

Display of the events processing log.

</td></tr></tbody>
</table>