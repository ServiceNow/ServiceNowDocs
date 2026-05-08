---
title: Event - Global
description: The Event API provides methods that enable the setting and getting of values within an event.Instantiates an Event constructor.Returns the current value of the passed in event management field.Replaces the existing additional\_info field in the associated event with the passed in JSON string.Sets the specified field in the associated event.Sets the description field of the associated event to the passed in value.Sets the time\_of\_event field in the associated event to the passed in UTC time value.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# Event- Global

The Event API provides methods that enable the setting and getting of values within an event.

These events are sent from a MID Server to a ServiceNow instance. Before you are able to successfully send events, the connection between the MID Server and the ServiceNow instance must be defined.

Use the Event API to add/update fields within an event. Use the SNEventSenderProvider API to instantiate an event sender object. Then use the IEventSender API to send the event to a ServiceNow instance.

You must activate the Event Management \(com.glideapp.itom.snac\) plugin before attempting to access this API. The Event Management plugin requires a separate subscription and must be activated. This plugin includes demo data and activates related plugins if they are not already active.

For additional information on event management, see Event Management.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Event - Event\(\)

Instantiates an Event constructor.

|Name|Type|Description|
|----|----|-----------|
|None| | |

```
var event = new Event();
var esource = event.getField("source");
var eseverity = event.getField("severity");       

```

## Event - getField\(String field\)

Returns the current value of the passed in event management field.

|Name|Type|Description|
|----|----|-----------|
|field|String|Name of the event management field value to return.|

|Type|Description|
|----|-----------|
|String|Value of the requested event management field.|

```
var event = new Event();
var eventSource = event.getField("source");
var eventSeverity = event.getField("severity");       

```

## Event - setAdditionalInfo\(String additionalInfo\)

Replaces the existing **additional\_info** field in the associated event with the passed in JSON string.

**Note:** You can use the [setField\(\)](EventAPI.md#) method to update a specific field within the **additional\_info** field.

<table id="table_pc2_dbh_kkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

additionalInfo

</td><td>

String

</td><td>

JSON String \(key/value pairs\) to save in the **additional\_info** field.**Note:** This parameter replaces the existing information. It does not update the existing fields.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
event.setAdditionalInfo("{\"evtComponent\":\"Microsoft-Windows- WindowsUpdateClient\",\"evtMessage\":\"Installation Failure: Windows failed. Error 0x80070490\"}");
```

## Event - setField\(String key, String value\)

Sets the specified field in the associated event.

If the passed in **key** matches a predefined event field, the method updates the corresponding event field. Otherwise, the method adds the **key** parameter to the **additional\_info** section of the event before applying the passed in **value**.

The following are the predefined event fields that you can modify using this method:

<table id="table_ddd_32g_pkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

additional\_info

</td><td>

Key-value pair to add to the **additional\_info** field of the associated event. If the passed in key already exists, its value is overwritten.Maximum length: 4,000 characters

 Associated UI field: Additional information

</td></tr><tr><td>

ci\_identifier

</td><td>

JSON string that uniquely identifies a configuration item. For example, `{"name":"SAP ORA01","type":"Oracle"}`. Maximum length: 1,000 characters

</td></tr><tr><td>

cmdb\_ci

</td><td>

Sys\_id of the Configuration Item \[cmdb\_ci\] record to bind the event to.Default: Null

</td></tr><tr><td>

description

</td><td>

Free-form description of the event.Maximum length: 4,000 characters

 Associated UI field: Description

 Default: Null

</td></tr><tr><td>

event\_class

</td><td>

Enterprise Message Service \(EMS\) that generated the event. For example, "Solarwinds" or "SCOM".Maximum length: 100

 Associated UI field: Source instance

 Default: Null

</td></tr><tr><td>

message\_key

</td><td>

Unique event identifier. To override an existing event severity, use the same **message\_key** value.Maximum length: 1024 characters

 Associated UI field: Message key

 Default: Combination of **source**, **node**, **type**, **resource**, and **metric name**.

</td></tr><tr><td>

resolution\_state

</td><td>

Event resolution state.Valid values:

-   New: Resolution state for the corresponding event is open.
-   Closing: Resolution state for corresponding event is closing/closed.

 Associated UI field: Resolution state

 Default: New

</td></tr><tr><td>

resource

</td><td>

Node resource to associate with the event. For example, "Disk C:", "CPI-1", or the name of a process or service.Maximum length: 100 characters

 Associated UI field: Resource

</td></tr><tr><td>

severity

</td><td>

Event severity.Valid values:

-   0: Clear - No action is required. An alert is not created from this event. Existing alerts are closed.
-   1: Ok - An alert is created. The resource is still functional.
-   2: Warning - Attention is required, even though the resource is still functional.
-   3: Minor - Partial, non-critical loss of functionality or performance degradation occurred.
-   4: Major - Major functionality is severely impaired or performance has degraded.
-   5: Critical - Immediate action is required. The resource is either not functional or critical problems are imminent.

 Associated UI field: Severity

 Default: Null

</td></tr><tr><td>

source

</td><td>

Instance of the EMS that triggered the event. Typically the connector instance name.Maximum length: 200 characters

 Associated UI field: Source

 Default: Null

</td></tr><tr><td>

time\_of\_event

</td><td>

UTC time that the event occurred in the source system.Format: "yyyy-MM-dd HH:mm:ss"

 Maximum length: 40 characters

 Associated UI field: Time of event

 Default: Current date/time

</td></tr><tr><td>

type

</td><td>

Metric type to which the event is related, such as Disk or CPU. This value is used to identify an event record from which alerts are created.Maximum length: 100 characters

 Associated UI field: Type

 Default: Null

</td></tr></tbody>
</table>**Note:** You can also use the [setText\(\)](EventAPI.md#) method to update the **description** field and the [setTimeOfEvent\(\)](EventAPI.md#) method to update the event time.

For additional information on events, see Event Management.

<table id="table_ijd_4ck_jkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Name of the key to add or update in the event. For additional information on the predefined event fields, see Event field format for event collection.

</td></tr><tr><td>

value

</td><td>

String

</td><td>

Information to store in the associated event field.**Note:** The **value** string is trimmed before it is stored, whereby multiple spaces are replaced with a single space.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var event = new Event();
event.setField("source","SAP Solman");
event.setField("severity","3");
event.setField("time_of_event", "2019-18-05 13:12:05");
event.setField("type", "SAP object");
event.setField("user", "admin"); // parameter will be added to additional_info section       

```

## Event - setText\(String text\)

Sets the **description** field of the associated event to the passed in value.

**Note:** You can also use the [Event - setField\(String key, String value\)](EventAPI.md#) method to set the **text** field in the current event. Unlike the setField\(\) method, this method does not trim the passed in text.

<table id="table_r2j_mgh_kkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

text

</td><td>

String

</td><td>

Text to store in the **description** field of the associated event.Max length: 4000 characters

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var event = new Event();
event.setText("SAP Solman");       

```

## Event - setTimeOfEvent\(String timeOfEvent\)

Sets the **time\_of\_event** field in the associated event to the passed in UTC time value.

**Note:** You can also use the [Event - setField\(String key, String value\)](EventAPI.md#) method to set the **time\_of\_event** field.

<table id="table_m43_kwg_kkb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

timeOfEvent

</td><td>

String

</td><td>

UTC time value to set in the **time\_of\_event** field.Format: "yyyy-MM-dd HH:mm:ss"

 Max length: 40 characters

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

```
var event = new Event();
event.setTimeOfEvent("2019-18-05 13:12:05");
```

