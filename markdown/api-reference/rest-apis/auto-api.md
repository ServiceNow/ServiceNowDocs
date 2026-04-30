---
title: Automation Center API
description: The Automation Center API provides endpoints to create and update data related to robots, processes, and execution jobs. By leveraging this API, you can integrate and reflect details from your automation workflows into the Automation Center dashboard.Creates robot, process, and execution events.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Automation Center API

The Automation Center API provides endpoints to create and update data related to robots, processes, and execution jobs. By leveraging this API, you can integrate and reflect details from your automation workflows into the Automation Center dashboard.

Key concepts of the API:

-   Robots: Software agents that execute bot processes. RPA robots can operate in attended or unattended modes.
-   Processes: Instances of RPA workflows executed on a specific robot. To uniquely identify a process, both the process ID and the robot ID must be specified.
-   Executions: Individual tasks performed within a process, such as transferring information from one resource to another \(such as, copying data from emails into a spreadsheet\).

How to use the API:

You can use the API to send data from third-party RPA tools, including robots, processes, and executions, to Automation Center.

Recommended Workflow:

1.  Send the robot data.
2.  Send the process data linked to the sent robot.
3.  Send execution data that references the corresponding robot and process.

    **Note:** Execution data without its associated robot and process already captured in Automation Center will not appear on the dashboard.


Additional information:

-   Event retention: Events created using this API are automatically removed from your instance after 14 days \(default setting\).
-   Record limits: Each API call can handle a maximum of 2,000 records. This limit cannot be changed.
-   Event deletion: This API does not support event deletion.

This API requires the Automation Center plugin to be active and requires the user to have either the sn\_as.automation\_technical\_user or sn\_ac.automation\_admin role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Automation Center - POST /sn\_ac/automation/rpa

Creates robot, process, and execution events.

These events provide process automation. They appear in the Overview and Execution Automation Center dashboards to measure and monitor the output from multiple RPA vendors.

### URL format

Versioned URL: `/api/sn_ac/{api_version}/automation/rpa`

Default URL: `/api/sn_ac/v1/automation/rpa`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

departmentName

</td><td>

Process and robot event types only. Name of the department to which the event belongs. This value is stored in the following tables depending on the event type:

-   process: department field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.
-   robot: department field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

</td></tr><tr><td>

domainId

</td><td>

Sys\_id of the domain to which the event belongs. This value is stored in the following tables depending on the event type:

-   execution: sys\_domain field in the Automation Execution \[sn\_ac\_automation\_execution\] table.
-   process: sys\_domain field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.
-   robot: sys\_domain field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

</td></tr><tr><td>

endtime

</td><td>

Execution event type only. End time of the execution. This value is stored in the end\_time field in the Automation Execution \[sn\_ac\_automation\_execution\] table.Format: YYYY-MM-DD HH:MM:SS

Data type: String

</td></tr><tr><td>

environment

</td><td>

Execution event type only. Environment of the execution, such as a URL. This value is stored in the environment field in the Automation Execution \[sn\_ac\_automation\_execution\] table.**Note:** This value is not used by the ServiceNow instance and can contain any value required by your implementation.

Data type: String

</td></tr><tr><td>

errorMessage

</td><td>

Execution event type only. Name of the error message log. This value is stored in the message field in the Automation Execution \[sn\_ac\_automation\_execution\] table.Data type: String

</td></tr><tr><td>

eventName

</td><td>

Required. Name of the event type. This value determines the type of event to process.Valid values \(case-sensitive\):

-   execution
-   process
-   robot

Data type: String

</td></tr><tr><td>

id

</td><td>

Required. Unique numeric identifier of the associated event. This value is stored in the following tables depending on the event type:

-   execution: automation\_execution\_id field in the Automation Execution \[sn\_ac\_automation\_execution\] table.
-   process: correlation\_id field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.
-   robot: correlation\_id field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: Number \(Integer\)

</td></tr><tr><td>

name

</td><td>

Process and robot event types only. Required. Name of the event. This value is stored in the following tables depending on the event type:

-   process: name field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.
-   robot: name field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

</td></tr><tr><td>

priority

</td><td>

Execution event type only. Priority of the execution.Valid values \(case-sensitive\):

-   Critical
-   High
-   Medium
-   Low

This value is stored in the priority field in the Automation Execution \[sn\_ac\_automation\_execution\] table.Data type: String

Default: None - Not displayed in the dashboard.

</td></tr><tr><td>

processId

</td><td>

Execution event type only. Required. Unique identifier of the process on which to run the execution. This value is located in the correlation\_id field of the corresponding process record in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.This value is stored in the automation field in the Automation Execution \[sn\_ac\_automation\_execution\] table.

Data type: String

</td></tr><tr><td>

robotId

</td><td>

Execution event type only. Required. Unique identifier of the robot on which to run the execution. This value is located in the correlation\_id field of the corresponding robot record in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table. This value is stored in the robot field in the Automation Execution \[sn\_ac\_automation\_execution\] table.

Data type: String

</td></tr><tr><td>

source

</td><td>

Required. Source to which the event belongs, such as "servicenow\_rpa". This value is located in the internal\_name field of the Automation Source \[sn\_ac\_automation\_source\] table. This value is stored in the following tables depending on the event type:

-   execution: Source field in the Automation Execution \[sn\_ac\_automation\_execution\] table.
-   process: Source field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.
-   robot: Source field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

</td></tr><tr><td>

starttime

</td><td>

Execution event type only. Start time of the execution. This value is stored in the start\_time field in the Automation Execution \[sn\_ac\_automation\_execution\] table.Data type: String

Format: YYYY-MM-DD HH:MM:SS

</td></tr><tr><td>

state

</td><td>

Robot and execution event types only. State of the associated event.Valid values for robot \(case-sensitive\):

-   Cancelled
-   Complete
-   Error
-   Queued
-   Running

Default: Queued

Possible values for execution \(case-sensitive\):

-   Available
-   Busy
-   Disconnected
-   New
-   Responsive

Default: New

This value is stored in the following tables depending on the event type:

-   execution: state field in the Automation Execution \[sn\_ac\_automation\_execution\] table.
-   robot: robot\_state field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

</td></tr><tr><td>

status

</td><td>

Process event type only. Required. Status of the process.Possible values \(case-sensitive\):

-   Build
-   In Maintenance
-   In Use
-   Retired

This value is stored in the life\_cycle\_stage\_status field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.Data type: String

</td></tr><tr><td>

triggeredBy

</td><td>

Execution event type only. Trigger source of the execution. This value is stored in the trigger\_by field in the Automation Execution \[sn\_ac\_automation\_execution\] table.**Note:** This value is not used by the ServiceNow instance and can contain any value required by your implementation.

Data type: String

</td></tr><tr><td>

type

</td><td>

Process and robot event types only. Required for process, Optional for robot. Type of processing to perform.Valid values \(case-sensitive\):

-   Attended
-   Unattended

This value is stored in the following tables depending on the event type:

-   process: process\_type field in the Base Bot Process \[cmdb\_ci\_base\_rpa\_process\] table.
-   robot: robot\_type field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

Default: Unattended for robot

</td></tr><tr><td>

version

</td><td>

Robot event type only. Version of the robot.This value is stored in the version field in the Base Robot \[cmdb\_ci\_base\_rpa\_robot\] table.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Failure. The request was rejected, due to mandatory fields missing or the request contains invalid values. The associated error message describes the reason for failure.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Empty if the request is successful. For failure, additional information is provided.Data type: Object

```
"result": {
  "fields": {
    "<record_number>": [Array]
  }
  "reason": "String"
}
```

For example, if records 1, 2, and 3 are all missing a required field, a message similar to the following is returned:

```
{
  "result": {
    "fields": {
      "1": [
        "id"
      ],
      "2": [
        "status"
      ],
      "3": [
        "name"
      ]
    },
    "reason": "We are not able to process the data as following records have insufficient data"
  }
}
```

</td></tr></tbody>
</table>### cURL request

The following code example shows how to post three robot event type records.

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  records: [{
    id: 8001,
    name: "Quotes system Automation Robot",
    state: "Available",
    status: "In Use",
    version: 5.6,
    departmentName: "Customer Support",
    type: "Unattended",
    source: "servicenow_rpa",
    eventName: "robot"
  },
  {
    id: 8002,
    name: "Invoice Matching Robot",
    state: "Responsive",
    status: "In Maintenance",
    version: 3,
    departmentName: "HR",
    type: "Unattended",
    source: "servicenow_rpa",
    eventName: "robot"
  },
  {
    id: 8003,
    name: "Data Reconciliation Robot",
    state: "Busy",
    status: "Retired",
    version: 2,
    departmentName: "Finance",
    type: "Unattended",
    source: "servicenow_rpa",
    eventName: "robot"
  }]
} "\
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

### cURL request

The following code example shows how to post three process event type records.

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  records: [{
    id: 9001,
    name: "RPA Execution Process",
    status: "In Maintenance",
    type: "Attended",
    departmentName: "Customer Support",
    source: "servicenow_rpa",
    eventName: "process"
  },
  {
    id: 9002,
    name: "Customer Onboarding",
    status: "In Use",
    type: "Attended",
    departmentName: "Finance",
    source: "servicenow_rpa",
    eventName: "process"
  },
  {
    id: 9003,
    name: "Data Reconciliation",
    status: "Retired",
    type: "Unattended",
    departmentName: "HR",
    source: "servicenow_rpa",
    eventName: "process"
  }]
}" \
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

### cURL request

The following code example shows how to post three execution event type records.

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  records: [{
    id: 7001,
    name: "Customer Onboarding",
    starttime: "2022-03-18 00:49:13",
    endtime: "2022-03-20 00:58:03",
    state: "Running",
    priority: "Critical",
    environment: "system",
    triggeredBy: "Schedule",
    processId: 9001,
    robotId: 8001,
    source: "servicenow_rpa",
    eventName: "execution"
  },
  {
    id: 7002,
    name: "Data Reconciliation",
    starttime: "2022-04-30 00:19:11",
    endtime: "2022-05-02 00:41:35",
    state: "Error",
    priority: "Low",
    environment: "system",
    triggeredBy: "API",
    processId: 9002,
    robotId: 8002,
    source: "servicenow_rpa",
    eventName: "execution"
  },
  {
    id: 7003,
    name: "Customer Onboarding",
    starttime: "2022-01-22 02:38:53",
    endtime: "2022-01-23 02:50:44",
    state: "Queued",
    priority: "Moderate",
    environment: "system",
    triggeredBy: "Schedule",
    processId: 9003,
    robotId: 8003,
    source: "servicenow_rpa",
    eventName: "execution"
  }]
} "\
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

### cURL request

The following code example shows how to create or update a process. You create a process by passing all of the mandatory parameters for a process to execute along with the **eventName** set to "process". The mandatory parameters needed to create a process are: **id**, **type**, **status**, **name**, and **source**.

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
records: [{
id: 9001,
name: "RPA Execution Process",
status: "In Maintenance",
type: "Attended",
departmentName: "Customer Support",
source: "servicenow_rpa",
eventName: "process"
}]
} "\
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

### cURL request

The following code example shows how to publish a process. You can publish a process by passing the **status** parameter set to "Published".

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
records: [{
id: 9002,
name: "RPA Execution Process",
status: "Published",
type: "Attended",
departmentName: "Customer Support",
source: "servicenow_rpa",
eventName: "process"
}]
} "\
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

### cURL request

The following code example shows how to create or update a robot. You create a robot by passing all of the mandatory parameters for a robot along with the **eventName** set to "robot". The mandatory parameters needed to create a robot are: **id**, **status**, **name**, and **source**.

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
records: [{
id: 8001,
name: "Quotes system Automation Robot",
state: "Available",
status: "In Use",
version: 5.6,
departmentName: "Customer Support",
type: "Unattended",
source: "servicenow_rpa",
eventName: "robot"
} "\
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

### cURL request

The following code example shows how to create or update an execution. You create an execution by passing all of the mandatory parameters for an execution along with the **eventName** set to "execution". The mandatory parameters needed to create an execution are: **id**, **processId**, **robotId**, and **source**.

```
curl "https://instance.servicenow.com/api/sn_ac/automation/rpa" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
records: [{
id: 7001,
name: "Customer Onboarding",
starttime: "2022-03-18 00:49:13",
endtime: "2022-03-20 00:58:03",
state: "Running",
priority: "Critical",
environment: "http://acqa.servicenow.com",
triggeredBy: "Schedule",
processId: 9001,
robotId: 8001,
source: "servicenow_rpa",
eventName: "execution",
errorMessage:"Error due to Inactivity"
}]
} "\
--user "username":"password"
```

This endpoint only returns an HTTP status code on success and an HTTP status code and error message on failure.

```
None
```

