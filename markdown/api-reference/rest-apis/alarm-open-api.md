---
title: Alarm Management Open API
description: The Alarm Management Open API provides endpoints to create, update, and retrieve data from the Events \[em\_event\] and Alert \[em\_alert\] tables.Retrieves a list of all alarm records from the Events \[em\_event\] and Alert \[em\_alert\] tables.Retrieves a specified alarm record from the Events \[em\_event\] or Alert \[em\_alert\] table.Updates a specified alarm and any associated alert.Creates an alarm record in the Events \[em\_event\] table.Clears a specified alarm and closes any associated alert.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 27
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Alarm Management Open API

The Alarm Management Open API provides endpoints to create, update, and retrieve data from the Events \[em\_event\] and Alert \[em\_alert\] tables.

The telecommunications Alarm Management Open API \(sn\_ind\_tmf642\) is a ServiceNow® implementation of the TM Forum Open API specification. This API is based on [TMF642 Alarm Management API REST Specification Release 20](https://www.tmforum.org/resources/specification/tmf642-alarm-management-api-user-guide-v4-0/), April 2020.

The calling user must have to access the `sn_ind_tmf642.alarm_mgmt_integration` endpoint.

This API is provided within the `sn_ind_tmf642` namespace.

The TM Forum Open API specification requires a synchronous response for every inbound request it receives. Apply correlation and de-duplication in the source operational support system \(OSS\) before forwarding payloads to the system.

This API can be extended to make customizations around required parameters, request body validation, additional REST operations, and field mappings. For more information, see the [Alarm Management Open API Developer Guide](../../guides/telecom/concept/alarm-mgmt_dev-guide.md#).

The Alarm Management Open API is conformance certified by TM Forum.

![TMF conformance logo](../image/tmf-conformance.png)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Alarm Management Open API – GET /sn\_ind\_tmf642/alarm\_mgmt/alarm

Retrieves a list of all alarm records from the Events \[em\_event\] and Alert \[em\_alert\] tables.

### URL format

Default URL: `/api/sn_ind_tmf642/alarm_mgmt/alarm`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

<table id="table_qcn_fkm_qtb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alarmRaisedTime

</td><td>

Date the alarm was raised. Only alarms with a date matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   alarmedObject
-   alarmRaisedTime
-   alarmType
-   crossedThresholdInformation
-   externalAlarmId
-   id
-   perceivedSeverity
-   probableCause
-   source
-   sourceSystemId
-   state
-   type

Default: All fields

Data type: String

</td></tr><tr><td>

id

</td><td>

Alarm ID. Only alarms with an ID matching the value of this parameter are returned in the response.Data type: String

Table: In the Message key field in the Events \[em\_event\] table.

</td></tr><tr><td>

limit

</td><td>

Maximum number of records to return. For requests that exceed this number of records, use the **offset** parameter to paginate record retrieval. Default: 1000

Maximum: 2000

Data type: Number

</td></tr><tr><td>

offset

</td><td>

Starting index at which to begin retrieving records. Use this value to paginate record retrieval. This functionality enables the retrieval of all records, regardless of the number of records, in small manageable chunks.Data type: Number

Default: 0

</td></tr><tr><td>

probableCause

</td><td>

Probable cause of the alarm. Only alarms with a probable cause matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

state

</td><td>

Alarm state. Only alarms with a state matching the value of this parameter are returned in the response.Data type: String

</td></tr><tr><td>

sourceSystemId

</td><td>

Source system ID of the alarm. Only alarms with a source system ID matching the value of this parameter are returned in the response.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|None| |

<table id="table_c2r_4gm_lsb" class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr id="content-range-row"><td>

Content-Range

</td><td>

Range of content returned in a paginated call. For example, if `offset=2` and `limit=3`, the value of the **Content-Range** header is `items 3-5`.

</td></tr><tr id="content-type-row"><td>

Content-Type

</td><td>

Data format of the response body. Only supports **application/json**.

</td></tr><tr id="links-pagination-row"><td>

Link

</td><td>

Contains the following links to navigate through query results.-   first
-   last
-   next
-   previous

</td></tr><tr id="x-total-count-row"><td id="x-total-count">

X-Total-Count

</td><td>

For paginated queries, this header specifies the total number of records available on the server.

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_qbg_4cm_lsb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="tmf-get-status-200-entry">

Request successfully processed. Full resource returned in response \(no pagination\).

</td></tr><tr><td>

206

</td><td id="tmf-get-status-206-entry">

Partial resource returned in response \(with pagination\).

</td></tr><tr><td>

400

</td><td id="tmf-get-status-400-entry">

Bad request. Possible reasons:

-   Invalid path parameter
-   Invalid URI

</td></tr><tr><td>

404

</td><td id="tmf-get-status-404-entry">

Record not found. No records matching the query parameters are found in the table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_zjc_fbg_qtb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

affectedService

</td><td id="alm-mgmt-affectedService-entry">

List of one or more services affected by the alarm.Data type: Array of Objects

```
"affectedService":[
  {
    "href": "String",
    "id": "String"
  },
]
```

</td></tr><tr><td>

affectedService.href

</td><td id="alm-mgmt-affectedServiceHREF-entry">

URL reference that provides details of the affected service.Data type: String

</td></tr><tr><td>

affectedService.id

</td><td>

Identifier of the service affected by the alarm. This value maps to the affected configuration item \(CI\) on the alert. Data type: String

</td></tr><tr><td>

alarmDetails

</td><td>

Additional details about the alarm.Data type: String

</td></tr><tr><td>

alarmedObject

</td><td>

Details of the alarm object. ```
"alarmedObject":
{
  "href": "String",
  "id": "String"
}
```

 Data type: Object

</td></tr><tr><td>

alarmedObject.id

</td><td>

Unique identifier of the alarm object. This value maps to a CI in the system. Data type: String

</td></tr><tr><td>

alarmedObject.href

</td><td id="alm-mgmt-create-alarmobj-href-entry">

URL reference to get the details of the alarm object.

Data type: String

</td></tr><tr><td>

alarmedObjectType

</td><td>

Type or class of object associated with the event.Data type: String

</td></tr><tr><td>

alarmRaisedTime

</td><td>

Date and time at which the alarm occurs at its source.Data type: String

</td></tr><tr><td>

alarmReportingTime

</td><td>

Date and time at which the OSS reports its alarm.This value might differ from the **alarmRaisedTime** value. For example, if an element management system \(EMS\) maintains the alarm list:

-   The **alarmRaisedTime** is the time of alarm detection by the network element \(NE\).
-   The **alarmReportingTime** is the alarm report time of storage in the EMS alarm list.

Data type: String

</td></tr><tr><td>

alarmType

</td><td>

Alarm category. Data type: String

</td></tr><tr><td>

crossedThresholdInformation

</td><td>

Details about the crossed threshold.Data type: Object

```
"crossedThresholdInformation":
{
  "direction": "String",
  "granularity": "String",
  "indicatorName": "String",
  "indicatorUnit": "String",
  "observedValue": "String",
  "thresholdCrossingDescription": "String",
  "thresholdId": "String",
  "thresholdRef": "String"
}
```

</td></tr><tr><td>

crossedThresholdInformation.direction

</td><td>

Threshold crossing direction.Valid values:

-   DOWN
-   UP

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.granularity

</td><td>

Granularity at which the indicator is evaluated for threshold crossing. For example, `5MINUTES`.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorName

</td><td>

Name of the indicator that crosses the alarm threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorUnit

</td><td>

Measurement unit of the indicator corresponding to the crossed threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.observedValue

</td><td>

Number identifying the indicator crossing the threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdCrossingDescription

</td><td>

More threshold details of the threshold crossing alarm.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdId

</td><td>

Unique identifier of the threshold that caused the alarm. Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdRef

</td><td>

URL of the threshold object.Data type: String

</td></tr><tr><td>

externalAlarmId

</td><td>

Unique identifier for the alarm from the source system posting the alarm. Data type: String

</td></tr><tr><td>

href

</td><td>

URL of the resource.Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier for the system to identify and process the alarm payload as an event. Data type: String

</td></tr><tr><td>

perceivedSeverity

</td><td>

Alarm severity. Valid values:

-   CLEAR
-   CRITICAL
-   MAJOR
-   MINOR
-   WARNING

 Data type: String

</td></tr><tr><td>

plannedOutageIndication

</td><td>

Indicates that the managed object for this alarm is in a planned outage state. For example, planned maintenance or out-of-service.Data type: String

</td></tr><tr><td>

probableCause

</td><td>

Most likely situation to trigger the alarm. Use with **alarmType** to qualify the alarm. Data type: String

</td></tr><tr><td>

proposedRepairActions

</td><td>

If available to the system, provides a repair action to resolve the issue that triggers the alarm.Data type: String

</td></tr><tr><td>

serviceAffecting

</td><td>

Flag that indicates whether the alarm affects service.Valid values:

-   true: Alarm affects service performance or availability.
-   false: Alarm doesn't affect service.

Default: false

Data type: Boolean

</td></tr><tr><td>

sourceSystemId

</td><td>

Instance ID of the source alarm. Data type: String

</td></tr><tr><td>

specificProblem

</td><td id="alm-mgmt-specificProb-entry">

Specific problem that triggers the alarm. Use with the **probableCause** tparameter o qualify the alarm.Data type: String

</td></tr><tr><td>

state

</td><td>

Alarm state.Valid values:

-   Error
-   Ignored
-   Ready
-   Processed

If an invalid value is provided, the state is set to `Ready`.

If the state is `Ready`, an alert is created in the Alert \[em\_alert\] table and the state then becomes `Processed`.

If the state is `Processed`, `Ignored`, or `Error` no alert is created.

Default value: Ready

Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves all alarms.

```
curl "https://instance.servicenow.com/api/sn_ind_tmf642/alarm_mgmt/alarm" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
[
   {
      "externalAlarmId": "2212331",
      "alarmType": "QualityOfServiceAlarm23",
      "perceivedSeverity": "MAJOR",
      "probableCause": "ProbB",
      "sourceSystemId": "checkSB",
      "alarmedObject": {
         "id": "vManage_000000",
         "href": " http://api/alarmedobject/000000"
      },
      "crossedThresholdInformation": {
         "direction": "111",
         "granularity": "1234",
         "indicatorName": "sdfgds",
         "indicatorUnit": "asdfdsaf",
         "observedValue": "adsfds",
         "thresholdId": "12fasdfasdfasd",
         "thresholdCrossingDescription": "S23rtring",
         "thresholdRef": "asdfasf"
      },
      "type": "QualityOfServiceAlarm",
      "ackState": "acknowledged",
      "specificProblem": "Inbound Traffic threshold crossed",
      "alarmedObjectType": "ROUTER",
      "alarmDetails": "Software Failure on SD-WAN Controller vManage_000000",
      "state": "processed",
      "alarmChangedTime": "2017-08-15T07:04:15.666Z",
      "proposedRepairActions": "Switch in standby equipment",
      "alarmReportingTime": "2017-06-15T07:04:15.666Z",
      "alarmRaisedTime": "2020-09-15T14:04:15.000Z",
      "plannedOutageIndication": "IN_SERVICE",
      "serviceAffecting": true,
      "affectedService": [
         {
            "id": "SD WAN Enterprise Solutions",
            "href": "http://api/service/vlan_dot0_dot0"
         },
         {
            "id": "Santa Clara SD WAN Application Service",
            "href": "http://api/service/vlan_dot0_dot0"
         }
      ],
      "source": "Alarm Management Open API",
      "href": "/api/sn_ind_tmf642/alarm_mgmt/alarm/001a0ca629078d10f87759e2f69e4c64_2212331",
      "id": "001a0ca629078d10f87759e2f69e4c64_2212331"
   },
   {
      "externalAlarmId": "2212331",
      "alarmType": "QualityOfServiceAlarm23",
      "perceivedSeverity": "MAJOR",
      "probableCause": "ProbB",
      "sourceSystemId": "checkSB",
      "alarmedObject": {
         "id": "vManage_000000",
         "href": " http://api/alarmedobject/000000"
      },
      "crossedThresholdInformation": {
         "direction": "111",
         "granularity": "1234",
         "indicatorName": "sdfgds",
         "indicatorUnit": "asdfdsaf",
         "observedValue": "adsfds",
         "thresholdId": "12fasdfasdfasd",
         "thresholdCrossingDescription": "S23rtring",
         "thresholdRef": "asdfasf"
      },
      "type": "QualityOfServiceAlarm",
      "ackState": "acknowledged",
      "specificProblem": "Inbound Traffic threshold crossed",
      "alarmedObjectType": "ROUTER",
      "alarmDetails": "Software Failure on SD-WAN Controller vManage_000000",
      "state": "processed",
      "alarmChangedTime": "2017-08-15T07:04:15.666Z",
      "proposedRepairActions": "Switch in standby equipment",
      "alarmReportingTime": "2017-06-15T07:04:15.666Z",
      "alarmRaisedTime": "2020-09-15T14:04:15.000Z",
      "plannedOutageIndication": "IN_SERVICE",
      "serviceAffecting": true,
      "affectedService": [
         {
            "id": "SD WAN Enterprise Solutions",
            "href": "http://api/service/vlan_dot0_dot0"
         },
         {
            "id": "Santa Clara SD WAN Application Service",
            "href": "http://api/service/vlan_dot0_dot0"
         }
      ],
      "source": "Alarm Management Open API",
      "href": "/api/sn_ind_tmf642/alarm_mgmt/alarm/001c84aa29078d10f87759e2f69e4cfa_2212331",
      "id": "001c84aa29078d10f87759e2f69e4cfa_2212331"
   }
]
```

## Alarm Management Open API – GET /sn\_ind\_tmf642/alarm\_mgmt/alarm/\{id\}

Retrieves a specified alarm record from the Events \[em\_event\] or Alert \[em\_alert\] table.

### URL format

Default URL: `/api/sn_ind_tmf642/alarm_mgmt/alarm/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Unique identifier of the record to retrieve.Data type: String

Table: In the Message key field of the Events \[em\_event\] table.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fields

</td><td>

List of fields to return in the response. Invalid fields are ignored.Valid fields:

-   alarmedObject
-   alarmRaisedTime
-   alarmType
-   crossedThresholdInformation
-   externalAlarmId
-   id
-   perceivedSeverity
-   probableCause
-   source
-   sourceSystemId
-   state
-   type

Default value: All fields

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td id="entry-200-status-code">

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad Request. A bad request type or malformed request was detected for one or more of the following reasons.-   Invalid path parameter.
-   Invalid URI.

</td></tr><tr><td>

404

</td><td>

Record not found. A record associated with the specified ID is not found in the Event \[em\_event\] or Alert \[em\_alert\] table.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table id="table_gtd_dbg_qtb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

affectedService

</td><td id="alm-mgmt-affectedService-entry">

List of one or more services affected by the alarm.Data type: Array of Objects

```
"affectedService":[
  {
    "href": "String",
    "id": "String"
  },
]
```

</td></tr><tr><td>

affectedService.href

</td><td id="alm-mgmt-affectedServiceHREF-entry">

URL reference that provides details of the affected service.Data type: String

</td></tr><tr><td>

affectedService.id

</td><td>

Identifier of the service affected by the alarm. This value maps to the affected configuration item \(CI\) on the alert. Data type: String

</td></tr><tr><td>

alarmDetails

</td><td>

Additional details about the alarm.Data type: String

</td></tr><tr><td>

alarmedObject

</td><td>

Details of the alarm object. Data type: Object

```
"alarmedObject":
{
  "href": "String",
  "id": "String"
}
```

</td></tr><tr><td>

alarmedObject.id

</td><td>

Unique identifier of the alarm object. This value maps to a CI in the system. Data type: String

</td></tr><tr><td>

alarmedObject.href

</td><td id="alm-mgmt-create-alarmobj-href-entry">

URL reference to get the details of the alarm object.

Data type: String

</td></tr><tr><td>

alarmedObjectType

</td><td>

Type or class of object associated with the event.Data type: String

</td></tr><tr><td>

alarmRaisedTime

</td><td>

Date and time at which the alarm occurs at its source.Data type: String

</td></tr><tr><td>

alarmReportingTime

</td><td>

Date and time at which the OSS reports its alarm.This value might differ from the **alarmRaisedTime** value. For example, if an element management system \(EMS\) maintains the alarm list:

-   The **alarmRaisedTime** is the time of alarm detection by the network element \(NE\).
-   The **alarmReportingTime** is the alarm report time of storage in the EMS alarm list.

Data type: String

</td></tr><tr><td>

alarmType

</td><td>

Alarm category. Data type: String

</td></tr><tr><td>

crossedThresholdInformation

</td><td>

Details about the crossed threshold.Data type: Object

```
"crossedThresholdInformation":
{
  "direction": "String",
  "granularity": "String",
  "indicatorName": "String",
  "indicatorUnit": "String",
  "observedValue": "String",
  "thresholdCrossingDescription": "String",
  "thresholdId": "String",
  "thresholdRef": "String"
}
```

</td></tr><tr><td>

crossedThresholdInformation.direction

</td><td>

Threshold crossing direction.Valid values:

-   DOWN
-   UP

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.granularity

</td><td>

Granularity at which the indicator is evaluated for threshold crossing. For example, `5MINUTES`.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorName

</td><td>

Name of the indicator that crosses the alarm threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorUnit

</td><td>

Measurement unit of the indicator corresponding to the crossed threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.observedValue

</td><td>

Number identifying the indicator crossing the threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdCrossingDescription

</td><td>

More threshold details of the threshold crossing alarm.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdId

</td><td>

Unique identifier of the threshold that caused the alarm. Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdRef

</td><td>

URL of the threshold object.Data type: String

</td></tr><tr><td>

externalAlarmId

</td><td>

Unique identifier for the alarm from the source system posting the alarm. Data type: String

</td></tr><tr><td>

href

</td><td>

URL of the resource.Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier for the system to identify and process the alarm payload as an event. Data type: String

</td></tr><tr><td>

perceivedSeverity

</td><td>

Alarm severity. Valid values:

-   CLEAR
-   CRITICAL
-   MAJOR
-   MINOR
-   WARNING

 Data type: String

</td></tr><tr><td>

plannedOutageIndication

</td><td>

Indicates that the managed object for this alarm is in a planned outage state. For example, planned maintenance or out-of-service.Data type: String

</td></tr><tr><td>

probableCause

</td><td>

Most likely situation to trigger the alarm. Use with **alarmType** to qualify the alarm. Data type: String

</td></tr><tr><td>

proposedRepairActions

</td><td>

If available to the system, provides a repair action to resolve the issue that triggers the alarm.Data type: String

</td></tr><tr><td>

serviceAffecting

</td><td>

Flag that indicates whether the alarm affects service.Valid values:

-   true: Alarm affects service performance or availability.
-   false: Alarm doesn't affect service.

Default: false

Data type: Boolean

</td></tr><tr><td>

sourceSystemId

</td><td>

Instance ID of the source alarm. Data type: String

</td></tr><tr><td>

specificProblem

</td><td id="alm-mgmt-specificProb-entry">

Specific problem that triggers the alarm. Use with the **probableCause** tparameter o qualify the alarm.Data type: String

</td></tr><tr><td>

state

</td><td>

Alarm state.Valid values:

-   Error
-   Ignored
-   Ready
-   Processed

If an invalid value is provided, the state is set to `Ready`.

If the state is `Ready`, an alert is created in the Alert \[em\_alert\] table and the state then becomes `Processed`.

If the state is `Processed`, `Ignored`, or `Error` no alert is created.

Default value: Ready

Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves an alarm.

```
curl "https://instance.servicenow.com/api/sn_ind_tmf642/alarm_mgmt/alarm/001a0ca629078d10f87759e2f69e4c64_2212331" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'


```

Response body.

```
{
   "externalAlarmId": "2212331",
   "alarmType": "QualityOfServiceAlarm23",
   "perceivedSeverity": "MAJOR",
   "probableCause": "ProbB",
   "sourceSystemId": "checkSB",
   "alarmedObject": {
      "id": "vManage_000000",
      "href": " http://api/alarmedobject/000000"
   },
   "crossedThresholdInformation": {
      "direction": "111",
      "granularity": "1234",
      "indicatorName": "ind_name",
      "indicatorUnit": "ind_unit",
      "observedValue": "232",
      "thresholdId": "200",
      "thresholdCrossingDescription": "sample_description",
      "thresholdRef": "sample_ref"
   },
   "type": "QualityOfServiceAlarm",
   "ackState": "acknowledged",
   "specificProblem": "Inbound Traffic threshold crossed",
   "alarmedObjectType": "ROUTER",
   "alarmDetails": "Software Failure on SD-WAN Controller vManage_000000",
   "state": "processed",
   "alarmChangedTime": "2017-08-15T07:04:15.666Z",
   "proposedRepairActions": "Switch in standby equipment",
   "alarmReportingTime": "2017-06-15T07:04:15.666Z",
   "alarmRaisedTime": "2020-09-15T14:04:15.000Z",
   "plannedOutageIndication": "IN_SERVICE",
   "serviceAffecting": true,
   "affectedService": [
      {
         "id": "SD WAN Enterprise Solutions",
         "href": "http://api/service/vlan_dot0_dot0"
      },
      {
         "id": "Santa Clara SD WAN Application Service",
         "href": "http://api/service/vlan_dot0_dot0"
      }
   ],
   "source": "Alarm Management Open API",
   "href": "/api/sn_ind_tmf642/alarm_mgmt/alarm/001a0ca629078d10f87759e2f69e4c64_2212331",
   "id": "001a0ca629078d10f87759e2f69e4c64_2212331"
}
```

## Alarm Management Open API – PATCH /sn\_ind\_tmf642/alarm\_mgmt/alarm/\{id\}

Updates a specified alarm and any associated alert.

This endpoint writes the response body to the **Additional Info** field of the event record in the Events \[em\_event\] table.

### URL format

Default URL: `/api/sn_ind_tmf642/alarm_mgmt/alarm/{id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Unique identifier of the record to update.Data type: String

Table: In the Message key field of the Events \[em\_event\] table.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_kmr_mjs_xnb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

affectedService

</td><td id="alm-mgmt-affectedService-entry">

List of one or more services affected by the alarm.Data type: Array of Objects

```
"affectedService":[
  {
    "href": "String",
    "id": "String"
  },
]
```

</td></tr><tr><td>

affectedService.href

</td><td id="alm-mgmt-affectedServiceHREF-entry">

URL reference that provides details of the affected service.Data type: String

</td></tr><tr><td>

affectedService.id

</td><td>

Required. Identifier of the service affected by the alarm. This value maps to the affected configuration item \(CI\) on the alert.

Data type: String

</td></tr><tr><td>

alarmChangedTime

</td><td>

Indicates the last date and time the alarm changed on the alarm-owning system. Any change to the alarm updates this value whether coming from the alarmed resource or triggered by a change from the client.Data type: String

</td></tr><tr><td>

alarmDetails

</td><td>

Additional details about the alarm.Data type: String

</td></tr><tr><td>

alarmEscalation

</td><td>

Flag that indicates an escalation in alarm severity.

 Valid values:

-   true: There is an escalation in alarm severity.
-   false: The alarm severity is the same or lower.

 Default: false

 Data type: Boolean

</td></tr><tr><td>

crossedThresholdInformation

</td><td>

Details about the crossed threshold.Data type: Object

```
"crossedThresholdInformation":
{
  "direction": "String",
  "granularity": "String",
  "indicatorName": "String",
  "indicatorUnit": "String",
  "observedValue": "String",
  "thresholdCrossingDescription": "String",
  "thresholdId": "String",
  "thresholdRef": "String"
}
```

</td></tr><tr><td>

crossedThresholdInformation.direction

</td><td>

Threshold crossing direction.Valid values:

-   DOWN
-   UP

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.granularity

</td><td>

Granularity at which the indicator is evaluated for threshold crossing. For example, `5MINUTES`.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorName

</td><td>

Name of the indicator that crosses the alarm threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorUnit

</td><td>

Measurement unit of the indicator corresponding to the crossed threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.observedValue

</td><td>

Number identifying the indicator crossing the threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdCrossingDescription

</td><td>

More threshold details of the threshold crossing alarm.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdId

</td><td>

Required.Unique identifier of the threshold that caused the alarm.

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdRef

</td><td>

URL of the threshold object.Data type: String

</td></tr><tr><td>

href

</td><td>

URL reference to the alarm.Data type: String

</td></tr><tr><td>

perceivedSeverity

</td><td>

Required. Alarm severity. Valid values:

-   CLEAR
-   CRITICAL
-   MAJOR
-   MINOR
-   WARNING

Data type: String

</td></tr><tr><td>

plannedOutageIndication

</td><td>

Indicates that the managed object for this alarm is in a planned outage state. For example, planned maintenance or out-of-service.Data type: String

</td></tr><tr><td>

probableCause

</td><td>

Required. Most likely situation to trigger the alarm. Use with **alarmType** to qualify the alarm.

Data type: String

</td></tr><tr><td>

proposedRepairActions

</td><td>

If available to the system, provides a repair action to resolve the issue that triggers the alarm.Data type: String

</td></tr><tr><td>

serviceAffecting

</td><td>

Flag that indicates whether the alarm affects service.Valid values:

-   true: Alarm affects service performance or availability.
-   false: Alarm doesn't affect service.

Default: false

Data type: Boolean

</td></tr><tr><td>

specificProblem

</td><td id="alm-mgmt-specificProb-entry">

Specific problem that triggers the alarm. Use with the **probableCause** tparameter o qualify the alarm.Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_ifj_lyb_ynb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad request.Possible reasons:

-   Invalid payload. Missing required alarm ID.
-   Invalid payload. Required field missing:&lt;field name&gt;.
-   Invalid payload. Missing required object.
-   Event not created, failed.
-   Unable to clear event.
-   Unable to update event.
-   The event doesn’t exist.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alarmChangedTime

</td><td>

Date and time the alarm changed in GMT on the alarm-owning system. This value updates when changes to the alarm from the alarmed resource occur or a change from a client update triggers the alarm. This value is required in the response.Data type: String

</td></tr><tr><td>

href

</td><td>

URL reference to the alarm.Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier of the alarm. Value determined by the system owning the alarm.Data type: String

</td></tr></tbody>
</table>### cURL request

In this example, the severity is reduced to MINOR.

```
curl "https://<instance>.service-now.com/api/sn_ind_tmf642/alarm_mgmt/alarm/6e116bb8db09201087b9a8394b961950_<external-alarm-id>" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
     \"href\":\"http://api/alarm/ROUTER_IF@Cisco-0000-0-0-0-0-00-00-0-- Xz0/00@00\",
     \"externalAlarmId\":\"<external-alarm-id>\",
     \"alarmType\":\"QualityOfServiceAlarm\",
     \"type\":\"QualityOfServiceAlarm\",
     \"ackState\":\"acknowledged\",
     \"perceivedSeverity\":\"MINOR\",
     \"probableCause\":\"Threshold crossed\",
     \"specificProblem\":\"Inbound Traffic threshold crossed\",
     \"alarmedObjectType\":\"ROUTER\",
     \"alarmedObject\":{
        \"id\":\"vManage_000000\",
        \"href\":\" http://api/alarmedobject/000000\"
     },
     \"sourceSystemId\":\"SOURCE_SYSTEM_vManage_00000_000_00\",
     \"alarmDetails\":\"Software Failure on SD-WAN Controller vManage_000000\",
     \"alarmEscalation\": false,
     \"state\":\"RAISED\",
     \"alarmChangedTime\":\"2017-08-15T07:04:15.666Z\",
     \"proposedRepairActions\":\"Switch in standby equipment\",
     \"alarmReportingTime\":\"2017-06-15T07:04:15.666Z\",
     \"alarmRaisedTime\":\"2020-09-15T07:04:15.666Z\",
     \"plannedOutageIndication\":\"IN_SERVICE\",
     \"serviceAffecting\":true,
     \"affectedService\":[
        {
           \"id\":\"SD WAN Enterprise Solutions\",
           \"href\":\"http://api/service/vlan_dot0_dot0\"
        },
        {
           \"id\":\"Santa Clara SD WAN Application Service\",
           \"href\":\"http://api/service/vlan_dot0_dot0\"
        }
     ] 
 }" \
--user 'user:'password'
```

Response body.

```
{
  "result": {
    "alarmChangedTime": "2017-08-15T07:04:15.666Z",
    "id": "6e116bb8db09201087b9a8394b961950_<external-alarm-id>"
  }
}
```

## Alarm Management Open API – POST /sn\_ind\_tmf642/alarm\_mgmt/alarm

Creates an alarm record in the Events \[em\_event\] table.

When the alarm record is created, an ID for the alarm is added in the **Message key** field.

An alert record might also be created based on [Alert management rules](https://www.servicenow.com/docs/access?context=alert-management-rule&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

This endpoint writes the response body to the **Additional Info** field of the event record in the Events \[em\_event\] table.

### URL format

Default URL: `/api/sn_ind_tmf642/alarm_mgmt/alarm`

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

affectedService

</td><td id="alm-mgmt-affectedService-entry">

List of one or more services affected by the alarm.Data type: Array of Objects

```
"affectedService":[
  {
    "href": "String",
    "id": "String"
  },
]
```

</td></tr><tr><td>

affectedService.href

</td><td id="alm-mgmt-affectedServiceHREF-entry">

URL reference that provides details of the affected service.Data type: String

</td></tr><tr><td>

affectedService.id

</td><td>

Required. Identifier of the service affected by the alarm. This value maps to the affected configuration item \(CI\) on the alert.

Data type: String

</td></tr><tr><td>

alarmDetails

</td><td>

Additional details about the alarm.Data type: String

</td></tr><tr><td>

alarmedObject

</td><td>

Required. Details of the alarm object. ```
"alarmedObject":
{
  "href": "String",
  "id": "String"
}
```

 Data type: Object

</td></tr><tr><td>

alarmedObject.id

</td><td>

Required. Unique identifier of the alarm object. This value maps to a CI in the system. Data type: String

</td></tr><tr><td>

alarmedObject.href

</td><td id="alm-mgmt-create-alarmobj-href-entry">

URL reference to get the details of the alarm object.

Data type: String

</td></tr><tr><td>

alarmedObjectType

</td><td>

Type or class of object associated with the event.Data type: String

</td></tr><tr><td>

alarmRaisedTime

</td><td>

Date and time at which the alarm occurs at its source.Data type: String

</td></tr><tr><td>

alarmReportingTime

</td><td>

Date and time at which the OSS reports its alarm.This value might differ from the **alarmRaisedTime** value. For example, if an element management system \(EMS\) maintains the alarm list:

-   The **alarmRaisedTime** is the time of alarm detection by the network element \(NE\).
-   The **alarmReportingTime** is the alarm report time of storage in the EMS alarm list.

Data type: String

</td></tr><tr id="alm-mgmt-create-alarmtype"><td>

alarmType

</td><td>

Required. Alarm category. Data type: String

</td></tr><tr><td>

crossedThresholdInformation

</td><td>

Details about the crossed threshold.Data type: Object

```
"crossedThresholdInformation":
{
  "direction": "String",
  "granularity": "String",
  "indicatorName": "String",
  "indicatorUnit": "String",
  "observedValue": "String",
  "thresholdCrossingDescription": "String",
  "thresholdId": "String",
  "thresholdRef": "String"
}
```

</td></tr><tr><td>

crossedThresholdInformation.direction

</td><td>

Threshold crossing direction.Valid values:

-   DOWN
-   UP

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.granularity

</td><td>

Granularity at which the indicator is evaluated for threshold crossing. For example, `5MINUTES`.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorName

</td><td>

Name of the indicator that crosses the alarm threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorUnit

</td><td>

Measurement unit of the indicator corresponding to the crossed threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.observedValue

</td><td>

Number identifying the indicator crossing the threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdCrossingDescription

</td><td>

More threshold details of the threshold crossing alarm.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdId

</td><td>

Required.Unique identifier of the threshold that caused the alarm.

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdRef

</td><td>

URL of the threshold object.Data type: String

</td></tr><tr><td>

externalAlarmId

</td><td>

Required. Unique identifier for the alarm from the source system posting the alarm. Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier for the system to identify and process the alarm payload as an event. This value must be empty if used in the payload. The system generates this unique ID for the event and sends it as part of the response payload.

 Data type: String

</td></tr><tr><td>

perceivedSeverity

</td><td>

Required. Alarm severity. Valid values:

-   CLEAR
-   CRITICAL
-   MAJOR
-   MINOR
-   WARNING

Data type: String

</td></tr><tr><td>

plannedOutageIndication

</td><td>

Indicates that the managed object for this alarm is in a planned outage state. For example, planned maintenance or out-of-service.Data type: String

</td></tr><tr><td>

probableCause

</td><td>

Required. Most likely situation to trigger the alarm. Use with **alarmType** to qualify the alarm.

Data type: String

</td></tr><tr><td>

proposedRepairActions

</td><td>

If available to the system, provides a repair action to resolve the issue that triggers the alarm.Data type: String

</td></tr><tr><td>

serviceAffecting

</td><td>

Flag that indicates whether the alarm affects service.Valid values:

-   true: Alarm affects service performance or availability.
-   false: Alarm doesn't affect service.

Default: false

Data type: Boolean

</td></tr><tr><td>

sourceSystemId

</td><td>

Required. Instance ID of the source alarm. Data type: String

</td></tr><tr><td>

specificProblem

</td><td id="alm-mgmt-specificProb-entry">

Specific problem that triggers the alarm. Use with the **probableCause** tparameter o qualify the alarm.Data type: String

</td></tr><tr><td>

state

</td><td>

Alarm state.Valid values:

-   Error
-   Ignored
-   Ready
-   Processed

If an invalid value is provided, the state is set to `Ready`.

If the state is `Ready`, an alert is created in the Alert \[em\_alert\] table and the state then becomes `Processed`.

If the state is `Processed`, `Ignored`, or `Error` no alert is created.

Default value: Ready

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_bly_lyb_ynb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad request.Possible reasons:

-   Invalid payload. Missing required alarm ID.
-   Invalid payload. Required field missing:&lt;field name&gt;.
-   Invalid payload. Missing required object.
-   Event not created, failed.
-   Unable to clear event.
-   Unable to update event.
-   The event doesn’t exist.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

affectedService

</td><td id="d3402e76">

List of one or more services affected by the alarm.Data type: Array of Objects

```
"affectedService":[
  {
    "href": "String",
    "id": "String"
  },
]
```

</td></tr><tr><td>

affectedService.href

</td><td id="d3402e89">

URL reference that provides details of the affected service.Data type: String

</td></tr><tr><td>

affectedService.id

</td><td>

Identifier of the service affected by the alarm. This value maps to the affected configuration item \(CI\) on the alert. Data type: String

</td></tr><tr><td>

alarmDetails

</td><td>

Additional details about the alarm.Data type: String

</td></tr><tr><td>

alarmedObject

</td><td>

Details of the alarm object. ```
"alarmedObject":
{
  "href": "String",
  "id": "String"
}
```

Data type: Object

</td></tr><tr><td>

alarmedObject.id

</td><td>

Unique identifier of the alarm object. This value maps to a CI in the system. Data type: String

</td></tr><tr><td>

alarmedObject.href

</td><td id="d3402e404">

URL reference to get the details of the alarm object.

Data type: String

</td></tr><tr><td>

alarmedObjectType

</td><td>

Type or class of object associated with the event.Data type: String

</td></tr><tr><td>

alarmRaisedTime

</td><td>

Date and time at which the alarm occurs at its source.Data type: String

</td></tr><tr><td>

alarmReportingTime

</td><td>

Date and time at which the OSS reports its alarm.This value might differ from the **alarmRaisedTime** value. For example, if an element management system \(EMS\) maintains the alarm list:

-   The **alarmRaisedTime** is the time of alarm detection by the network element \(NE\).
-   The **alarmReportingTime** is the alarm report time of storage in the EMS alarm list.

Data type: String

</td></tr><tr><td>

alarmType

</td><td>

Alarm category. Data type: String

</td></tr><tr><td>

crossedThresholdInformation

</td><td>

Details about the crossed threshold.Data type: Object

```
"crossedThresholdInformation":
{
  "direction": "String",
  "granularity": "String",
  "indicatorName": "String",
  "indicatorUnit": "String",
  "observedValue": "String",
  "thresholdCrossingDescription": "String",
  "thresholdId": "String",
  "thresholdRef": "String"
}
```

</td></tr><tr><td>

crossedThresholdInformation.direction

</td><td>

Threshold crossing direction.Valid values:

-   DOWN
-   UP

Data type: String

</td></tr><tr><td>

crossedThresholdInformation.granularity

</td><td>

Granularity at which the indicator is evaluated for threshold crossing. For example, `5MINUTES`.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorName

</td><td>

Name of the indicator that crosses the alarm threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.indicatorUnit

</td><td>

Measurement unit of the indicator corresponding to the crossed threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.observedValue

</td><td>

Number identifying the indicator crossing the threshold.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdCrossingDescription

</td><td>

More threshold details of the threshold crossing alarm.Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdId

</td><td>

Unique identifier of the threshold that caused the alarm. Data type: String

</td></tr><tr><td>

crossedThresholdInformation.thresholdRef

</td><td>

URL of the threshold object.Data type: String

</td></tr><tr><td>

externalAlarmId

</td><td>

Unique identifier for the alarm from the source system posting the alarm. Data type: String

</td></tr><tr><td>

href

</td><td>

URL of the resource.Data type: String

</td></tr><tr><td>

id

</td><td>

Unique identifier for the system to identify and process the alarm payload as an event. Data type: String

</td></tr><tr><td>

perceivedSeverity

</td><td>

Alarm severity. Valid values:

-   CLEAR
-   CRITICAL
-   MAJOR
-   MINOR
-   WARNING

 Data type: String

</td></tr><tr><td>

plannedOutageIndication

</td><td>

Indicates that the managed object for this alarm is in a planned outage state. For example, planned maintenance or out-of-service.Data type: String

</td></tr><tr><td>

probableCause

</td><td>

Most likely situation to trigger the alarm. Use with **alarmType** to qualify the alarm. Data type: String

</td></tr><tr><td>

proposedRepairActions

</td><td>

If available to the system, provides a repair action to resolve the issue that triggers the alarm.Data type: String

</td></tr><tr><td>

serviceAffecting

</td><td>

Flag that indicates whether the alarm affects service.Valid values:

-   true: Alarm affects service performance or availability.
-   false: Alarm doesn't affect service.

Default: false

Data type: Boolean

</td></tr><tr><td>

sourceSystemId

</td><td>

Instance ID of the source alarm. Data type: String

</td></tr><tr><td>

specificProblem

</td><td id="d3402e342">

Specific problem that triggers the alarm. Use with the **probableCause** tparameter o qualify the alarm.Data type: String

</td></tr><tr><td>

state

</td><td>

Alarm state.Valid values:

-   Error
-   Ignored
-   Ready
-   Processed

If an invalid value is provided, the state is set to `Ready`.

If the state is `Ready`, an alert is created in the Alert \[em\_alert\] table and the state then becomes `Processed`.

If the state is `Processed`, `Ignored`, or `Error` no alert is created.

Default value: Ready

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates an alarm.

```
curl "https://<instance>.service-now.com/api/sn_ind_tmf642/alarm_mgmt/alarm" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
     "href":"http://api/alarm/ROUTER_IF@Cisco-0000-0-0-0-0-00-00-0-- Xz0/00@00",
     "externalAlarmId":"<external-alarm-id>",
     "alarmType":"QualityOfServiceAlarm",
     "type":"QualityOfServiceAlarm",
     "ackState":"acknowledged",
     "perceivedSeverity":"CRITICAL",
     "probableCause":"Threshold crossed",
     "specificProblem":"Inbound Traffic threshold crossed",
     "alarmedObjectType":"ROUTER",
     "alarmedObject":{
        "id":"vManage_000000",
        "href":" http://api/alarmedobject/000000"
     },
     "sourceSystemId":"SOURCE_SYSTEM_vManage_00000_000_00",
     "alarmDetails":"Software Failure on SD-WAN Controller vManage_000000",
     "state":"RAISED",
     "alarmChangedTime":"2017-08-15T07:04:15.666Z",
     "proposedRepairActions":"Switch in standby equipment",
     "alarmReportingTime":"2017-06-15T07:04:15.666Z",
     "alarmRaisedTime":"2020-09-15T07:04:15.666Z",
     "plannedOutageIndication":"IN_SERVICE",
     "serviceAffecting":true,
     "affectedService":[
        {
           "id":"SD WAN Enterprise Solutions",
           "href":"http://api/service/vlan_dot0_dot0"
        },
        {
           "id":"Santa Clara SD WAN Application Service",
           "href":"http://api/service/vlan_dot0_dot0"
        }
     ] 
 }" \
--user 'user':'password'
```

Response body.

```
{
     "href":"http://api/alarm/ROUTER_IF@Cisco-0000-0-0-0-0-00-00-0-- Xz0/00@00",
     "externalAlarmId":"<external-alarm-id>",
     "alarmType":"QualityOfServiceAlarm",
     "type":"QualityOfServiceAlarm",
     "ackState":"acknowledged",
     "perceivedSeverity":"CRITICAL",
     "probableCause":"Threshold crossed",
     "specificProblem":"Inbound Traffic threshold crossed",
     "alarmedObjectType":"ROUTER",
     "alarmedObject":{
        "id":"vManage_000000",
        "href":" http://api/alarmedobject/000000"
     },
     "sourceSystemId":"SOURCE_SYSTEM_vManage_00000_000_00",
     "alarmDetails":"Software Failure on SD-WAN Controller vManage_000000",
     "state":"RAISED",
     "alarmChangedTime":"2017-08-15T07:04:15.666Z",
     "proposedRepairActions":"Switch in standby equipment",
     "alarmReportingTime":"2017-06-15T07:04:15.666Z",
     "alarmRaisedTime":"2020-09-15T07:04:15.666Z",
     "plannedOutageIndication":"IN_SERVICE",
     "serviceAffecting":true,
     "affectedService":[
        {
           "id":"SD WAN Enterprise Solutions",
           "href":"http://api/service/vlan_dot0_dot0"
        },
        {
           "id":"Santa Clara SD WAN Application Service",
           "href":"http://api/service/vlan_dot0_dot0"
        }
     ] 
 }
```

## Alarm Management Open API – POST /sn\_ind\_tmf642/alarm\_mgmt/alarm/\{id\}/clear

Clears a specified alarm and closes any associated alert.

### URL format

Default URL: `/api/sn_ind_tmf642/alarm_mgmt/alarm/{id}/clear`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

id

</td><td>

Unique identifier of the alarm to clear.Data type: String

Table: In the Message key field of the Events \[em\_events\] table.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alarmClearedTime

</td><td>

Date and time at which the alarm clears at the source.Data type: String

Table: In the Time of event field of the Events \[em\_events\] table.

</td></tr><tr><td>

clearSystemId

</td><td>

Required. Name of the instance from which the **alarmCleared** operation was invoked. Data type: String

</td></tr><tr><td>

clearUserId

</td><td>

Required. Unique ID of the user who invoked the **alarmCleared** operation. Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Name|Description|
|----|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

201

</td><td>

Successful. The request was successfully processed.

</td></tr><tr><td>

400

</td><td>

Bad request.Possible reasons:

-   Invalid payload. Missing required alarm ID.
-   Invalid payload. Required field missing:&lt;field name&gt;.
-   Invalid payload. Missing required object.
-   Event not created, failed.
-   Unable to clear event.
-   Unable to update event.
-   The event doesn’t exist.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

alarmClearedTime

</td><td>

Date and time at which the alarm clears at the source.Data type: String

Table: In the Time of event field of the Events \[em\_events\] table.

</td></tr><tr><td>

clearSystemId

</td><td>

Name of the instance from which the **alarmCleared** operation was invoked. Data type: String

</td></tr><tr><td>

clearUserId

</td><td>

Unique ID of the user who invoked the **alarmCleared** operation. Data type: String

</td></tr><tr><td>

href

</td><td>

URL of the alarm.Data type: String

</td></tr><tr><td>

id

</td><td>

Unique ID.Data type: String

Table: In the Message key field of the record in the Events \[em\_events\] table.

</td></tr></tbody>
</table>### cURL request

This example clears an alarm.

```
curl "https://<instance>.service-now.com/api/sn_ind_tmf642/alarm_mgmt/alarm/6e116bb8db09201087b9a8394b961950_<external-alarm-id>/clear" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"alarmClearedTime\": \"2017-08-15 06:04:15\",
  \"clearSystemId\": \"<source_instance_name>\",
  \"clearUserId\": \"SOURCE_SYSTEM_vManage_00000_000_00\" 
}" \
--user 'user':'password'
```

Response body.

```
{
  "result": {
    "alarmClearedTime": "2017-08-15 06:04:15",
    "clearSystemId": "<source_instance_name>",
    "clearUserId": "SOURCE_SYSTEM_vManage_00000_000_00",
    "id": "6e116bb8db09201087b9a8394b961950_<external-alarm-id>"
  }
}
```

