---
title: Event Notification Management Open API
description: The Event Notification Management Open API provides an endpoint to create, update, and delete events from the Events \[em\_event\] table.Places the payload of the associated request in the NowMQ queue. This queue is then processed in the background to create, update, and delete events within the Events \[em\_event\] table.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Event Notification Management Open API

The Event Notification Management Open API provides an endpoint to create, update, and delete events from the Events \[em\_event\] table.

The Event Notification Management Open API \(sn\_ind\_tmf688\) is a ServiceNow implementation of the TM Forum Open API specification. This API is based on [TMF688 Event Management API User Guide v4.0.0](https://www.tmforum.org/resources/standard/tmf688-event-management-api-user-guide-v4-0-0/). You can locate additional alarm information in the [TMF642 Alarm Management API User Guide](https://projects.tmforum.org/wiki/download/attachments/134776981/TMF642_Alarm_Management_API_User_Guide_v4.0.0.pdf?api=v2).

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. For more information, see the [Event Notification Management Open API Developer Guide](../../guides/telecom/concept/event-mgmt-notif_dev-guide.md#).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Event Notification Management Open API – POST instance\_name/scope\_id/GUID

Places the payload of the associated request in the NowMQ queue. This queue is then processed in the background to create, update, and delete events within the Events \[em\_event\] table.

This endpoint is different than other endpoints in the ServiceNow platform. Instead of having an endpoint for each specific task, such as create, update, and delete, there's only a single endpoint for all functionality. The parameter **eventType** in the call payload determines the task to perform based on its passed value of `AlarmCreateEvent`, `AlarmUpdateEvent`, or `AlarmDeleteEvent`.

The format of the REST call is also different than standard REST implementations. Each external system that will use this API, such as Kafka, database monitors, or other applications, must first register with the ServiceNow platform. They must also have their own webhook in place that uses the information provided during registration to generate the signature required to call this endpoint, including the `instance_name`, application `scope_id`, and unique `GUID`. The `GUID` identifies the external network system that the request came from.

The payload that you pass for this endpoint must correlate with the payload that is defined in the `TMFAlarmAPIConstants` script include for the corresponding **eventType** parameter value. Any parameters that are passed in the payload and not defined in the schema are ignored by the endpoint.

-   `AlarmCreateEvent`: `ALARM_CREATE_EVENT_SCHEMA`
-   `AlarmUpdateEvent`: `ALARM_CHANGE_EVENT_SCHEMA`
-   `AlarmDeleteEvent`: `ALARM_DELETE_EVENT_SCHEMA`

### URL format

Default URL: `<instance_name>/<scope_id>/<GUID>`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

event

</td><td>

Details about the event that occurred.Data type: Object

```
"event": {
    "alarm": {Object}
}
```

</td></tr><tr><td>

event.alarm

</td><td>

Required when **eventType** is `AlarmCreateEvent`. Details about the associated alarm.

Data type: Object

```
"alarm": {
  "affectedService": [Array],
  "alarmedObject": {Object},
  "alarmType": "String",
  "crossedThresholdInformation": {Object},
  "externalAlarmId": "String",
  "href": "String",
  "id": "String",
  "perceivedSeverity": "String",
  "probableCause": "String",
  "sourceSystemId": "String",
  "specificProblem": "String",
}
```

</td></tr><tr><td>

event.alarm.affectedService

</td><td>

List of objects identifying one or more services affected by the alarm.Data type: Array

```
"affectedService":[
  {
    "href": "String",
    "id": "String"
  },
]
```

</td></tr><tr><td>

event.alarm.affectedService.href

</td><td>

URL reference providing details of the affected service.Data type: String

</td></tr><tr><td>

event.alarm.affectedService.id

</td><td>

Identifier of the service affected by the alarm. This value maps to the affected configuration item \(CI\) on the alert.

Data type: String

</td></tr><tr><td>

event.alarm.alarmedObject

</td><td>

Required when creating an event. Details of the alarm object.

Data type: Object

```
"alarmedObject":
{
  "href": "String",
  "id": "String"
}
```

</td></tr><tr><td>

event.alarm.alarmedObject.href

</td><td>

Required when creating an event. URL reference to get the details of the alarm object.

Data type: String

</td></tr><tr><td>

event.alarm.alarmedObject.id

</td><td>

Required when **eventType** is `AlarmCreateEvent`. Unique identifier of the alarm object. This value maps to a CI in the system.

Data type: String

</td></tr><tr><td>

event.alarm.alarmType

</td><td>

Required when **eventType** is `AlarmCreateEvent`. Type of alarm. Used to categorize the alarm.

For example: "QualityOfServiceAlarm"

Data type: String

</td></tr><tr><td>

event.alarm.crossedThresholdInfomation

</td><td>

Details about the crossed threshold.Data type: Object

```
"crossedThresholdInformation":
{
  "thresholdId": "String"
}
```

</td></tr><tr><td>

event.alarm.crossedThresholdInfomation.thresholdId

</td><td>

Unique identifier of the threshold that caused the alarm.

Data type: String

</td></tr><tr><td>

event.alarm.externalAlarmId

</td><td>

Required when **eventType** is `AlarmCreateEvent`. Required when **eventType** is `AlarmDeleteEvent` or `AlarmChangeEvent` if the **Id** parameter is not specified. Unique identifier for the alarm from the source system posting the alarm.

Data type: String

</td></tr><tr><td>

event.alarm.href

</td><td>

URL reference to the alarm.For example: "http://api/alarm/ROUTER\_IF@Cisco-0000-0-0-0-0-00-00-0-- Xz0/00@00"

Data type: String

</td></tr><tr><td>

event.alarm.id

</td><td>

Required when **eventType** is `AlarmDeleteEvent` or `AlarmChangeEvent` if **externalAlarmId** is not specified. Unique identifier of the alarm. Specified by the alarm owning system.

For example: "8675399"

Data type: String

</td></tr><tr><td>

event.alarm.perceivedSeverity

</td><td>

Required when **eventType** is `AlarmCreateEvent`. Possible severities associated with the alarm. The values are consistent with ITU-T Recommendation X.733. After an alarm has been cleared, its perceived severity is set to 'CLEAR' and can no longer be set.

Possible values:

-   CLEAR
-   CRITICAL
-   MAJOR
-   MINOR
-   WARNING

Data type: String

</td></tr><tr><td>

event.alarm.probableCause

</td><td>

Required when **eventType** is `AlarmCreateEvent`.Most likely situation to trigger the alarm. Use with **alarmType** to qualify the alarm.

The possible values are consistent with ITU-T Recommendation X.733 or 3GPP TS 32.111-2 Annex B.

For example: "Threshold crossed"

Data type: String

</td></tr><tr><td>

event.alarm.sourceSystemId

</td><td>

Required when **eventType** is `AlarmCreateEvent`. Unique identifier of the source system of the alarm.

For example: "SOURCE\_SYSTEM\_vManage\_00000\_000\_00"

Data type: String

</td></tr><tr><td>

event.alarm.specificProblem

</td><td>

Specific problem that triggers the alarm. Use with **probableCause** to qualify the alarm.For example: "Inbound Traffic threshold crossed"

Data type: String

</td></tr><tr><td>

eventType

</td><td>

Required. Type of event to process.Valid values:

-   AlarmChangeNotification
-   AlarmCreateNotification
-   AlarmDeleteNotification

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Returned for every call regardless of the actual processing status of the call. Only indicates that the endpoint received the request.|

### Response body parameters

|Name|Description|
|----|-----------|
|None|This endpoint is asynchronous and therefore doesn't return any response data.|

### cURL request

The following shows the possible payload for a create alarm event. This example reflects the parameters that are in the default implementation \(`AlarmCreateEventSchema`\).

```

--data "{
  "eventType": "AlarmCreateNotification",
  "event": {
    "alarm": {
      "id": "",
      "externalAlarmId": "ext123456",
      "alarmType": "QualityOfServiceAlarm",
      "perceivedSeverity": "MINOR",
      "alarmedObject": {
        "id": "vManage_000000",
        "href": " http://api/alarmedobject/000000"
      },
      "probableCause": "Threshold crossed",
      "sourceSystemId": "SOURCE_SYSTEM_vManage_00000_000_00",
      "href": "http://api/alarm/ROUTER_IF@Cisco-0000-0-0-0-0-00-00-0-- Xz0/00@00",
      "specificProblem": "Inbound Traffic threshold crossed",
      "crossedThresholdInformation": {
        "thresholdId": "12fasdfasdfasd"
      },
      "affectedService": [
        {
          "id": "SD WAN Enterprise Solutions",
          "href": "http://api/service/vlan_dot0_dot0"
        }
      ]
    }
  }
}
```

No response returned.

### cURL request

The following shows the possible payload for a change alarm event. This example reflects the parameters that are in the default implementation \(`AlarmChangeEventSchema`\).

```

--data "{
  "eventType": "AlarmChangeEventSchema",
  "event": {
    "alarm": {
      "id": "",
      "externalAlarmId": "ext123456",
      "perceivedSeverity": "MAJOR",
      "probableCause": "Threshold crossed",
      "crossedThresholdInformation": {
        "thresholdId": "12fasdfasdfasd"
      },
      "affectedService": [
        {
          "id": "SD WAN Enterprise Solutions",
          "href": "http://api/service/vlan_dot0_dot0"
        }
      ]
    }
  }
}

```

No response returned.

### cURL request

The following shows the possible payload for a delete \(clear\) alarm event. This example reflects the parameters that are in the default implementation \(`AlarmDeleteEventSchema`\).

```

--data "{
  "eventType": "AlarmDeleteEventSchema",
  "event": {
    "alarm": {
      "id": "",
      "externalAlarmId": "ext123456",
      "perceivedSeverity": "MAJOR",
      "probableCause": "Threshold crossed",
      "crossedThresholdInformation": {
        "thresholdId": "12fasdfasdfasd"
      }
    }
  }
}
```

No response returned.

