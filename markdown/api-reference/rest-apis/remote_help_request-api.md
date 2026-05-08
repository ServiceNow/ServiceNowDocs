---
title: Remote help request API
description: The Remote help request API provides endpoints to create, view, and fetch lists of IT service requests and their details from an electronic medical record \(EMR\) system. An IT service request is associated with a task type such as an incident in the ServiceNow instance.Inserts electronic medical record \(EMR\) system data into the corresponding ServiceNow tables.Updates a record in the specified remote request data table for the task.Fetches a list of tasks that match the specified ID and query filter.Fetches a single task as specified in the task\_id.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Remote help request API

The Remote help request API provides endpoints to create, view, and fetch lists of IT service requests and their details from an electronic medical record \(EMR\) system. An IT service request is associated with a task type such as an incident in the ServiceNow instance.

You can only use this API when the EMR Help application \(sn\_ind\_rmt\_help\) is installed from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

Role required to access the endpoints of this API: sn\_ind\_rmt\_help.requester.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Remote help request - POST /remote\_help\_request/\{req\_defn\_id\}

Inserts electronic medical record \(EMR\) system data into the corresponding ServiceNow tables.

You need to specify a request definition ID in addition to the parameters for the task and additional data from the EMR system persisted in the request data table associated with the task. You pass two types of data into this endpoint. The first is the request data, which the endpoint inserts into the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table and its associated child tables. The second is the task parameters of the IT service request, which the endpoint inserts into the Remote Request Parameter \[sn\_ind\_rmt\_help\_request\_param\] table. Only data or fields that are defined in the request definitions are processed by the endpoint. For additional information on this data model, see EMR Help data model.

Records are identified using the request definition ID.

### URL format

Versioned URL: `/api/sn_ind_rmt_help/{api_version}/remote_help_request/{req_defn_id}`

Default URL: `/api/sn_ind_rmt_help/remote_help_request/{req_defn_id}`

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

</td></tr><tr><td>

req\_defn\_id

</td><td>

Unique ID of the request definition.Data type: String

Table: In the ID column of the Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request\_data

</td><td>

Required. Name-value pairs of the request data from the EMR system to add in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table and its child tables.For example:

```
"request_data":{
  "additional_info": "String",
  "application": "String",
  "environment": "String",
  "issue_type": "String",
  "millennium_username": "String",
  "position": "String",
  "server": "String",
  "session_recording_id": "String",
  "user_is_physician": "String",
  "work_station": "String"
} 
```

**Note:** Only pass parameters configured in a request definition in the **request\_data** object. Any other parameters are ignored. To learn more, see Configure request definitions for EMR systems.

Data type: Object

</td></tr><tr><td>

source

</td><td>

Required. Name of the EMR system invoking the endpoint as specified in a request definition.For example:

```
"source":"Cerner"
```

Data type: String

</td></tr><tr><td>

task\_parameters

</td><td>

Required. Name-value pairs that describe the task parameters of the IT service request. Each element in the object corresponds to a column in the corresponding task tables such as the Incident \[incident\] table.For example:

```
"task_parameters": {
  "caller_id": "String",
  "contact_type": "String",
  "impact": "String",
  "short_description": "String"
}
```

**Note:** Only pass parameters configured in a request definition in the **task\_parameters** object. Any other parameters are ignored. To learn more, see Configure request definitions for EMR systems.

Data type: Object

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object.Data type: Object

```
"result": {
  "code": "String",
  "error": "String",  
  "errorTranslated": "String",
  "status": "String",
  "task_id": "String",
  "task_table": "String",
  "warning": "String",
  "warningTranslated": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

Application error code when the **result.status** is returned as `failure`.Data type: String

</td></tr><tr><td>

result.error

</td><td>

Error message that is included if the **result.status** is failure.This message is in English only.

Data type: String

</td></tr><tr><td>

result.errorTranslated

</td><td>

Optional localized error message.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the response.Valid values:

-   failure
-   success

Data type: String

</td></tr><tr><td>

result.task\_id

</td><td>

Sys\_id of the created task.Data type: String

</td></tr><tr><td>

result.task\_table

</td><td>

Name of the task table in which the task was created as defined in the request definition.Data type: String

</td></tr><tr><td>

result.warning

</td><td>

Optional warning message. May be included if the **result.status** is `success`. This message is in English only.

Data type: String

</td></tr><tr><td>

result.warningTranslated

</td><td>

Optional localized warning message.Data type: String

</td></tr></tbody>
</table>### cURL request

Insert data from a Cerner EMR system.

```
curl "https://instance.servicenow.com/api/sn_ind_rmt_help/v1/remote_help_request/sn_it_request" 
--request POST \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data "{
  "source":"Cerner",
  "task_parameters":{
    "short_description":"Unable to load patient data",
    "caller_id":"82d4ecb4db40e8100e28aa594b96195c",
    "impact":"2",
    "contact_type":"email"
  },
  "request_data":{
    "application":"Powerchart",
    "server":"CTXCHSITN453",
    "environment":"CTX24",
    "issue_type":"Helpdesk",
    "millennium_username":"JOHN JASON",
    "position":"Lab Tech",
    "session_recording_id":"s5ds34dd96491b959a35010651896k",
    "user_is_physician":"Yes",
    "work_station":"PC354FLR3STATION7",
    "additional_info":"MRN 222333"    
  }
}" \
--user "username":"password"
```

The following output shows both a successful response and an error response.

```
// Successful response
{
  "result": {
    "task_id": "75b09061db2cac100e28aa594b9619fa",
    "status": "success",
    "task_table": "incident",
    "warning": "Ignored invalid fields on table incident : test1",
    "warningTranslated": "Ignored invalid fields on table incident : test1"
  }
}

// Error response
{  
      "result": {
      "status": "failure",
      "code": "1001",
      "error": "Invalid request definition: test_request1",
      "errorTranslated": "Invalid request definition: test_request1"
      }
      }
```

## Remote help request - PUT /remote\_help\_request/\{req\_defn\_id/task/\{task\_id\}

Updates a record in the specified remote request data table for the task.

Enables you to specify a request definition ID in addition to the task sys\_id to update a remote request that was created earlier.

### URL format

Versioned URL: `/api/sn_ind_rmt_help/{api_version}/remote_help_request/{req_defn_id/task/{task_id}`

Default URL: `/api/sn_ind_rmt_help/remote_help_request/{req_defn_id/task/{task_id}`

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

</td></tr><tr><td>

req\_defn\_id

</td><td>

Unique ID of the request definition.Data type: String

Table: In the ID column of the Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table.

</td></tr><tr><td>

task\_id

</td><td>

Sys\_id of the task to update. This field is provided by the EMR system.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request\_data

</td><td>

Required. Name-value pairs of the request data from the EMR system to update the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table or its child table. For example:

```
"request_data": {
 "additional_info" : "Please contact my office for more information."
}

```

**Note:** Only pass parameters configured in a request definition in the **request\_data** object. Any other parameters are ignored. To learn more, see Configure request definitions for EMR systems.

Data type: Object

</td></tr><tr><td>

source

</td><td>

Required. Name of the EMR system invoking the endpoint as specified in a request definition.For example:

```
"source":"Cerner"
```

Data type: String

</td></tr><tr><td>

task\_parameters

</td><td>

Required. Name-value pairs that describe the task parameters of the IT service request. Each element in the object corresponds to a column in the corresponding task tables such as the Incident \[incident\] table.For example:

```
"task_parameters": {
  "impact":"1",
  "contact_type":"phone"
}
```

**Note:** Only pass parameters configured in a request definition in the **task\_parameters** object. Any other parameters are ignored. To learn more, see Configure request definitions for EMR systems.

Data type: Object

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object.Data type: Object

```
"result": {
  "code": "String",
  "error": "String",  
  "errorTranslated": "String",
  "status": "String",
  "warning": "String",
  "warningTranslated": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

Application error code when the **result.status** is returned as `failure`.Data type: String

</td></tr><tr><td>

result.error

</td><td>

Error message that is included if the **result.status** is failure.This message is in English only.

Data type: String

</td></tr><tr><td>

result.errorTranslated

</td><td>

Optional localized error message.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the response.Valid values:

-   failure
-   success

Data type: String

</td></tr><tr><td>

result.warning

</td><td>

Optional warning message. May be included if the **result.status** is `success`. This message is in English only.

Data type: String

</td></tr><tr><td>

result.warningTranslated

</td><td>

Optional localized warning message.Data type: String

</td></tr></tbody>
</table>### cURL request

Update an IT service request created earlier in a Cerner EMR system

```
curl "https://instance.servicenow.com/api/sn_ind_rmt_help/v1/remote_help_request/sn_it_request/task/207e57c1db60a410f50fdc5b4b96192e"
--request PUT \
--header "Accept: application/json" \
--header "Content-Type: application/json" \
--data "{
  "source":"Cerner",
  "task_parameters":{
    "impact":"1",
    "contact_type":"phone"
  },
  "request_data":{
    "additional_info" : "Please contact my office for more information."
  }
}" \
--user "username":"password"

```

The following output shows both a successful response and an error response.

```
// Successful response
{
  "result": {
    "status": "success"
  }
}

// Error response
{
      {
      "result": {
      "status": "failure",
      "code": "1018",
      "error": "Record with sys_id 207e57js1db60a410f50fdc5b4b96192e does not exist in table incident",
      "errorTranslated": "Record with sys_id 207e57js1db60a410f50fdc5b4b96192e incident does not exist in table incident"
      }
      }
      }
```

## Remote help request - GET /remote\_help\_request/\{req\_defn\_id\}

Fetches a list of tasks that match the specified ID and query filter.

**Note:**

-   Reference and choice type fields are always returned as JSON objects with the value and display\_value.
-   DateTime fields are returned as strings and always in UTC.

### URL format

Versioned URL: `/api/sn_ind_rmt_help/{api_version}/remote_help_request/{req_defn_id}`

Default URL: `/api/sn_ind_rmt_help/remote_help_request/{req_defn_id}`

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

</td></tr><tr><td>

req\_defn\_id

</td><td>

Unique ID of the request definition to update.Data type: String

Table: In the ID column of the Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table.

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

query

</td><td>

Required. Encoded query used to filter the result set.Data type: String

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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Return results.Data type: Object

```
"result": {
  "code": "String",
  "error": "String",  
  "errorTranslated": "String",
  "status": "String",
  "task_list": [Array],
  "warning": "String",
  "warningTranslated": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

Application error code when the **result.status** is returned as `failure`.Data type: String

</td></tr><tr><td>

result.error

</td><td>

Error message that is included if the **result.status** is failure.This message is in English only.

Data type: String

</td></tr><tr><td>

result.errorTranslated

</td><td>

Optional localized error message.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the response.Possible values:

-   failure
-   success

Data type: String

</td></tr><tr><td>

result.task\_list

</td><td>

List of tasks. Data type: Array

</td></tr><tr><td>

result.warning

</td><td>

Optional warning message. May be included if the **result.status** is `success`. This message is in English only.

Data type: String

</td></tr><tr><td>

result.warningTranslated

</td><td>

Optional localized warning message.Data type: String

</td></tr></tbody>
</table>### cURL request

Fetch data from a Cerner EMR system

```
curl "https://instance.servicenow.com/api/remote_help_request/v1/sn_it_request/?query=active=true" \ 
--header "Accept: application/json" \
--header "Content-Type: application/json"
{
  "source":"Cerner",
} \
--user "username":"password"
```

The following output shows both a successful response and an error response.

```
// Successful response
{
  "result": {
    "status": "success",
    "task_list": [
      {
        "number": "INC0010096",
        "short_description": "Unable to load data - 1",
        "assigned_to": {
          "value": "7a381da2dbfb5410f50fdc5b4b9619f2",
          "display_value": "Abel Tuter (IT agent)"
        },
        "opened_at": "2020-11-16 18:37:57",
        "closed_at": "",
        "closed_by": {},
        "state": {
          "value": "2",
          "display_value": "In Progress"
        },
        "priority": {
          "value": "5",
          "display_value": "5 - Planning"
        },
        "resolved_at": "",
        "resolved_by": {},
        "task_id": "207e57c1db60a410f50fdc5b4b96192e"
      },
      {
        "number": "INC0010095",
        "short_description": "Application freezes intermittently 3",
        "assigned_to": {},
        "opened_at": "2020-11-16 18:32:05",
        "closed_at": "",
        "closed_by": {},
        "state": {
          "value": "1",
          "display_value": "New"
        },
        "priority": {
          "value": "5",
          "display_value": "5 - Planning"
        },
        "resolved_at": "",
        "resolved_by": {},
        "task_id": "561d1f8ddb20a410f50fdc5b4b9619da"
      }
    ]
  }
}

// Error response
{
  "result": {
  "status": "failure",
  "code": "1019",
  "error": "Invalid query in the request for table incident",
  "errorTranslated": "Invalid query in the request for table incident"
}
```

## Remote help request - GET /remote\_help\_request/\{req\_defn\_id\}/task/\{task\_id\}

Fetches a single task as specified in the **task\_id**.

Enables you to specify a request definition ID and task ID and retrieve the task details.

**Note:**

-   Reference and choice type fields are always returned as JSON objects with the value and display\_value.
-   DateTime fields are returned as strings and always in UTC.
-   Only additional comments are supported in journal type fields.
-   Additional comments are passed back as a JSON array of objects. Each object represents a comment with **created\_on**, **created\_by**, and **value** fields. The latest comments are sent first.

### URL format

Versioned URL: `/api/sn_ind_rmt_help/{api_version}/remote_help_request/{req_defn_id}/task/{task_id}`

Default URL: `/api/sn_ind_rmt_help/remote_help_request/{req_defn_id}/task/{task_id}`

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

</td></tr><tr><td>

req\_defn\_id

</td><td>

Unique ID of the request definition.Data type: String

Table: In the ID column of the Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table.

</td></tr><tr><td>

task\_id

</td><td>

Sys\_id of the task to return. This field is provided by the EMR system.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
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

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Return results.Data type: Object

```
"result": {
  "code": "String",
  "error": "String",  
  "errorTranslated": "String",
  "status": "String",
  "task_parameters": {Object},
  "warning": "String",
  "warningTranslated": "String"
}
```

</td></tr><tr><td>

result.code

</td><td>

Application error code when the **result.status** is returned as `failure`.Data type: String

</td></tr><tr><td>

result.error

</td><td>

Error message that is included if the **result.status** is failure.This message is in English only.

Data type: String

</td></tr><tr><td>

result.errorTranslated

</td><td>

Optional localized error message.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the response.Possible values:

-   failure
-   success

Data type: String

</td></tr><tr><td>

result.task\_parameters

</td><td>

Required. Name-value pairs that describe the task parameters of the IT service request. Each element in the object corresponds to a column in the corresponding task tables such as the Incident \[incident\] table.Data type: Object

</td></tr><tr><td>

result.warning

</td><td>

Optional warning message. May be included if the **result.status** is `success`. This message is in English only.

Data type: String

</td></tr><tr><td>

result.warningTranslated

</td><td>

Optional localized warning message.Data type: String

</td></tr></tbody>
</table>### cURL request

Fetch data from a Cerner EMR system

```
curl "https://instance.servicenow.com/api/sn_ind_rmt_help/v1/remote_help_request/sn_it_request/task/207e57c1db60a410f50fdc5b4b96192e"\ 
--request GET \ 
--header "Accept: application/json"\ 
--user "username":"password"
```

The following output shows both a successful response and an error response.

```
// Successful response
{
  "result": {
    "status": "success",
    "task_parameters": {
      "number": "INC0010096",
      "short_description": "Unable to load data - 1",
      "state": {
        "value": "2",
      "display_value": "In Progress"
      },
      "assigned_to": {
        "value": "7a381da2dbfb5410f50fdc5b4b9619f2",
        "display_value": "Abel Tuter (IT agent)"
      },
      "priority": {
        "value": "5",
        "display_value": "5 - Planning"
      },
      "caller_id": {
      "value": "82d4ecb4db40e8100e28aa594b96195c",
      "display_value": "Abel Tuter Requester"
    },
    "opened_at": "2020-11-16 18:37:57",
    "closed_at": "",
    "closed_by": {},
    "description": "",
    "impact": {
      "value": "1",
      "display_value": "1 - High"
    },
    "opened_by": {
      "value": "82d4ecb4db40e8100e28aa594b96195c",
      "display_value": "Abel Tuter Requester"
    },
    "close_code": {},
    "close_notes": "",
    "urgency": {
      "value": "3",
      "display_value": "3 - Low"
    },
    "category": {
      "value": "inquiry",
      "display_value": "Inquiry / Help"
    },
    "resolved_at": "",
    "resolved_by": {},
    "comments": [
      {
        "created_on": "2020-11-17 18:20:04",  
        "created_by": "Abel Tuter Requester",
        "value": "You can reach me during office hours."
      },
      {
        "created_on": "2020-11-16 18:40:14",
        "created_by": "Abel Tuter Requester",
        "value": "You can reach me during office hours."
      },
      {
        "created_on": "2020-11-16 18:38:29",
        "created_by": "Abel Tuter",
        "value": "Hello there\rName of app please"
      }],
    "task_id": "207e57c1db60a410f50fdc5b4b96192e"
    }
  }
}

// Error response
{
  "result": {
    "status": "failure",
    "code": "1001",
    "error": "Invalid request definition: test_request2",
    "errorTranslated": "Invalid request definition: test_request2"
  }
}
```

