---
title: DevOps Config API
description: The DevOps Config API provides endpoints to manage your applications.Deletes an application.Retrieves an application.Updates an application.Creates an application.
locale: en-US
release: xanadu
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 12
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# DevOps Config API

The DevOps Config API provides endpoints to manage your applications.

This API requires the DevOps Config application and is provided within the `sn_devops_config` namespace.

For DELETE, PATCH, and POST operations, the calling user must have the sn\_devops\_config.admin role. For GET operations, the calling user must have the sn\_devops\_config.viewer or sn\_devops\_config.admin role.

Use the DevOps Config API for application life cycle management. For more information about managing applications with DevOps Config, see [Configuring DevOps Config](https://www.servicenow.com/docs/access?context=setting-up-devops-config-validation&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## DevOps Config - DELETE /devops\_config/application/\{appid\}

Deletes an application.

### URL format

Versioned URL: `/api/sn_devops_config/v1/devops_config/application/{appid}`

Default URL: `/api/sn_devops_config/devops_config/application/{appid}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

appid

</td><td>

Sys\_id of the application to delete. Located in the CDM Application \[sn\_cdm\_application\] table.Data type: String

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
|400|Bad request. Invalid application id.|
|403|Forbidden. The user doesn't have permission to access the API.|

### Response body parameters \(JSON\)

<table id="table_z3v_z5d_gvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Error information. This parameter is only returned if the request failed.Data type: Object

 ```
"error": { 
   "message": "String", 
   "detail": "String" 
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional details about why the request failed.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failed.Data type: String

</td></tr><tr><td>

result

</td><td>

Result object containing information about the request.Data type: Object

 ```
"result": { 
   "errors": [Array], 
   "success": [Array] 
}
```

</td></tr><tr><td>

result.errors

</td><td>

Array of errors from the request. The array is empty for successful requests.Data type: Array

</td></tr><tr><td>

result.success

</td><td>

Success message for the request. The array is empty for failed requests.Data type: Array

</td></tr><tr><td>

status

</td><td>

Status of the request. This parameter is only returned if the request failed.Possible value: failure

 Data type: String

</td></tr></tbody>
</table>### cURL request

This example deletes an application.

```
curl "https://instance.service-now.com/api/sn_devops_config/devops_config/application/38e17dc3473d111072566862736d43c7" \ 
--request DELETE \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Response body.

```
{ 
  "result": { 
    "errors": [], 
    "success": [ 
      "CDM Application Demo Application 1234 has been deleted successfully." 
    ] 
  } 
}
```

### cURL request

This example shows an error response when a user doesn't have permission to access the API.

```
curl "https://instance.service-now.com/api/sn_devops_config/devops_config/application/38e17dc3473d111072566862736d43c7" \ 
--request DELETE \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Error response.

```
{ 
  "error": { 
    "message": "User Not Authorized", 
    "detail": "Failed API level ACL Validation" 
  }, 
  "status": "failure" 
}
```

## DevOps Config - GET /devops\_config/application/\{appid\}

Retrieves an application.

### URL format

Versioned URL: `/api/sn_devops_config/v1/devops_config/application/{appid}`

Default URL: `/api/sn_devops_config/devops_config/application/{appid}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

appid

</td><td>

Sys\_id of the application to retrieve. Located in the CDM Application \[sn\_cdm\_application\] table.Data type: String

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
|400|Bad request. Invalid application id.|
|403|Forbidden. The user doesn't have permission to access the API.|

### Response body parameters \(JSON\)

<table id="table_z3v_z5d_gvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Error information. This parameter is only returned if the request failed.Data type: Object

 ```
"error": { 
   "message": "String", 
   "detail": "String" 
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional details about why the request failed.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failed.Data type: String

</td></tr><tr><td>

result

</td><td>

Result object containing information about the request.Data type: Object

 ```
"result": { 
  "data": {Object},
  "message": "String",
  "status": Number
}
```

</td></tr><tr><td>

result.data

</td><td>

Data for the application.Data type: Object

 ```
"data": { 
  "appDescription": "String", 
  "appId": "String",
  "appManagedByGroups": [Array],
  "appManufacturerId": "String", 
  "appManufacturerName": "String", 
  "appModelId": "String", 
  "appModelName": "String", 
  "appModelOwnerId": "String", 
  "appModelOwnerName": "String", 
  "appName": "String", 
  "sdlcType": "String"
}
```

</td></tr><tr><td>

result.data.appDescription

</td><td>

Description of the application.Data type: String

</td></tr><tr><td>

result.data.appId

</td><td>

Sys\_id of the application. Located in the CDM Application \[sn\_cdm\_application\] table.Data type: String

</td></tr><tr><td>

result.data.appManagedByGroups

</td><td>

Comma-separated list of sys\_ids of the groups that manage the application. Located in the Group \[sys\_user\_group\] table.Data type: String

</td></tr><tr><td>

result.data.appManufacturerId

</td><td>

Sys\_id of the manufacturer. Located in the Company \[core\_company\] table.Data type: String

</td></tr><tr><td>

result.data.appManufacturerName

</td><td>

Name of the manufacturer.Data type: String

</td></tr><tr><td>

result.data.appModelId

</td><td>

Sys\_id of the application model. Located in the Application Model \[cmdb\_application\_product\_model\] table.Data type: String

</td></tr><tr><td>

result.data.appModelName

</td><td>

Name of the application model. Located in the Application Model \[cmdb\_application\_product\_model\] table.Data type: String

</td></tr><tr><td>

result.data.appModelOwnerId

</td><td>

Sys\_id of the application model owner. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

result.data.appModelOwnerName

</td><td>

Name of the application model owner.Data type: String

</td></tr><tr><td>

result.data.appName

</td><td>

Name of the application.Data type: String

</td></tr><tr><td>

result.data.error

</td><td>

Error information. This parameter is only returned if the request failed.Data type: String

</td></tr><tr><td>

result.data.sdlcType

</td><td>

The type of application.Possible values:

-   application
-   infrastructure

 Data type: String

</td></tr><tr><td>

result.message

</td><td>

Information about the successful or unsuccessful outcome of the request.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status code for the request.Possible values:

-   200
-   400
-   403

 Data type: Number

</td></tr><tr><td>

status

</td><td>

Status of the request. This parameter is only returned if the request failed.Possible value: failure

 Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves an application.

```
curl "https://instance.service-now.com/api/sn_devops_config/devops_config/application/38e17dc3473d111072566862736d43c7" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Response body.

```
{ 
  "result": { 
    "status": 200, 
    "message": "Success", 
    "data": { 
      "appName": "Demo Application 1234", 
      "appId": "38e17dc3473d111072566862736d43c7", 
      "appDescription": "Updated description of Demo Application created from REST API", 
      "sdlcType": "application", 
      "appModelId": "a4e13dc3473d111072566862736d4307", 
      "appModelName": "Demo Application 1234", 
      "appManufacturerId": "262702654725d950a34a3085d36d435e", 
      "appManufacturerName": "", 
      "appModelOwnerId": "6816f79cc0a8016401c5a33be04be441", 
      "appModelOwnerName": "System Administrator", 
      "appManagedByGroups": [] 
    } 
  } 
}
```

### cURL request

This example shows an error response when a user provides an invalid application id.

```
curl "https://instance.service-now.com/api/sn_devops_config/devops_config/application/18a17de3283d15107256686277777777" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Error response.

```
{ 
  "result": { 
    "status": 400, 
    "message": "No valid Application", 
    "data": { 
      "error": "No valid Application" 
    } 
  } 
}
```

## DevOps Config - PATCH /devops\_config/application/\{appid\}

Updates an application.

### URL format

Versioned URL: `/api/sn_devops_config/v1/devops_config/application/{appid}`

Default URL: `/api/sn_devops_config/devops_config/application/{appid}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

appid

</td><td>

Sys\_id of the application to update. Located in the CDM Application \[sn\_cdm\_application\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appDescription

</td><td id="app-descr">

Description of the application.Data type: String

</td></tr><tr><td>

appManagedByGroups

</td><td>

Comma-separated list of sys\_ids of the groups that manage the application. The calling user must belong to these groups. Located in the Group \[sys\_user\_group\] table.Data type: String

 ```
"appManagedByGroups": "sys_id, sys_id" 
```

</td></tr><tr><td>

appManufacturerId

</td><td id="app-mfct">

Sys\_id of the manufacturer. Located in the Company \[core\_company\] table.Data type: String

</td></tr><tr><td>

appModelOwnerId

</td><td id="app-owner-id">

Sys\_id of the application model owner. Located in the User \[sys\_user\] table.Data type: String

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
|200|Application successfully updated.|
|403|Forbidden. The user doesn't have permission to access the API.|
|404|Application not updated. The **message** property in the **result** object contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_z3v_z5d_gvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Error information. This parameter is only returned if the request failed.Data type: Object

 ```
"error": { 
   "message": "String", 
   "detail": "String" 
}
```

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failed.Data type: String

</td></tr><tr><td>

error.detail

</td><td>

Additional details about why the request failed.Data type: String

</td></tr><tr><td>

result

</td><td>

Result object containing information about the application.Data type: Object

 ```
"result": { 
   "message": "String", 
   "data": "String" 
}
```

</td></tr><tr><td>

result.message

</td><td>

Information about the successful or unsuccessful outcome of the request.Data type: String

</td></tr><tr><td>

result.data

</td><td>

Sys\_id of the application. Located in the CDM Application \[sn\_cdm\_application\] table.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request. This parameter is only returned if the request failed.Possible value: failure

 Data type: String

</td></tr></tbody>
</table>### cURL request

This example updates an existing application.

```
curl "https://instance.service-now.com/api/sn_devops_config/devops_config/application/38e17dc3473d111072566862736d43c7" \ 
--request PATCH \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"appDescription\": \"Updated description of Demo Application created from REST API\", 
  \"appManufacturerId\": \"262702654725d950a34a3085d36d435e\", 
  \"appModelOwnerId\": \"6816f79cc0a8016401c5a33be04be441\" 
}" \ 
--user 'username':'password' 
```

Response body.

```
{ 
  "result": { 
    "message": "Application with name Demo Application 1234 updated successfully.", 
    "data": "38e17dc3473d111072566862736d43c7" 
  } 
}
```

## DevOps Config - POST /devops\_config/application

Creates an application.

### URL format

Versioned URL: `/api/sn_devops_config/v1/devops_config/application`

Default URL: `/api/sn_devops_config/devops_config/application`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`.Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appDescription

</td><td id="app-descr">

Description of the application.Data type: String

</td></tr><tr><td>

appManagedByGroups

</td><td>

Comma-separated list of sys\_ids of the groups that manage the application. The calling user must belong to these groups. Located in the Group \[sys\_user\_group\] table.Data type: String

 ```
"appManagedByGroups": "sys_id, sys_id" 
```

</td></tr><tr><td>

appManufacturerId

</td><td id="app-mfct">

Sys\_id of the manufacturer. Located in the Company \[core\_company\] table.Data type: String

</td></tr><tr><td>

appModelId

</td><td>

Sys\_id of an existing application model to use to create the application. Located in the Application Model \[cmdb\_application\_product\_model\] table.If this parameter is provided, don't provide the **appName**, **appModelName**, **appServiceName**, **appServiceId**, or **technicalServiceId** parameters.

 Data type: String

</td></tr><tr><td>

appModelName

</td><td>

Name of an existing application model to use to create the application. Located in the Application Model \[cmdb\_application\_product\_model\] table.If this parameter is provided, don't provide the **appName**, **appModelId**, **appServiceName**, **appServiceId**, or **technicalServiceId** parameters.

 Data type: String

</td></tr><tr><td>

appModelOwnerId

</td><td id="app-owner-id">

Sys\_id of the application model owner. Located in the User \[sys\_user\] table.Data type: String

</td></tr><tr><td>

appName

</td><td>

Name of the application.Don't use the same name as any existing application.

 If this parameter is provided, don't provide the **appModelName**, **appModelId**, **appServiceName**, **appServiceId**, or **technicalServiceId** parameters.

 Data type: String

</td></tr><tr><td>

appServiceId

</td><td>

Sys\_id of an existing application service to use to create the application. Located in the Application Service \[cmdb\_ci\_service\_auto\] table. Use this parameter only when the **type** is `application`.

 If this parameter is provided, don't provide the **appName**, **appModelName**, **appModelId**, **appServiceName**, or **technicalServiceId** parameters.

 Data type: String

</td></tr><tr><td>

appServiceName

</td><td>

Name of an existing application service to use to create the application. Located in the Application Service \[cmdb\_ci\_service\_auto\] table. Use this parameter only when the **type** is `application`.

 If this parameter is provided, don't provide the **appName**, **appModelName**, **appModelId**, **appServiceId**, or **technicalServiceId** parameters.

 Data type: String

</td></tr><tr><td>

technicalServiceId

</td><td>

Sys\_id of an existing dynamic CI group to use to create the application. Located in the Dynamic CI Group \[cmdb\_ci\_query\_based\_service\] table. Use this parameter only when the **type** is `infrastructure`.

 If this parameter is provided, don't provide the **appName**, **appModelName**, **appModelId**, **appServiceName**, or **appServiceId** parameters.

 Data type: String

</td></tr><tr><td>

type

</td><td>

Required. The type of application to create.Valid values:

-   application
-   infrastructure

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

|Status code|Description|
|-----------|-----------|
|201|Application successfully created.|
|403|Forbidden. The user doesn't have permission to access the API.|
|404|Application not created. The **message** property in the **result** object contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_z3v_z5d_gvb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Error information. This parameter is only returned if the request failed.Data type: Object

 ```
"error": { 
   "message": "String", 
   "detail": "String" 
}
```

</td></tr><tr><td>

error.message

</td><td>

Error message containing the reason the request failed.Data type: String

</td></tr><tr><td>

error.detail

</td><td>

Additional details about why the request failed.Data type: String

</td></tr><tr><td>

result

</td><td>

Result object containing information about the application.Data type: Object

 ```
"result": { 
   "message": "String", 
   "data": "String" 
}
```

</td></tr><tr><td>

result.message

</td><td>

Information about the successful or unsuccessful outcome of the request.Data type: String

</td></tr><tr><td>

result.data

</td><td>

Sys\_id of the application. Located in the CDM Application \[sn\_cdm\_application\] table.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the request. This parameter is only returned if the request failed.Possible value: failure

 Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a new application.

```
curl "https://instance.service-now.com/api/sn_devops_config/devops_config/application" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"type\": \"application\", 
  \"appName\": \"Demo Application 1234\", 
  \"appDescription\": \"Description of Demo Application created from REST API\", 
  \"appManufacturerId\": \"262702654725d950a34a3085d36d435e\", 
  \"appModelOwnerId\": \"6816f79cc0a8016401c5a33be04be441\" 
}" \ 
--user 'username':'password' 
```

Response body.

```
{ 
  "result": { 
    "message": "Application with name Demo Application 1234 created successfully.", 
    "data": "38e17dc3473d111072566862736d43c7" 
  } 
} 
```

