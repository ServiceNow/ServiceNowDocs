---
title: Project Portfolio Management API
description: The Project Portfolio Management API provides endpoints to bulk import cost plans and project tasks.Creates cost plans in the Cost Plan \[cost\_plan\] table.Creates a project and associated project tasks.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Project Portfolio Management API

The Project Portfolio Management API provides endpoints to bulk import cost plans and project tasks.

The PPM Standard plugin \(com.snc.financial\_planning\_pmo\) is required to access this API. The calling user must have the it\_project\_manager role.

This API is provided within the `now` namespace.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Project Portfolio Management - POST /now/ppm/insert\_cost\_plans

Creates cost plans in the Cost Plan \[cost\_plan\] table.

### URL format

Default URL: `/api/now/ppm/insert_cost_plans`

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

end\_fiscal\_period

</td><td>

Required. Sys\_id of the ending fiscal period for the cost plan. Located in the Fiscal Period \[fiscal\_period\] table.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the cost plan.Data type: String

</td></tr><tr><td>

resource\_type

</td><td>

Required. Sys\_id of the resource type. Located in the Resource Type Definition \[resource\_type\_definition\] table.Data type: String

</td></tr><tr><td>

start\_fiscal\_period

</td><td>

Required. Sys\_id of the starting fiscal period for the cost plan. Located in the Fiscal Period \[fiscal\_period\] table.Data type: String

</td></tr><tr><td>

task

</td><td>

Required. Sys\_id of the project or demand for the cost plan. Located in the Project \[pm\_project\] or Demand \[dmn\_demand\] table.Data type: String

</td></tr><tr><td>

unit\_cost

</td><td>

Required. Unit cost for the cost plan.Data type: String

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

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing information about the status of the API request.Data type: Object

 ```
"result": {
   "status": "String"
}
```

</td></tr><tr><td>

result.status

</td><td>

Status of the API request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example imports two cost plans.

```
curl "https://instance.servicenow.com/api/now/ppm/insert_cost_plans" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "[
   {
      "name": "Cost plan 1",
      "resource_type": "3d16eaf79330120064f572edb67ffb04",
      "start_fiscal_period": "ed47e5d90b3010108d9ac74363673a98",
      "end_fiscal_period": "0a47e5d90b3010108d9ac74363673afd",
      "task": "0fc9f992db601810852ca6dc13961951",
      "unit_cost": 1200
   },
   {
      "name": "Cost plan 2",
      "resource_type": "3d16eaf79330120064f572edb67ffb04",
      "start_fiscal_period": "ed47e5d90b3010108d9ac74363673a98",
      "end_fiscal_period": "7947e5d90b3010108d9ac74363673ac9",
      "task": "0fc9f992db601810852ca6dc13961951",
      "unit_cost": 3600
   }
]" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "status": "success"
   }
}
```

## Project Portfolio Management - POST /now/ppm/insert\_project\_tasks

Creates a project and associated project tasks.

Projects are created in the Project \[pm\_project\] table and project tasks are created in the Project Task \[pm\_project\_task\] table.

### URL format

Default URL: `/api/now/ppm/insert_project_tasks`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table id="table_qqf_x5s_bwb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

child\_tasks

</td><td>

Array of tasks for the project. Each task is an object in the array.Data type: Array

 ```
"child_tasks": [
   {
      "child_tasks": [Array],
      "external_id": "String",
      "short_description": "String" 
   }
]
```

</td></tr><tr><td>

child\_tasks.child\_tasks

</td><td>

Array of child tasks for the parent task. Each child task is an object in the array. Each child task can have its own array of child tasks. Data type: Array

 ```
"child_tasks": [
   {
      "child_tasks": [Array],
      "external_id": "String",
      "short_description": "String" 
   }
]
```

</td></tr><tr><td>

child\_tasks.external\_id

</td><td>

Unique identifier of the task from the external system.Data type: String

</td></tr><tr><td>

child\_tasks.short\_description

</td><td>

Short description of the task.Data type: String

</td></tr><tr><td>

end\_date

</td><td>

End date for the project.Data type: String

</td></tr><tr><td>

external\_id

</td><td>

Unique identifier of the project from the external system.Data type: String

</td></tr><tr><td>

short\_description

</td><td>

Short description of the project.Data type: String

</td></tr><tr><td>

start\_date

</td><td>

Start date for the project.Data type: String

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

### Response body parameters \(JSON\)

<table id="table_wtd_kbt_bwb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing information about the status of the API request.Data type: Object

 ```
"result": {
   "status": "String"
}
```

</td></tr><tr><td>

result.status

</td><td>

Status of the API request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example imports a project with two tasks \(zpq\_T1 and zpq\_T2\). The first task contains several child tasks, and the second task has dependencies on the child tasks from the first task.

```
curl "https://instance.servicenow.com/api/now/ppm/insert_project_tasks" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   "start_date": "2022-05-18 08:00:00",
   "end_date": "2022-05-18 17:00:00",
   "short_description": "zpq_Project",
   "external_id": "0",
   "child_tasks": [
      {
         "short_description": "zpq_T1",
         "external_id": "1",
         "child_tasks": [
            {
               "external_id": "1.1",
               "short_description": "zpq_T11",
               "child_tasks": [
                  {
                     "external_id": "1.1.1",
                     "short_description": "zpq_T111"
                  }
               ]
            },
            {
               "external_id": "1.2",
               "short_description": "zpq_T12"
            }
         ]
      },
      {
         "short_description": "zpq_T2",
         "external_id": "2",
         "dependencies": [
            {
               "external_id": "1.1",
               "lag": -1,
               "type": "fs"
            },
            {
               "external_id": "1.2",
               "lag": 2,
               "type": "fs"
            }
         ]
      }
   ]
}" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "status": "success"
   }
}
```

