---
title: CdmApplicationsApi
description: The CdmApplicationsApi provides endpoints that enable you to uploadzoominsoftware.io/utah-devops/ configuration data to the component, collection, deployable, and component variable folders found in the DevOps Config Workspace UI. It also has endpoints that enable you to export deployable configuration data to your DevOps pipeline and manage shared components and shared applications.Deletes a specified Configuration Data Management \(CDM\) deployable.Removes the shared component usage reference from a specified Configuration Data Management \(CDM\) application.Returns the content associated with a specified configuration data export request.Returns the current status of the specified configuration data export request.Returns the list of shared components used by a specified application. You can also specify to only return those shared components that have a new version available.Returns a map of shared components and the applications that use them that are within a specified library.Returns the current status of the specified configuration data upload request.Creates a new deployable and automatically connects it to a specified Configuration Data Management \(CDM\) application.Creates one or more new deployables.Submits a request to export the current snapshot for a specified application and one or more deployables into the CDM Exporter Cache \[sn\_cdm\_exporter\_cache\] table.Associates the specified shared component to the application within a specified changeset.Submits a request to upload the passed-in configuration data for a specific component, within the system components folder, for the specified application.Uploads files as part of the Configuration Data Model \(CDM\) to the components folder.Submits a request to upload the passed-in configuration data under the vars folder, within the system components folder, for the specified application.Submits a request to upload the passed-in configuration data for a specific collection, within the system collections folder, for the specified application.Uploads a file to the collections folder in the Configuration Data Model \(CDM\).Submits a request to upload the configuration content for a specific deployable within the deployables system folder of a specified application.Uploads files to the deployables folder in the Configuration Data Model \(CDM\).Updates the specified shared component in an application within a specified changeset.Need proper description.Updates the specified shared component in an application within a specified changeset.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 92
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmApplicationsApi

The CdmApplicationsApi provides endpoints that enable you to `uploadzoominsoftware.io/utah-devops/`configuration data to the component, collection, deployable, and component variable folders found in the DevOps Config Workspace UI. It also has endpoints that enable you to export deployable configuration data to your DevOps pipeline and manage shared components and shared applications.

The export and upload endpoints use an asynchronous queuing implementation. With this type of implementation, you first call the desired export or upload request endpoint. These endpoints queue your request and return a request identifier. You then use this request identifier to call the appropriate status endpoint, one for uploads and a different one for exports, to obtain the status of the upload/export. For export requests, once the export is complete, you can also request the content of the export.

This API does not provide endpoints that perform simple retrieval of application records. To retrieve these records, use the [Table](c_TableAPI.md#) API.

You must have one of the following roles to access this API:

-   Scripted REST CDM View ACL \(sn\_cdm.cdm.viewer\)
-   Scripted REST CDM Editor ACL \(sn\_cdm.cdm\_editor\)

In addition, the Configuration Data Management \(CDM\) plugin must be activated for this API to be available in an instance.

For additional information on Configuration Data Management and the DevOps Config Workspace UI, see [Uploading your config data](https://www.servicenow.com/docs/access?context=cdm-upload-process&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

For additional information on shared components and shared libraries, see [Sharing components among applications — Component libraries](https://www.servicenow.com/docs/access?context=cdm-component-libraries&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmApplicationsApi - DELETE /sn\_cdm/applications/deployables

Deletes a specified Configuration Data Management \(CDM\) deployable.

The caller of this endpoint must have the CDM Admin role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables`

Default URL: `/api/sn_cdm/applications/deployables`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the CDM application to which the deployable is associated.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

name

</td><td>

Name of the deployable to delete.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

|Name|Description|
|----|-----------|
|None||

### cURL request

The following code example shows how to remove a deployable.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/deployables?appName=testApp&name=Dep-1" \ 
--request DELETE \ 
--header "Accept:application/json" \ 
--user 'username':'password1' 
```

For a successful deletion of the deployable, no response is returned other than the HTTP status code.

```
None - results defined by the HTTP status code
```

## CdmApplicationsApi - DELETE /sn\_cdm/applications/shared\_components

Removes the shared component usage reference from a specified Configuration Data Management \(CDM\) application.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/shared_components`

Default URL: `/api/sn_cdm/applications/shared_components`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the application from which to remove the specified shared component association. The specified application must have the type field set to "shared\_library".Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

changesetNumber

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

sharedComponentName

</td><td>

Required. Unique name of the shared component to remove from the specified application.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Empty. The HTTP status code indicates the result of the call.

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to delete the "paymentService-V1.1" shared component from the "App1" application.

```
curl "https://instance-name.service-now.com/api/sn_cdm/applications/shared_components?appName=App1&sharedComponentName=paymentService-V1.1&changesetNumber=Chset-25" \ 
--request DELETE \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Response:

```
""
```

## CdmApplicationsApi - GET /sn\_cdm/applications/deployables/exports/\{export\_id\}/content

Returns the content associated with a specified configuration data export request.

Only call this endpoint once you have received a `complete` response from the [CdmApplicationsApi - GET /sn\_cdm/applications/deployables/exports/\{export\_id\}/status](applications-api.md#) endpoint. If you call this endpoint before the export is complete, a 400 status error is returned.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables/exports/{export_id}/content`

Default URL: `/api/sn_cdm/applications/deployables/exports/{export_id}/content`

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

export\_id

</td><td>

Unique identifier for the export request whose configuration data to return. This value is returned by the [CdmApplicationsApi - POST /sn\_cdm/applications/deployables/exports](applications-api.md#) endpoint.

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td>

Description of the errors encountered during export.Data type: String

</td></tr><tr><td>

export\_id

</td><td>

Export request ID. Same as that passed into the endpoint.Data type: String

</td></tr><tr><td>

exporter\_result

</td><td>

Content of the specified configuration data export.Data type:

-   JSON object: If the request was to export data in JSON format.
-   String: If the request was to export data in any other format.

</td></tr><tr><td>

request\_id

</td><td>

Export request ID. Same as that passed into the endpoint.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the specified export.Possible values:

-   completed
-   error
-   in\_progress
-   new
-   ready

Data type: String

Table: In state column of the CDM Request Queue \[sn\_cdm\_request\_queue\] table.

</td></tr></tbody>
</table>### cURL request

The following example requests the configuration data of an export request with the ID of 3ab14a7d53b1301096edddeeff7b12f.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/deployables/exports/3ab14a7d53b1301096edddeeff7b12f/content" \ 
--request GET \ 
--header "Accept:application/json" \
--user 'username':'password' 
```

The following shows the possible return results.

```
// Successful completion of the export request
{ 
  "result": { 
    "export_id": "3ab14a7d53b1301096edddeeff7b12f" 
    "exporter_result": "DEP1.COMP.cdi_1=cdi-1-value" 
  } 
}

// Response when an incorrect export_id is passed. Note: Status code is 200.
{ 
  "result": { 
    "request_id": "3ab14a7d53b1301096edddeeff7b12e", 
    "state": "error", 
    "errors": "Invalid requestId '3ab14a7d53b1301096edddeeff7b12fe'", 
    "export_id": "3ab14a7d53b1301096edddeeff7b12e" 
  } 
}
```

## CdmApplicationsApi - GET /sn\_cdm/applications/deployables/exports/\{export\_id\}/status

Returns the current status of the specified configuration data export request.

Use the [CdmApplicationsApi - POST /sn\_cdm/applications/deployables/exports](applications-api.md#) endpoint to make an export request.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables/exports/{export_id}/status`

Default URL: `/api/sn_cdm/applications/deployables/exports/{export_id}/status`

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

export\_id

</td><td>

Sys\_id of the export request whose status to return. This value is returned by the [CdmApplicationsApi - POST /sn\_cdm/applications/deployables/exports](applications-api.md#) endpoint.

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td>

Description of the errors encountered during export.Data type: String

</td></tr><tr><td>

export\_id

</td><td>

Export request ID. Same as that passed into the endpoint.Data type: String

</td></tr><tr><td>

exporter\_result

</td><td>

Details about the associated error.Data type: Object

</td></tr><tr><td>

exporter\_result.errors

</td><td>

Description of the error\(s\) encountered during export.Data type: Array

</td></tr><tr><td>

exporter\_result.execution\_id

</td><td>

Unique identifier for the exporter execution record.Data type: String

Table: CDM Exporter Execution \[sn\_cdm\_exporter\_execution\]

</td></tr><tr><td>

exporter\_result.state

</td><td>

Current state of the specified export.Possible values:

-   complete
-   error
-   in\_progress
-   new

Data type: String

Table: CDM Exporter Execution \[sn\_cdm\_exporter\_execution\]

</td></tr><tr><td>

request\_id

</td><td>

Export request ID. Same as that passed into the endpoint.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the specified export.Possible values:

-   completed
-   error
-   in\_progress
-   new
-   ready

Data type: String

Table: In state column of the CDM Request Queue \[sn\_cdm\_request\_queue\] table.

</td></tr></tbody>
</table>### cURL request

The following example requests the status of an export with the ID of 3ab14a7d53b1301096edddeeff7b12f.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/deployables/exports/3ab14a7d53b1301096edddeeff7b12f/status" \ 
--request GET \ 
--header "Accept:application/json" \
--user 'username':'password' 
```

The following are the possible return results.

```
// Successful completion of the export request
{ 
  "result": { 
    "state": "completed", 
    "export_id": "3ab14a7d53b1301096edddeeff7b12f0" 
  } 
}

// Response when an incorrect export_id is passed. Note: Status code is 200.
{ 
  "result": { 
    "request_id": "3ac8e1b05311301096edddeeff7b123c", 
    "state": "error", 
    "errors": "Invalid requestId '3ac8e1b05311301096edddeeff7b123c'", 
    "export_id": "3ac8e1b05311301096edddeeff7b123c" 
  } 
} 

// Response when the export encounters an error. The exporter_result array contains the error information. Note: Status code is 200.
{ 
  "result": { 
    "state": "completed", 
    "export_id": "24536c3353f9301096edddeeff7b12b1", 
    "exporter_result": { 
      "execution_id": "81536c3353f9301096edddeeff7b129e", 
      "state": "failure", 
      "errors": [ 
        "Snapshot 'SNA-001-published-non_compliant' has not passed validation. All snapshots of deployable '/ApplicationA/deployables/DEP3' are required to pass validation" 
      ] 
    } 
  } 
}
```

## CdmApplicationsApi - GET /sn\_cdm/applications/shared\_components

Returns the list of shared components used by a specified application. You can also specify to only return those shared components that have a new version available.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/shared_components`

Default URL: `/api/sn_cdm/applications/shared_components`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the application whose list of shared components you want returned. The type field of the application must be set to shared\_library.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

withUpdatesOnly

</td><td>

Flag that indicates whether to only return shared components that have a new updated version available.Valid values:

-   true: Only return shared components that have a new updated version available.
-   false: Return all shared components used by the specified application.

Default: false

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

currentVersion

</td><td>

Current version of the CDM application. Data type: Number \(Integer\)

</td></tr><tr><td>

currentVersionName

</td><td>

Name of shared component version currently in use.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of shared component.Data type: String

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

name

</td><td>

Unique name of the shared component.Data type: String

</td></tr><tr><td>

sharedLibraryName

</td><td>

Name of shared library to which the shared component belongs.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr><td>

updateVersionName

</td><td>

Name of shared component version available for update.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to retrieve the shared components that have a new version used by "App1".

```
curl "https://instance-name.service-now.com/api/sn_cdm/applications/shared_components?updatesOnly=true&appName=App1" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Response:

```
{ 
  "result": [
    {
      "name": "Component_Name",
      "description": "”,
      "sharedLibraryName": "Shared Library",
      "currentVersion": "2",
      "currentVersionName": "Component_A-v2.shc",
      "updateVersionName": "Component_A-v3.shc"
    } 
  ]
}
```

## CdmApplicationsApi - GET /sn\_cdm/applications/shared\_libraries/components/applications

Returns a map of shared components and the applications that use them that are within a specified library.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/shared_libraries/components/applications`

Default URL: `/api/sn_cdm/applications/shared_libraries/components/applications`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sharedComponentName

</td><td>

Required. Name of the shared component to include in the map.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library to include in the map. The specified application must have the type field set to "shared\_library".Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of application using shared component Data type: String

</td></tr><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

managed\_by\_group

</td><td>

Comma-separated list of sys\_ids of the groups that can manage the application.Data type: String

</td></tr><tr><td>

name

</td><td>

Unique name of the application using the component.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the application utilizing the shared component.Data type: String

</td></tr></tbody>
</table>### cURL request

The following code example shows how to call this endpoint to retrieve the map that shows the applications in the "OracleG-Library-10" shared library that use the "paymentService-V1.1" shared component.

```
curl "https://instance-name.service-now.com/api/sn_cdm/applications/shared_libraries/components/applications?sharedLibraryName=OracleG-Library-10&sharedComponentName=paymentService-V1.1" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Response:

```
{
  "result": {
    "component_name": [
      { 
        "name": "App Name",
        "description": "desc",
        "managed_by_group": null,
        "sys_id": "4e7808bb1b371110636e0fe0604bcb08"
      }, 
      {
        "name": "Config App",
        "description": "desc",
        "managed_by_group": null,
        "sys_id": "55a75cfb1b771110636e0fe0604bcb5c"
      },
      {
        "name": "Database App",
        "description": "desc",
        "managed_by_group": null,
        "sys_id": "2eb7503f1b771110636e0fe0604bcb06"
      }
    ]
  } 
}
```

## CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}

Returns the current status of the specified configuration data upload request.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/upload-status/{upload_id}`

Default URL: `/api/sn_cdm/applications/upload-status/{upload_id}`

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

upload\_id

</td><td>

Sys\_id of the upload request whose status to return. This value is returned by the various CdmApplications upload request endpoints.

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

errors

</td><td>

Description of the error\(s\) encountered during upload.Data type: String

</td></tr><tr><td>

output

</td><td>

Description of the uploaded data or if an error occurred during the upload, an error message describing the error that was encountered.Data type: Array of String

```
"output": {
  "auto_validate": "String",
  "cdm_application": "String",
  "committed_at": "String",
  "committed_by": "String",
  "description": "String",
  "last_conflict_detection_time": "String",
  "number": "String",
  "publish_option": "String",
  "snapshot_description": "String",
  "snapshot_name": "String",
  "state": "String",
  "sys_created_by": "String",
  "sys_id": "String",
  "title": "String"
}
```

</td></tr><tr><td>

output.auto\_validate

</td><td>

Indicates whether to invoke validation after the commit.Data type: String

</td></tr><tr><td>

output.cdm\_application

</td><td>

Name of application under which the upload was performed.Data type: String

</td></tr><tr><td>

output.committed\_at

</td><td>

Date and time that the uploaded content was committed.Data type: String

</td></tr><tr><td>

output.committed\_by

</td><td>

Sys\_id of the record of the entity that performed the commit.Data type: String

</td></tr><tr><td>

output.description

</td><td>

Not currently used.Data type: String

</td></tr><tr><td>

output.last\_conflict\_detection\_time

</td><td>

Date and time conflict detection invocation.Data type: String

</td></tr><tr><td>

output.number

</td><td>

Unique number of the changeset.Data type: String

</td></tr><tr><td>

output.publish\_option

</td><td>

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

 **Note:** This option is only available if the value for the **autoCommit** parameter is true.

</td></tr><tr><td>

output.snapshot\_description

</td><td>

Description of the associated snapshot.Data type: String

</td></tr><tr><td>

output.snapshot\_name

</td><td>

Name of the associated snapshot.Data type: String

</td></tr><tr><td>

output.state

</td><td>

State of the upload content.Possible values:

-   blocked
-   checking\_for\_conflict
-   commit\_failed
-   commit\_in\_progress
-   committed
-   open

Data type: String

</td></tr><tr><td>

output.sys\_created\_by

</td><td>

Sys\_id of the entity that created the record.Data type: String

</td></tr><tr><td>

output.sys\_id

</td><td>

Sys\_id of the record containing the changeset.Data type: String

</td></tr><tr><td>

output.title

</td><td>

Title of changeset created as part of the upload.Data type: String

</td></tr><tr><td>

processing\_state

</td><td>

Current processing state of the upload request.Possible values:

-   NOT\_PROCESSED
-   PROCESSED

Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the upload request.Possible values:

-   completed
-   error
-   in\_progress
-   new
-   ready

</td></tr><tr><td>

type

</td><td>

Type of upload request.Possible values:

-   commit
-   upload\_and\_commit

Data type: String

</td></tr><tr><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example show requesting the status for an upload with the ID of 5560a6895326301096edddeeff7b1230.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/upload-status/5560a6895326301096edddeeff7b1230" \ 
--request GET \ 
--header "Accept:application/json" \
--user 'username':'password' 
```

The following are the possible return results.

```
// Successful completion of the upload request
{ 
  "result": { 
    "type": "upload_and_commit", 
    "state": "completed", 
    "output": { 
      "sys_id": "be681dc95362301096edddeeff7b12ba", 
      "number": "Chset-102", 
      "title": "admin2021-09-10 08:09:07", 
      "description": null, 
      "committed_at": "2021-09-10 20:23:37", 
      "committed_by": "6816f79cc0a8016401c5a33be04be441", 
      "sys_created_by": "admin", 
      "state": "committed", 
      "publish_option": "publish_none", 
      "auto_validate": false, 
      "snapshot_name": null, 
      "snapshot_description": null, 
      "cdm_application": "Demo_App1631126164773", 
      "last_conflict_detection_time": "1631305417894" 
    }, 
    "processing_state": "PROCESSED", 
    "upload_id": "5560a6895326301096edddeeff7b1230"
  } 
}

// Response when an incorrect upload_id is passed. Note: Status code is 200.
{ 
  "result": { 
    "state": "error", 
    "errors": "Invalid requestId '5560a6895326301096edddeeff7b1240'", 
    "upload_id": "5560a6895326301096edddeeff7b1240" 
  } 
} 

// Response when the upload encounters an error. The exporter_result array contains the error information. Note: Status code is 200.
{ 
  "result": { 
    "type": "upload_and_commit", 
    "state": "error", 
    "output": "Error encountered during execution of request.\nError: Node 'dbSettings' of type 'sg_cdm_node_component' cannot create child 'dbSettings' of type 'sg_cdm_node_folder'", 
    "processing_state": "PROCESSED", 
    "upload_id": "272f8a415326301096edddeeff7b1232" 
  } 
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/deployables

Creates a new deployable and automatically connects it to a specified Configuration Data Management \(CDM\) application.

You can create a deployable for any one of three environment types: Development, Test, or Production.

To access this endpoint the caller must have the CDM Admin role.

If you need to create multiple deployables, use the [CdmApplicationsApi - POST /sn\_cdm/applications/deployables/create](applications-api.md#) endpoint.

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables`

Default URL: `/api/sn_cdm/applications/deployables`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of an existing, active CDM application to associate with the deployable.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

envType

</td><td id="cdm_apps-envType-entry">

Required. Environment type for the deployable.

Valid values \(case-sensitive\):

-   Development
-   Production
-   Test

**Note:** The deployable environment type can't be changed after creation.

Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the CDM deployable.Should not be more than 255 chars. Default allowed characters are 0-9, A-Z, a-z, \_,-,., %, $, whitespace, :, \#.

 Data type: String

 Maximum length: 255 characters

 Allowable characters: 0-9, A-Z, a-z, \_, -, ., %, $, whitespace, :, and \#

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

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
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_dkr_tdn_qtb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cdi\_count

</td><td>

Number of configuration data items \(CDIs\) contained in the associated CDM application.Data type: Number \(Integer\)

</td></tr><tr><td>

cdi\_usage

</td><td>

Percentage of the CDIs used by the deployable.Data type: Number \(Integer\)

</td></tr><tr><td>

cdm\_app

</td><td>

CDM application object associated with the deployable.Data type: Object

```
"cdm_app": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_app.link

</td><td id="cdm_app_link-app-entry">

Call to use to access the CDM application record using the REST Table API. Data type: String

</td></tr><tr><td>

cdm\_app.value

</td><td id="cdm_app_value-app-entry">

Sys\_id of the associated CDM application record.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

cdm\_ci

</td><td>

Application service object associated with the deployable.Data type: Object

```
"cdm_ci": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_ci.link

</td><td>

Call to use to access the application service record using the REST Table API.Data type: String

</td></tr><tr><td>

cdm\_ci.value

</td><td>

Sys\_id of the associated application service record. Data type: String

Table: Configuration Item \[cmdb\_ci\]

</td></tr><tr><td>

description

</td><td>

Description of the generated CDM deployable.Data type: String

</td></tr><tr><td>

environment\_type

</td><td>

Environment type of the deployable.Possible values:

-   Development
-   Production
-   Test

Data type: String

</td></tr><tr><td>

error

</td><td id="cdm_apps-error-entry">

Only returned if an error occurred during processing.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the CDM deployable.Data type: String

</td></tr><tr><td>

node

</td><td>

Details about the deployable node.Data type: Object

```
"node": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

node.link

</td><td>

Call to use to access the deployable node record using the REST Table API. Data type: String

</td></tr><tr><td>

node.value

</td><td>

Sys\_id of the deployable node record.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

snapshot\_version\_counter

</td><td>

Number of snapshots created for the deployable.Data type: Number \(Integer\)

</td></tr><tr><td>

state

</td><td>

Current state of the deployable.Possible values:

-   active
-   deleted

Data type: String

</td></tr><tr id="cdm_dep-sys_created_by-row"><td>

sys\_created\_by

</td><td>

User name of the user that created the CDM deployable. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_deps-sys_created_on-row"><td>

sys\_created\_on

</td><td>

Date and time when the CDM deployable was created.Data type: String

Format: YYYY-mm-DD hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the created deployable.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr id="cdm_dep-sys_updated_by-row"><td>

sys\_updated\_by

</td><td>

User name of the user that last updated the CDM deployable. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_dep-sys_updated_on-row"><td>

sys\_updated\_on

</td><td>

Date and time when the CDM deployable was last updated.Data type: String

Format: YYYY-mm-DD hh:mm:ss

</td></tr></tbody>
</table>### cURL request

The following code example shows how to create and associate a deployable to a CDM application.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/deployables?name=Dep-1&returnFields=name%2Csys_id%2Cstate&appName=testApp&envType=Test" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user 'username':'password1' 
```

Return results:

```
{ 
  "result": [ 
    { 
      "cmdb_ci": { 
        "value": "f5b9e00b53901110a1d3ddeeff7b12b8", 
        "link": "http://192.168.0.233:8080/api/now/table/cmdb_ci_service_auto/f5b9e00b53901110a1d3ddeeff7b12b8" 
      }, 
      "cdi_count": "0", 
      "snapshot_version_counter": "0", 
      "description": null, 
      "sys_updated_on": "2022-06-29 12:53:57", 
      "environment_type": "Test", 
      "node": { 
        "value": "7db9e00b53901110a1d3ddeeff7b12b6", 
        "link": "http://192.168.0.233:8080/api/now/table/sn_cdm_node/7db9e00b53901110a1d3ddeeff7b12b6" 
      }, 
      "sys_id": "39b9e00b53901110a1d3ddeeff7b12b7", 
      "sys_updated_by": "admin", 
      "cdm_app": { 
        "value": "62b517a953b70110a1d3ddeeff7b128c", 
        "link": "http://192.168.0.233:8080/api/now/table/sn_cdm_application/62b517a953b70110a1d3ddeeff7b128c" 
      }, 
      "sys_created_on": "2022-06-29 12:53:57", 
      "cdi_usage": "0", 
      "name": "Dep-2", 
      "state": "active", 
      "sys_created_by": "admin" 
    } 
  ] 
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/deployables/create

Creates one or more new deployables.

You can create one of two types of deployables:

-   Deployables that must be manually connected to an Application Model \(CI Service\).
-   Deployables that are automatically connected to new, dynamically created Application Models \(CI Services\).

You can create a deployable for any one of three environment types: Development, Test, or Production. When creating multiple deployables, the auto-generated names of the deployables follow the pattern: `DeployableType_Number`, where `Number` is a running sequence number based on the creation of a new deployable. For example, if you create three deployables of type `Test` in an endpoint call, they are named Test\_1, Test\_2, and Test\_3. If you then call the endpoint again, and create a different Test deployable, its auto-gen'd name is Test\_4. These numbers are never reused, even if a deployable is deleted.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables/create`

Default URL: `/api/sn_cdm/applications/deployables/create`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appSysId

</td><td>

Required. Sys\_id of an active CDM Application to associate with the deployables.Data type: String

</td></tr><tr><td>

autoConnect

</td><td>

Required. Flag that determines whether to automatically connect the newly created deployables to dynamically generated Application Models.Valid values:

-   true: Connect the newly created deployables to dynamically generated Application Models.
-   false: Just create the deployables. These deployables must be manually mapped to Application Models using the UI.

 Data type: Boolean

</td></tr><tr><td>

envType

</td><td id="cdm_apps-envType-entry">

Required. Environment type for the deployable.

Valid values \(case-sensitive\):

-   Development
-   Production
-   Test

**Note:** The deployable environment type can't be changed after creation.

Data type: String

</td></tr><tr><td>

quantity

</td><td>

Required. Number of deployables to create.Data type: Number

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

result

</td><td>

Sys\_ids of the created deployables.Data type: Array

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a single deployable and associate it with and existing CDM application.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/deployables/create?envType=Production&appSysId=5e118055b712011054c1e5a6ce11a9d4&quantity=5&autoConnect=true" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

The following shows the possible responses to this call, both as a success and an error.

```
// Successful completion of the upload request
{
  "result": [
    "8ba43a3db7d6011054c1e5a6ce11a9a4",
    "93a47a3db7d6011054c1e5a6ce11a90d",
    "dba47a3db7d6011054c1e5a6ce11a91d",
    "6fa47a3db7d6011054c1e5a6ce11a921",
    "efa47a3db7d6011054c1e5a6ce11a925"
  ]
} 

// Error response
{
  "error": {
    "message": "Error: CDM Application with SysID 5e118055b712011054c1e5a6ce11a9d1 was not found. (sys_script_include.8cf0fbf453626010a1d3ddeeff7b12fe.script; line 211)",
    "detail": ""
  },
  "status": "failure"
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/deployables/exports

Submits a request to export the current snapshot for a specified application and one or more deployables into the CDM Exporter Cache \[sn\_cdm\_exporter\_cache\] table.

This endpoint returns a unique identifier for the request, which you then use to call the [CdmApplicationsApi - GET /sn\_cdm/applications/deployables/exports/\{export\_id\}/status](applications-api.md#) endpoint to retrieve the status of the export. Once the export is complete, you can use the [CdmApplicationsApi - GET /sn\_cdm/applications/deployables/exports/\{export\_id\}/content](applications-api.md#) endpoint to retrieve the associated application's configuration data.

A snapshot is the complete data model of a deployable at the time a configuration change is committed. This includes any included components, collections, and vars, as well as deployable-specific vars and overrides. For additional information on deployables, see [Create and update a deployable](https://www.servicenow.com/docs/access?context=cdm-deployable-define&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Note:** Snapshots cannot exceed 10,000 configuration data items \(CDIs\) per deployable or 100,000 CDIs per application.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables/exports`

Default URL: `/api/sn_cdm/applications/deployables/exports`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

additionalDeployables

</td><td>

Non-primary deployables to export.Data type: Array of Objects

```
"additionalDeployables": [
  {
    "app_name": "String",
    "deployable_name": "String"
  }
]
```

For example: `[{'app_name':'TestApp', "deployable_name:'DEP-1'}]`

Default: Empty array - \[\]

</td></tr><tr><td>

additionalDeployables.app\_name

</td><td>

Required if **additionalDeployables** array is specified. Name of the application associated with the deployable whose configuration data you want to export.Data type: String

</td></tr><tr><td>

additionalDeployables.deployable\_name

</td><td>

Required if **additionalDeployables** array is specified. Name of the non-primary deployable whose configuration data you want to export.Data type: String

</td></tr><tr><td>

appName

</td><td>

Required. Name of the application whose configuration data you want to export.Data type: String

</td></tr><tr><td>

args

</td><td>

A JSON object containing key-value pairs for custom arguments.Data type: Object

</td></tr><tr><td>

dataFormat

</td><td>

Output format of the exported data.Valid values \(case-sensitive\):

-   ini
-   json
-   properties
-   raw \(Data is returned in String format\)
-   xml
-   yaml

Data type: String

Default: json

</td></tr><tr><td>

deployableName

</td><td>

Required. Name of the deployable whose configuration data you want to export.Data type: String

</td></tr><tr><td>

exporterName

</td><td>

Required. Name of the exporter to use to export the snapshot data. Exporters are custom to the implementer. For details on creating a custom exporter, see [Create a custom exporter](https://www.servicenow.com/docs/access?context=cdm-exporter-create-custom&version=australia&pubname=australia-it-service-management&ft:locale=en-US).Data type: String

</td></tr><tr><td>

restrictExport

</td><td>

Flag that indicates whether the endpoint validates snapshots when exporting the data.Valid values:

-   true: Validate snapshots.
-   false: Don't validate snapshots.

Data type: Boolean

Default: false

</td></tr><tr><td>

snapshotName

</td><td>

Name of the snapshot to export. This can only be one of the snapshot names associated with the deployable as specified in the **deployableName** or **additionalDeployables.deployable\_name** parameters. Default: The endpoint exports the latest published snapshot. If there is not a published snapshot, the system throws the error “Failed to find latest published snapshot for deployable '\{0\}'”

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

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

Bad Request. A bad request type or malformed request was detected.Possible error messages:

-   Error: Missing required param 'appName'
-   Error: User does not have necessary permission to create Export request
-   Error: Invalid Boolean value \(&lt;xyz&gt;\).

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

Details about the error that occurred.Data type: Array

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr><td>

export\_id

</td><td>

Unique identifier of the export request. Use this ID when calling the [CdmApplicationsApi - GET /sn\_cdm/applications/deployables/exports/\{export\_id\}/status](applications-api.md#) endpoint to check the current status of the export request.Data type: String

</td></tr><tr><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example requests the export of the configuration data for the following: application name = TestAppA, deployable name = DEP, using the exporter = exporter-1-primary\_deployable.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/deployables/exports?appName=TestAppA&args=%7B%22arg_A_required%22%20%3A%20%22value%20A%22%7D&exporterName=exporter-1-primary_deployable&deployableName=DEP1" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

Returns the unique identifier of the export request.

```
{ 
  "result": {
    "export_id": "64b5f79f5379301096edddeeff7b12eb" 
  } 
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/shared\_components

Associates the specified shared component to the application within a specified changeset.

The CDM Admin role is required to access this endpoint.

**Note:** The specified shared component must have an associated published version \(snapshot\).

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/shared_components`

Default URL: `/api/sn_cdm/applications/shared_components`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the application to associate with the shared component.Data type: String

</td></tr><tr><td>

changesetNumber

</td><td>

Required. Unique identifier of the changeset associated with the component.Data type: String

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr><tr><td>

sharedComponentName

</td><td>

Required. Name of the shared component to associate with the specified application.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library under which to create the component. The shared library must have the following fields defined as follows:-   state = active
-   available = true
-   type = shared\_library

Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. The passed changeset doesn't exist.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

The response fields depend on what fields were specified in the **returnFields** parameter in the request. The following describes some of the more important fields.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeset\_id

</td><td id="changeset-node-editor-entry">

Details of the changeset record associated with the node. Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

changeset\_id.link

</td><td id="changeset_link-node-editor-entry">

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr><td>

changeset\_id.value

</td><td id="changeset_value-node-editor-entry">

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

description

</td><td>

Description of the CDM node.Data type: String

</td></tr><tr><td>

error

</td><td id="cdm_apps-error-entry">

Only returned if an error occurred during processing.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="cdm_apps-error_detail-entry">

Details about the error that occurred.Data type: String

</td></tr><tr><td>

error.message

</td><td id="cdm_apps-error_message-entry">

Message that provides an overview of the error.Data type: String

</td></tr><tr><td>

linked\_to

</td><td>

ID of the main node associated with the shared component.Data type: String

</td></tr><tr><td>

linked\_to\_version

</td><td>

Details of the CDM snapshot record associated with the node. Data type: Object

```
"linked_to_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

linked\_to\_version.link

</td><td>

Call syntax for querying this version record using the Table REST API.Data type: String

</td></tr><tr><td>

linked\_to\_version.value

</td><td>

Sys\_id of the version record.Data type: String

</td></tr><tr><td>

main

</td><td>

Flag that indicates whether the associated snapshot was published.

 Valid values:

-   true: Snapshot was published.
-   false: Snapshot wasn't published.

</td></tr><tr><td>

main\_id

</td><td>

Unique ID of the newly created main node.Data type: String

</td></tr><tr><td>

main\_id\_encoded

</td><td>

Encoded ID of the newly created main node.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the CDM node.Data type: String

</td></tr><tr><td>

node

</td><td>

Sys\_id of the shared component node.Data type: String

</td></tr><tr><td>

node\_path

</td><td>

Path to the new linked node created when adding the shared component. Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the node.Possible values: New

Data type: String

</td></tr><tr id="cdm_dep-sys_created_by-row"><td>

sys\_created\_by

</td><td>

User name of the user that create the CDM node. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_deps-sys_created_on-row"><td>

sys\_created\_on

</td><td>

Date and time when the CDM node was created.Format: YYYY-mm-DD hh:mm:ss

Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="sys_id-node-editor-entry">

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr id="cdm_dep-sys_updated_by-row"><td>

sys\_updated\_by

</td><td>

User name of the user that last updated the CDM node. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_dep-sys_updated_on-row"><td>

sys\_updated\_on

</td><td>

Date and time when the CDM node was last updated.Format: YYYY-mm-DD hh:mm:ss

Data type: String

</td></tr><tr><td>

type

</td><td>

Node type.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to associate the application "App1" with the shared component "paymentService-V1.1" under the shared library "OracleG-Library-10" within the "Chset-20" changeset.

```
curl "https://instance.servicenow.com/api/sn_cdm/applications/shared_components?appName=App1&changesetNumber=Chset-20&sharedLibraryName=OracleG-Library-10&sharedComponentName=paymentService-V1.1" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Response:

```
{ 
  "result": { 
    "changeset_id": { 
      "value": "74b7ff6fc33711100c257e2cc840dd6b", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/74b7ff6fc33711100c257e2cc840dd6b" 
    }, 
    "node_path": "!,0!,1!/D", 
    "description": null, 
    "sys_updated_on": "2022-12-22 17:07:29", 
    "type": "sn_cdm_node_linked_shared_component", 
    "sys_class_name": "sn_cdm_node", 
    "sys_id": "ff8b37ebc3b711100c257e2cc840ddba", 
    "sys_updated_by": "admin", 
    "previous_version": null, 
    "sys_created_on": "2022-12-22 17:07:29", 
    "value": null, 
    "effective_from": null, 
    "linked_to": "210", 
    "sys_created_by": "admin", 
    "restricted_to": null, 
    "linked_to_version": { 
      "value": "581fc3e9c3b311100c257e2cc840dd17", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_snapshot/581fc3e9c3b311100c257e2cc840dd17" 
    }, 
    "level": "2", 
    "conflict_type": null, 
    "main_id": "483",
    "effective_to": null,
    "secure_value": null, 
    "node_classifier": "/application/components", 
    "main_id_encoded": "/D",
    "name": "LIB2_C",
    "position": null,
    "reason_for_conflict": null,
    "system_folder": false,
    "status": "new",
    "conflict": false
  } 
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/uploads/components

Submits a request to upload the passed-in configuration data for a specific component, within the system components folder, for the specified application.

This endpoint returns the ID of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.

**Note:** The maximum default upload content size is 2 MB. You can modify this default by updating the property sn\_cdm.max\_allowed\_upload\_file\_size.

The following image shows an example of where the component configuration data is uploaded in reference to the ServiceNow DevOps Config UI. Assumes the component is **dbComponent** and the application is **paymentSvc**.

![Example configuration content location within UI](../image/apps-uploads-components_data.png)

**Note:** This upload method cannot be used to modify nodes. Use the alternative [CdmApplicationsApi - POST sn\_cdm/applications/uploads/components/file](applications-api.md#) method to modify nodes.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/uploads/components`

Default URL: `/api/sn_cdm/applications/uploads/components`

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
</table><table id="id_plp_1vh_psb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-appName-row"><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr id="cdm_apps-autoCommit-row"><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr id="cdm_apps-autoDelete-row"><td>

autoDelete

</td><td>

Flag that indicates whether the existing nodes, that aren’t part of the upload content, are deleted after the processing is complete.Valid values:

-   true: Automatically delete existing nodes.
-   false: Don't automatically delete existing nodes.

Data type: Boolean

Default: false

</td></tr><tr id="cdm_apps-autoValidate-row"><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr id="cdm_apps-changesetNumber-row"><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr id="cdm_apps-dataFormat-row"><td>

dataFormat

</td><td>

Required. Format of the configuration data.Valid values:

-   csv
-   ini
-   json
-   properties
-   raw
-   xml
-   yaml

Data type: String

</td></tr><tr id="cdm_app-dataFormAtt-row"><td>

dataFormatAttributes

</td><td id="cdm_app-dataFormAtt-entry">

Only supported when the **dataFormat** parameter is set to `csv`. Attributes that define the CSV data format. For additional information, see [Parsing of CSV files in CDM](https://www.servicenow.com/docs/access?context=cdm-parsing-csv-file&version=australia&pubname=australia-it-service-management&ft:locale=en-US).Data type: Object

```
"dataFormatAttributes" {
  "containsHeader": Boolean,
  "delimeter": "String"
  "headers": [Array],
  "securedHeaders": [Array]
}
```

</td></tr><tr id="cdm_app-dataFormAtt_containsHeaders-row"><td>

dataFormatAttributes.containsHeaders

</td><td id="cdm_app-dataFormAtt_containsHeaders-entry">

Flag that indicates whether the data contains a header row.Valid values:

-   true: Data contains a header row. The first row in the data is considered the header row.

![Header row example](../image/cdm_header_row_example.png)

-   false: Data doesn't contain a header row. You must pass the header information in the **dataFormatAttributes.headers** parameter.

Data type: Boolean

Default: false

</td></tr><tr id="cdm_app-dataFormAtt_delimeter-row"><td>

dataFormatAttributes.delimeter

</td><td id="cdm_app-dataFormAtt_delimeter-entry">

Character to use to delineate fields within the data.Data type: String

Default: Comma ","

</td></tr><tr id="cdm_app-dataFormAtt_headers-row"><td>

dataFormatAttributes.headers

</td><td id="cdm_app-dataFormAtt_headers-entry">

Required if **dataFormatAttributes.containsHeaders** parameter is `false`. Fields in the data that comprise the header. These headers are converted to the key names of the CDIs in the JSON format. The number of headers must match the number of record fields.Data type: Array

Default: Empty array

</td></tr><tr id="cdm_app-dataFormAtt_securedHeaders-row"><td>

dataFormatAttributes.securedHeaders

</td><td id="cdm_app-dataFormAtt_securedHeaders-entry">

Fields in the data that are secure fields and must be encrypted in the data uploaded to CDM. The name of the secured headers must match the name of the headers in the headers attribute or data file. These fields are stored in a column of type Password \(2 Way Encrypted\).**Note:** You can only secure fields using this attribute. You can't unsecure the secured fields.

Data type: Array

Default: Empty array

</td></tr><tr id="cdm_apps-deleteRedundantOverrides-row"><td>

deleteRedundantOverrides

</td><td>

Flag that indicates whether to create an override where redundant values are present.Valid values:

-   true: If redundant values are present, an override isn’t created.
-   false: If redundant values are present, proceeds with an override.

Default: true

</td></tr><tr id="cdm_apps-fileName-row"><td>

fileName

</td><td>

Name of the file to upload. This name can differ from than the actual file name and contain the file extension. For example, .txt/.scv/.jar. The fileName value is applied when downloading the file.Data type: String

</td></tr><tr id="cdm_apps-fileNodeName-row"><td>

fileNodeName

</td><td>

Name of the file node. This file name is used in the configuration data when exporting it. This name doesn’t require a file extension nor does it affect the download.Data type: String

</td></tr><tr id="cdm_apps-identifierKeys-row"><td>

identifierKeys

</td><td>

List of names that indicate which key in an array child to use to identify the same node.For example, if you’re uploading:

```
[
  {"name" : "Allan, "city" : "Paris"}, 
  {"name" : "Karen, "city" : "Sydney"}
]
```

in the following existing model:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"}
]
```

and you set **identifierKeys** to `name`, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Sydney"},
  {"name" : "Allan, "city" : "Paris"}
]
```

Otherwise, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"},
  {"name" : "Allan, "city" : "Paris"},
  {"name" : "Karen, "city" : "Sydney"}
]
```

Data type: Array of Strings

</td></tr><tr id="cdm_apps-ignoreAttributes-row"><td>

ignoreAttributes

</td><td>

Flag that indicates whether the given data format supports attributes \(currently only XML\).Valid values:

-   true: If the given data format supports attributes, any attributes in the input data are skipped during the upload.
-   false: If the given data format supports attributes, any attributes in the input data are included in the upload.

Data type: Boolean

Default: false

</td></tr><tr id="cdm_apps-namePath-row"><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr id="cdm_apps-sharedLibraryName-row"><td>

sharedLibraryName

</td><td>

Required. Name of the shared library where the component to delete is located.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|Variable upload data|Configuration data to upload. This can be any data in the format defined by the **dataFormat** parameter of the query parameters.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="id_trg_k25_2wb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **text/plain** and **application/x-www-form-urlencoded**.Default: **text/plain**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_vvq_4wh_psb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_b4z_nwh_psb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows an upload request for the application Demo\_App1631126164773.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/components?namePath=%2FSettings%2FdbSettings&dataFormat=json&appName=Demo_App1631126164773&changesetNumber=Chset-8&autoCommit=false&publishOption=publish_none&autoValidate=false&autoDelete=true" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "{
  \"dbIPAddress\": \"10.10.10.110\",
  \"dbPort\": \"8080\",
  \"dbConnectionString\": \"admin:admin server1.xyz.com:8080 dbName_payments\",
  \"dbConnectionStringBackup\": \"admin:admin server2.xyz.com dbName_payments_backup\
"}" \ 
--user 'username':'password' 
```

The following return results show both a successful and an error response for this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Size of uploaded data:6853632.0(bytes) is greater than max allowed upload limit of 2097152.0(bytes)", 
    "detail": "" 
  },
  "status": "failure"
}
```

## CdmApplicationsApi - POST sn\_cdm/applications/uploads/components/file

Uploads files as part of the Configuration Data Model \(CDM\) to the components folder.

Use this method to upload to a components file node.

### URL format

Versioned URL: `POST /api/sn_cdm/{api_version}/applications/uploads/components/file`

Default URL: `POST /api/sn_cdm/applications/uploads/components/file`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="table_rgl_tbt_byb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table id="cdm_app-upload_query_parms-table" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

fileName

</td><td>

Name of the file to upload. This name can differ from than the actual file name and contain the file extension. For example, .txt/.scv/.jar. The fileName value is applied when downloading the file.Data type: String

</td></tr><tr><td>

fileNodeName

</td><td>

Name of the file node. This file name is used in the configuration data when exporting it. This name doesn’t require a file extension nor does it affect the download.Data type: String

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

publishOption

</td><td id="publish_option-changeset-entry">

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

 **Note:** This option is only available if the value for the **autoCommit** parameter is true.

</td></tr></tbody>
</table><table id="table_j22_fgm_2yb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable upload data

</td><td>

Configuration data to upload. By default, file size uploads are limited to 5 MB. For information about how to adjust your upload file sizes and type, see this [Now Support article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0718101).Data type: String/stream

</td></tr></tbody>
</table>### Headers

<table id="table_bd2_pqs_byb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td>

Data type of the file to be uploaded. Supported types: **application/zip**, **text/plain**, **application/json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_cdq_fft_byb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_af3_kft_byb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to upload a content to a text file.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/components/file?autoValidate=true&appName=testApp&namePath=testComponent%2FfilesFolder&fileName=testFileNodeName.txt&publishOption=publish_valid&changesetNumber=Chset-108&autoCommit=true&fileNodeName=testFile.txt" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "This is sample content that will be uploaded to a plain text file."\ 
--user 'username':'password' 
```

The following return results show both a successful and an error response for this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Could not find active application with name: ‘testApp’ of type application", 
    "detail": "" 
  },
  "status": "failure"
}

```

## CdmApplicationsApi - POST /sn\_cdm/applications/uploads/components/vars

Submits a request to upload the passed-in configuration data under the vars folder, within the system components folder, for the specified application.

The following image shows an example of where the component's vars configuration data is uploaded in reference to the ServiceNow DevOps Config Workspace UI. Assumes the application is **paymentSvc**.

![Upload vars directory](../image/apps-uploads-comp-vars_data.png)

**Note:** The maximum default upload content size is 2 MB. You can modify this default by updating the property sn\_cdm.max\_allowed\_upload\_file\_size.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/uploads/components/vars`

Default URL: `/api/sn_cdm/applications/uploads/components/vars`

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
</table><table id="id_ey4_w13_psb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoDelete

</td><td>

Flag that indicates whether the existing nodes, that aren’t part of the upload content, are deleted after the processing is complete.Valid values:

-   true: Automatically delete existing nodes.
-   false: Don't automatically delete existing nodes.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr id="cdm_apps-dataFormat-row"><td>

dataFormat

</td><td>

Required. Format of the configuration data.Valid values:

-   ini
-   json
-   properties
-   raw
-   xml
-   yaml

Data type: String

</td></tr><tr><td>

deleteRedundantOverrides

</td><td>

Flag that indicates whether to create an override where redundant values are present.Valid values:

-   true: If redundant values are present, an override isn’t created.
-   false: If redundant values are present, proceeds with an override.

Default: true

</td></tr><tr><td>

fileName

</td><td>

Name of the file to upload. This name can differ from than the actual file name and contain the file extension. For example, .txt/.scv/.jar. The fileName value is applied when downloading the file.Data type: String

</td></tr><tr><td>

fileNodeName

</td><td>

Name of the file node. This file name is used in the configuration data when exporting it. This name doesn’t require a file extension nor does it affect the download.Data type: String

</td></tr><tr><td>

identifierKeys

</td><td>

List of names that indicate which key in an array child to use to identify the same node.For example, if you’re uploading:

```
[
  {"name" : "Allan, "city" : "Paris"}, 
  {"name" : "Karen, "city" : "Sydney"}
]
```

in the following existing model:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"}
]
```

and you set **identifierKeys** to `name`, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Sydney"},
  {"name" : "Allan, "city" : "Paris"}
]
```

Otherwise, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"},
  {"name" : "Allan, "city" : "Paris"},
  {"name" : "Karen, "city" : "Sydney"}
]
```

Data type: Array of Strings

</td></tr><tr><td>

ignoreAttributes

</td><td>

Flag that indicates whether the given data format supports attributes \(currently only XML\).Valid values:

-   true: If the given data format supports attributes, any attributes in the input data are skipped during the upload.
-   false: If the given data format supports attributes, any attributes in the input data are included in the upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library where the component to delete is located.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|Variable upload data|Configuration data to upload. This can be any data in the format defined by the **dataFormat** parameter of the query parameters.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="id_cvs_bmb_fwb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **text/plain** and **application/x-www-form-urlencoded**.Default: **text/plain**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_dqr_z13_psb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_pcq_1b3_psb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows a vars upload request for the application Demo\_App1631126164773.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/components/vars?changesetNumber=Chset-102&autoValidate=false&autoDelete=true&publishOption=publish_none&appName=Demo_App1631126164773&namePath=%2FSettings%2FdbSettings&autoCommit=false&dataFormat=json" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "{ 
  \"dbSettings\": { 
    \"dbIPAddress\": \"10.10.10.110\", 
    \"dbPort\": \"8080\", 
    \"dbConnectionString\": \"username:password server1.xyz.com:8080 dbName_payments\", 
    \"dbConnectionStringBackup\": \"username:password server2.xyz.com dbName_payments_backup\"
  } 
}"
--user 'username':'password' 
```

The following return results show both a successful and an error response for this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "d21f71f45322301096eccceaff7b1ce3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Size of uploaded data:6853632.0(bytes) is greater than max allowed upload limit of 2097152.0(bytes)", 
    "detail": "" 
  },
  "status": "failure"
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/uploads/collections

Submits a request to upload the passed-in configuration data for a specific collection, within the system collections folder, for the specified application.

This endpoint returns the ID of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.

**Note:** The maximum default upload content size is 2 MB. You can modify this default by updating the property sn\_cdm.max\_allowed\_upload\_file\_size.

The following image shows an example of where the configuration data is uploaded in reference to the ServiceNow DevOps Config Workspace UI. Assumes the collection is **db0Release1.0** and the application is **paymentSvc**.

![Collections upload folder](../image/apps-uploads-collections_data.png)

**Note:** This upload method cannot be used to modify nodes. Use the alternative [CdmApplicationsApi - POST /sn\_cdm/applications/uploads/collections/file](applications-api.md#) method to modify nodes.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/uploads/collections`

Default URL: `/api/sn_cdm/applications/uploads/collections`

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
</table><table id="id_ycw_c33_psb" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoDelete

</td><td>

Flag that indicates whether the existing nodes, that aren’t part of the upload content, are deleted after the processing is complete.Valid values:

-   true: Automatically delete existing nodes.
-   false: Don't automatically delete existing nodes.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

collectionName

</td><td>

Required. Name of the collection under which to store the uploaded payload. **Note:** If the specified **namePath** does not exist under this collection, the system automatically creates the component\(s\) under this collection and then uploads the configuration content. For example, if you want to upload the collection `collA`, with the path `compA/comp/compC`, the data is uploaded under `/collA/collections/compa/compB/compC`.

If `compA` exists but not `compB` and `compC`, then the endpoint creates these components and uploads the data under `compC`.

Data type: String

</td></tr><tr><td>

dataFormat

</td><td>

Required. Format of the configuration data.Valid values:

-   csv
-   ini
-   json
-   properties
-   raw
-   xml
-   yaml

Data type: String

</td></tr><tr><td>

dataFormatAttributes

</td><td id="cdm_app-dataFormAtt-entry">

Only supported when the **dataFormat** parameter is set to `csv`. Attributes that define the CSV data format. For additional information, see [Parsing of CSV files in CDM](https://www.servicenow.com/docs/access?context=cdm-parsing-csv-file&version=australia&pubname=australia-it-service-management&ft:locale=en-US).Data type: Object

```
"dataFormatAttributes" {
  "containsHeader": Boolean,
  "delimeter": "String"
  "headers": [Array],
  "securedHeaders": [Array]
}
```

</td></tr><tr><td>

dataFormatAttributes.containsHeaders

</td><td id="cdm_app-dataFormAtt_containsHeaders-entry">

Flag that indicates whether the data contains a header row.Valid values:

-   true: Data contains a header row. The first row in the data is considered the header row.

![Header row example](../image/cdm_header_row_example.png)

-   false: Data doesn't contain a header row. You must pass the header information in the **dataFormatAttributes.headers** parameter.

Data type: Boolean

Default: false

</td></tr><tr><td>

dataFormatAttributes.delimeter

</td><td id="cdm_app-dataFormAtt_delimeter-entry">

Character to use to delineate fields within the data.Data type: String

Default: Comma ","

</td></tr><tr><td>

dataFormatAttributes.headers

</td><td id="cdm_app-dataFormAtt_headers-entry">

Required if **dataFormatAttributes.containsHeaders** parameter is `false`. Fields in the data that comprise the header. These headers are converted to the key names of the CDIs in the JSON format. The number of headers must match the number of record fields.Data type: Array

Default: Empty array

</td></tr><tr><td>

dataFormatAttributes.securedHeaders

</td><td id="cdm_app-dataFormAtt_securedHeaders-entry">

Fields in the data that are secure fields and must be encrypted in the data uploaded to CDM. The name of the secured headers must match the name of the headers in the headers attribute or data file. These fields are stored in a column of type Password \(2 Way Encrypted\).**Note:** You can only secure fields using this attribute. You can't unsecure the secured fields.

Data type: Array

Default: Empty array

</td></tr><tr><td>

deleteRedundantOverrides

</td><td>

Flag that indicates whether to create an override where redundant values are present.Valid values:

-   true: If redundant values are present, an override isn’t created.
-   false: If redundant values are present, proceeds with an override.

Default: true

</td></tr><tr><td>

ignoreAttributes

</td><td>

Flag that indicates whether the given data format supports attributes \(currently only XML\).Valid values:

-   true: If the given data format supports attributes, any attributes in the input data are skipped during the upload.
-   false: If the given data format supports attributes, any attributes in the input data are included in the upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|Variable upload data|Configuration data to upload. This can be any data in the format defined by the **dataFormat** parameter of the query parameters.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="id_h4r_fmb_fwb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **text/plain** and **application/x-www-form-urlencoded**.Default: **text/plain**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_szz_f33_psb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_i55_g33_psb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

This example shows how to upload JSON-formatted **dbSettings** configuration date into the collections folder for the application Demo\_App1631126164773.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/collections?dataFormat=json&autoValidate=false&changesetNumber=Chset-102&appName=Demo_App1631126164773&autoDelete=true&namePath=%2FSettings%2FdbSettings&collectionName=release-1.0&autoCommit=false&publishOption=publish_none" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "{ 
  \"dbSettings\": { 
    \"dbIPAddress\": \"10.10.10.110\", 
    \"dbPort\": \"8080\", 
    \"dbConnectionString\": \"admin:admin server1.xyz.com:8080 dbName_payments\", 
    \"dbConnectionStringBackup\": \"admin:admin server2.xyz.com dbName_payments_backup\" 
  } 
}" \ 
--user 'username':'password' 
```

The following shows the possible responses to this call, both as a success and an error.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Size of uploaded data:6853632.0(bytes) is greater than max allowed upload limit of 2097152.0(bytes)", 
    "detail": "" 
  },
  "status": "failure"
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/uploads/collections/file

Uploads a file to the collections folder in the Configuration Data Model \(CDM\).

### URL format

Versioned URL: `POST /api/sn_cdm/{api_version}/applications/uploads/collections/file`

Default URL: `POST /api/sn_cdm/applications/uploads/collections/file`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="table_rgl_tbt_byb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table id="cdm_app-upload_query_parms-table" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

collectionName

</td><td>

Required. Name of the collection under which to store the uploaded payload.**Note:** If the specified `namePath` does not exist under this collection, the system automatically creates the component\(s\) under this collection and then uploads the configuration content. For example, if you want to upload the collection `collA`, with the path `compA/comp/compC`, the data is uploaded under `/collA/collections/compa/compB/compC`. If `compA` exists but not `compB` and `compC`, then the endpoint creates these components and uploads the data under `compC`.

Data type: String

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

fileName

</td><td>

Name of the file to upload. This name can differ from than the actual file name and contain the file extension. For example, .txt/.scv/.jar. The fileName value is applied when downloading the file.Data type: String

</td></tr><tr><td>

fileNodeName

</td><td>

Name of the file node. This file name is used in the configuration data when exporting it. This name doesn’t require a file extension nor does it affect the download.Data type: String

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

publishOption

</td><td id="publish_option-changeset-entry">

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

 **Note:** This option is only available if the value for the **autoCommit** parameter is true.

</td></tr></tbody>
</table><table id="table_j22_fgm_2yb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable upload data

</td><td>

Configuration data to upload. By default, file size uploads are limited to 5 MB. For information about how to adjust your upload file sizes and type, see this [Now Support article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0718101).Data type: String/stream

</td></tr></tbody>
</table>### Headers

<table id="table_enr_pqs_byb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td>

Content Type of the file to be uploaded. Examples: application/zip, text/plain, application/json.

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_cdq_fft_byb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="table_gft_zht_byb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following call uploads a plain text file to the CDM collections folder.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/collections/file?autoValidate=true&collectionName=collA&appName=testApp&namePath=testComponent%2FfilesFolder&fileName=testFileNodeName.txt&publishOption=publish_valid&changesetNumber=Chset-108&autoCommit=true&fileNodeName=testFile.txt" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "This is sample content that will be uploaded to a plain text file."\ 
--user 'username':'password'
```

The following return results show both a successful and an error response to this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Could not find active application with name: ‘testApp’ of type application", 
    "detail": "" 
  },
  "status": "failure"
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/uploads/deployables

Submits a request to upload the configuration content for a specific deployable within the deployables system folder of a specified application.

This endpoint returns the ID of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.

**Note:** The maximum default upload content size is 2 MB. You can modify this default by updating the property sn\_cdm.max\_allowed\_upload\_file\_size.

The following image shows an example of where the deployable configuration data is uploaded in reference to the ServiceNow DevOps Config UI. Assumes the deployable is **Development\_1** and the application is **paymentSvc**.

![Deployables config data location in UI](../image/apps-uploads-deployables_data.png)

**Note:** This upload method cannot be used to modify nodes. Use the alternative [CdmApplicationsApi - POST /sn\_cdm/applications/uploads/deployables/file](applications-api.md#) method to modify nodes.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/uploads/deployables`

Default URL: `/api/sn_cdm/applications/uploads/deployables`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoDelete

</td><td>

Flag that indicates whether the existing nodes, that aren’t part of the upload content, are deleted after the processing is complete.Valid values:

-   true: Automatically delete existing nodes.
-   false: Don't automatically delete existing nodes.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

dataFormat

</td><td>

Required. Format of the configuration data.Valid values:

-   csv
-   ini
-   json
-   properties
-   raw
-   xml
-   yaml

Data type: String

</td></tr><tr><td>

dataFormatAttributes

</td><td id="cdm_app-dataFormAtt-entry">

Only supported when the **dataFormat** parameter is set to `csv`. Attributes that define the CSV data format. For additional information, see [Parsing of CSV files in CDM](https://www.servicenow.com/docs/access?context=cdm-parsing-csv-file&version=australia&pubname=australia-it-service-management&ft:locale=en-US).Data type: Object

```
"dataFormatAttributes" {
  "containsHeader": Boolean,
  "delimeter": "String"
  "headers": [Array],
  "securedHeaders": [Array]
}
```

</td></tr><tr><td>

dataFormatAttributes.containsHeaders

</td><td id="cdm_app-dataFormAtt_containsHeaders-entry">

Flag that indicates whether the data contains a header row.Valid values:

-   true: Data contains a header row. The first row in the data is considered the header row.

![Header row example](../image/cdm_header_row_example.png)

-   false: Data doesn't contain a header row. You must pass the header information in the **dataFormatAttributes.headers** parameter.

Data type: Boolean

Default: false

</td></tr><tr><td>

dataFormatAttributes.delimeter

</td><td id="cdm_app-dataFormAtt_delimeter-entry">

Character to use to delineate fields within the data.Data type: String

Default: Comma ","

</td></tr><tr><td>

dataFormatAttributes.headers

</td><td id="cdm_app-dataFormAtt_headers-entry">

Required if **dataFormatAttributes.containsHeaders** parameter is `false`. Fields in the data that comprise the header. These headers are converted to the key names of the CDIs in the JSON format. The number of headers must match the number of record fields.Data type: Array

Default: Empty array

</td></tr><tr><td>

dataFormatAttributes.securedHeaders

</td><td id="cdm_app-dataFormAtt_securedHeaders-entry">

Fields in the data that are secure fields and must be encrypted in the data uploaded to CDM. The name of the secured headers must match the name of the headers in the headers attribute or data file. These fields are stored in a column of type Password \(2 Way Encrypted\).**Note:** You can only secure fields using this attribute. You can't unsecure the secured fields.

Data type: Array

Default: Empty array

</td></tr><tr><td>

deleteRedundantOverrides

</td><td>

Flag that indicates whether to create an override where redundant values are present.Valid values:

-   true: If redundant values are present, an override isn’t created.
-   false: If redundant values are present, proceeds with an override.

Default: true

</td></tr><tr><td>

deployableName

</td><td>

Required. Name of the deployable under which to store the uploaded payload. **Note:** If the specified **namePath** does not exist under this deployable, the system automatically creates the component\(s\) under this deployable and then uploads the configuration content.

</td></tr><tr><td>

identifierKeys

</td><td>

List of names that indicate which key in an array child to use to identify the same node.For example, if you’re uploading:

```
[
  {"name" : "Allan, "city" : "Paris"}, 
  {"name" : "Karen, "city" : "Sydney"}
]
```

in the following existing model:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"}
]
```

and you set **identifierKeys** to `name`, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Sydney"},
  {"name" : "Allan, "city" : "Paris"}
]
```

Otherwise, it produces the following output:

```
[
  {"name" : "Karen, "city" : "Manila"},
  {"name" : "Allan, "city" : "Brussels"},
  {"name" : "Allan, "city" : "Paris"},
  {"name" : "Karen, "city" : "Sydney"}
]
```

Data type: Array of Strings

</td></tr><tr><td>

ignoreAttributes

</td><td>

Flag that indicates whether the given data format supports attributes \(currently only XML\).Valid values:

-   true: If the given data format supports attributes, any attributes in the input data are skipped during the upload.
-   false: If the given data format supports attributes, any attributes in the input data are included in the upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

publishOption

</td><td id="publish_option-changeset-entry">

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

 **Note:** This option is only available if the value for the **autoCommit** parameter is true.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|Variable upload data|Configuration data to upload. This can be any data in the format defined by the **dataFormat** parameter of the query parameters.|

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="id_ilq_dmb_fwb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

Content-Type

</td><td>

Data format of the request body. Supported types: **text/plain** and **application/x-www-form-urlencoded**.Default: **text/plain**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_gty_cw3_psb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_gcv_2w3_psb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows an upload request for the application Demo\_App1631126164773.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/deployables?deployableName=TST-1&autoValidate=false&dataFormat=json&autoDelete=false&changesetNumber=Chset-102&appName=Demo_App1631126164773&publishOption=publish_none&autoCommit=true&namePath=%2FSettings%2FdbSettings" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "{
  \"dbIPAddress\": \"10.10.10.110\",
  \"dbPort\": \"8080\",
  \"dbConnectionString\": \"admin:admin server1.xyz.com:8080 dbName_payments\",
  \"dbConnectionStringBackup\": \"admin:admin server2.xyz.com dbName_payments_backup\"
}" \ 
--user 'username':'password' 
```

The following return results show both a successful and an error response for this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Size of uploaded data:6853632.0(bytes) is greater than max allowed upload limit of 2097152.0(bytes)", 
    "detail": "" 
  },
  "status": "failure"
}
```

## CdmApplicationsApi - POST /sn\_cdm/applications/uploads/deployables/file

Uploads files to the deployables folder in the Configuration Data Model \(CDM\).

### URL format

Versioned URL: `POST /api/sn_cdm/{api_version}/applications/uploads/deployables/file`

Default URL: `POST /api/sn_cdm/applications/uploads/deployables/file`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table id="table_rgl_tbt_byb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr></tbody>
</table><table id="cdm_app-upload_query_parms-table" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Name of the application to associate with the configuration data. This application must be in the active state.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

autoCommit

</td><td>

Flag that indicates whether the changeset identified in the **changesetNumber** parameter is committed to the data model after upload.Valid values:

-   true: Changeset is committed after upload.
-   false: Changeset isn't committed after upload.

Data type: Boolean

Default: false

</td></tr><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created when committed are validated.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

**Note:** This option is only available if the **autoCommit** parameter is `true`.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td>

String that uniquely identifies the [changeset](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=australia&pubname=australia-it-service-management&ft:locale=en-US) associated with the application, such as Chset-102. This changeset must be in the "Open" state.Data type: String

Default: Creates a changeset to use. The changeset details are returned as part of the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) results.

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

deployableName

</td><td id="deployableName-policy-entry">

Required. Name of the CDM deployable for which to map the policy.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

fileName

</td><td>

Name of the file to upload. This name can differ from than the actual file name and contain the file extension. For example, .txt/.scv/.jar. The fileName value is applied when downloading the file.Data type: String

</td></tr><tr><td>

fileNodeName

</td><td>

Name of the file node. This file name is used in the configuration data when exporting it. This name doesn’t require a file extension nor does it affect the download.Data type: String

</td></tr><tr><td>

namePath

</td><td>

Path of the targeted node under which the configuration data should be uploaded. This path is relative to the components, collection, or deployable folder \(depending on the endpoint being called\).You can pass the name path in any of the following formats. For example, to define the name path for the node `testApp/deployables/Development1/cdi1`:

-   Backslash format: `testApp/deployables/Development1/cdi1`

**Note:** If your node name contains a backslash \("/"\), you can’t use this format.

-   Backend name path with replacement characters: `testApp�deployables�​Development1​�​cdi1`
-   Array: `['testApp','deployables','Development1','cdi1']`

**Note:** If the specified component doesn't exist at the specified path, the system automatically creates the component at the specified path and then uploads the data.

Data type: String

</td></tr><tr><td>

publishOption

</td><td id="publish_option-changeset-entry">

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

 **Note:** This option is only available if the value for the **autoCommit** parameter is true.

</td></tr></tbody>
</table><table id="table_j22_fgm_2yb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Variable upload data

</td><td>

Configuration data to upload. By default, file size uploads are limited to 5 MB. For information about how to adjust your upload file sizes and type, see this [Now Support article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0718101).Data type: String/stream

</td></tr></tbody>
</table>### Headers

<table id="table_bd2_pqs_byb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td>

Data type of the file to be uploaded. Supported types: **application/zip**, **text/plain**, **application/json**.Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="id_cdq_fft_byb"><thead><tr><th>

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

Bad request.Upload request has been rejected.

Possible issues:

-   Size of configuration payload is greater that the allowed maximum - 2 MB by default.
-   Required parameters are missing from the call.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table id="id_af3_kft_byb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-stat-error"><td>

error

</td><td>

If an error occurred during processing, the details about the error.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr id="cdm_apps-stat-error_detail-row"><td>

error.detail

</td><td>

Additional information about the error.Data type: String

</td></tr><tr id="cdm_apps-stat-error_messaage-row"><td>

error.message

</td><td>

Error message that was generated while trying to process the request.Data type: String

</td></tr><tr id="cdm_apps-stat-error_status-row"><td>

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr><tr id="cdm_apps-upload_id-row"><td>

upload\_id

</td><td>

Sys\_id of the upload request. Use this ID to call the [CdmApplicationsApi - GET /sn\_cdm/applications/upload-status/\{upload\_id\}](applications-api.md#) endpoint to obtain the status of the upload.Data type: String

</td></tr></tbody>
</table>### cURL request

The following request uploads a plain text file to the deployables folder of the CDM application.

```
curl "http://instance.servicenow.com/api/sn_cdm/applications/uploads/deployables/file?autoValidate=true&deployableName=depA&appName=testApp&namePath=testComponent%2FfilesFolder&fileName=testFileNodeName.txt&publishOption=publish_valid&changesetNumber=Chset-108&autoCommit=true&fileNodeName=testFile.txt" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:text/plain" \ 
--data "This is sample content that will be uploaded to a plain text file."\ 
--user 'username':'password' 

```

The following return results show both a successful and an error response to this request.

```
// Successful completion of the upload request
{ 
  "result": { 
    "upload_id": "ec1f71f45322301096edddeeff7b12b3" 
  } 
} 

// Error response. Payload is too large.
{ 
  "error": { 
    "message": "Could not find active application with name: ‘testApp’ of type application", 
    "detail": "" 
  },
  "status": "failure"
}

```

## CdmApplicationsApi - PUT /sn\_cdm/applications/deployables

Updates the specified shared component in an application within a specified changeset.

Allows an update to the following fields:

-   Name
-   Description
-   Application Service\\Dynamic CI Group
-   Deployable identifier

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/deployables`

Default URL: `/api/sn_cdm/applications/deployables`

**Note:** Available versions are specified in the [REST API Explorer](use-REST-API-Explorer.md). For scripted REST APIs there is additional version information on the [Scripted REST Service form](../../custom-web-services/concept/c_CustomWebServices.md).

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td>

Optional. Version of the endpoint to access. For example, v1 or v2. Only specify this value to use an endpoint version other than the latest.Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the CDM Application.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the CDM Deployable.Data type: String

</td></tr><tr><td>

newDescription

</td><td>

Optional. A description for the CDM Deployable.Data type: String

</td></tr><tr><td>

newServiceId

</td><td>

Optional. The ID of the desired Application Service/Dynamic CI Group. In the cURL request, provide `'’` to disconnect the Deployable from the service.

</td></tr><tr><td>

newIdentifier

</td><td>

Optional. The identifier of the Deployable.Data type: Choice \(Development/Test/Production

</td></tr><tr><td>

newName

</td><td>

Optional. The new name of the Deployable.Data type: String

</td></tr><tr><td>

returnFields

</td><td>

Optional. Comma-separated list of fields to be returned as part of the response.

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported types: application/json|

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad request. A bad request type or malformed request was detected.|
|500|Internal Server Error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

CDM deployable sys\_Id.

</td></tr><tr><td>

name

</td><td>

Name of the CDM Deployable.

</td></tr><tr><td>

node

</td><td>

Deployable node object.`{ ‘value’: ‘<sysId>’, ‘link’: ‘http://localhost:8081/api/now/table/*’}`

</td></tr><tr><td>

description

</td><td>

CDM deployable description.

</td></tr><tr><td>

identifier

</td><td>

An identifier for the deployable.

</td></tr><tr><td>

cmdb\_ci

</td><td>

The app service object which is connected to a deployable.`{ ‘value’: ‘<sysId>’, ‘link’: ‘http://localhost:8081/api/now/table/*’}`

</td></tr><tr><td>

cmdb\_app

</td><td>

The CDM application object.`{ ‘value’: ‘<sysId>’, ‘link’: ‘http://localhost:8081/api/now/table/*’}`

</td></tr><tr><td>

snapshot\_version\_counter

</td><td>

The count of snapshots created for a deployable.

</td></tr><tr><td>

cdi\_count

</td><td>

The number of CDIs contained in this CDM deployable.

</td></tr><tr><td>

cdi\_usage

</td><td>

The CDI usage percentage.

</td></tr><tr><td>

environment\_type

</td><td>

The environment type. Possible values: -   development
-   production
-   test

</td></tr><tr><td>

state

</td><td>

The active or deleted state . Possible values: -   active
-   deleted

</td></tr><tr><td>

sys\_created\_by

</td><td>

CDM deployable created by &lt;username&gt;.

</td></tr><tr><td>

sys\_created\_on

</td><td>

CDM deployable creation timestamp in the format of &lt;yyyy-MM-dd hh:mm:ss&gt;.

</td></tr><tr><td>

sys\_updated\_by

</td><td>

CDM deployable updated by &lt;username&gt;.

</td></tr><tr><td>

sys\_updated\_on

</td><td>

CDM deployable updated by timestamp in the format of &lt;yyyy-MM-dd hh:mm:ss&gt;.

</td></tr></tbody>
</table>### cURL request

```
curl "http://localhost:8080/api/sn_cdm/applications/deployables?appName=testApp&name=Dep-1" \ 
--request PUT\ 
--header "Accept:application/json" \ 
--user 'cdm_admin':'password1!' 
```

Output:

```
{ 
  "result": { 
    "identifier": "identiy1", 
    "cmdb_ci": { 
      "value": "f5b9e00b53901110a1d3ddeeff7b12b8", 
      "link": "http://192.168.0.233:8080/api/now/table/cmdb_ci_service_auto/f5b9e00b53901110a1d3ddeeff7b12b8" 
    }, 
    "cdi_count": "3", 
    "snapshot_version_counter": "1", 
    "description": "cdcds", 
    "sys_updated_on": "2022-07-27 13:40:13", 
    "environment_type": "Test", 
    "node": { 
      "value": "30c00d4053015110a1d3ddeeff7b12bf", 
      "link": "http://192.168.0.233:8080/api/now/table/sn_cdm_node/30c00d4053015110a1d3ddeeff7b12bf" 
    }, 
    "sys_id": "39b9e00b53901110a1d3ddeeff7b12b7", 
    "sys_updated_by": "admin", 
    "cdm_app": { 
      "value": "62b517a953b70110a1d3ddeeff7b128c", 
      "link": "http://192.168.0.233:8080/api/now/table/sn_cdm_application/62b517a953b70110a1d3ddeeff7b128c" 
    }, 
    "sys_created_on": "2022-06-29 12:53:57", 
    "cdi_usage": "0.03", 
    "name": "Dep-2", 
    "state": "active", 
    "sys_created_by": "admin" 
  } 
} 
```

## CdmApplicationsApi - PUT /sn\_cdm/applications/shared\_components

Updates the specified shared component in an application within a specified changeset.

The CDM Admin role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/applications/shared_components`

Default URL: `/api/sn_cdm/applications/shared_components`

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
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changesetNumber

</td><td>

Required. Unique identifier of the changeset associated with the component.Data type: String

</td></tr><tr><td>

returnFields

</td><td id="cdm_apps-returnFields-entry">

List of fields to return as part of the response. Pass the record column names such as sys\_id, sys\_updated\_by, or state.Data type: Array

Default: All fields as determined by the endpoint

</td></tr><tr><td>

sharedComponentName

</td><td>

Required. Name of the shared component associated with the specified application.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library under which the component resides. The shared library must have the following fields defined as follows:-   state = active
-   available = true
-   type = shared\_library

Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

version

</td><td>

Required. Version name associated with the shared component.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. The passed changeset does not exist.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

The response fields depend on what fields were specified in the **returnFields** parameter in the request. The following describes some of the more important fields.

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeset\_id

</td><td id="changeset-node-editor-entry">

Details of the changeset record associated with the node. Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

changeset\_id.link

</td><td id="changeset_link-node-editor-entry">

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr><td>

changeset\_id.value

</td><td id="changeset_value-node-editor-entry">

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

description

</td><td>

Description of the CDM node.Data type: String

</td></tr><tr><td>

error

</td><td id="cdm_apps-error-entry">

Only returned if an error occurred during processing.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
}
```

</td></tr><tr><td>

error.detail

</td><td id="cdm_apps-error_detail-entry">

Details about the error that occurred.Data type: String

</td></tr><tr><td>

error.message

</td><td id="cdm_apps-error_message-entry">

Message that provides an overview of the error.Data type: String

</td></tr><tr><td>

linked\_to

</td><td>

ID of the main node associated with the shared component.Data type: String

</td></tr><tr><td>

linked\_to\_version

</td><td>

Details of the CDM snapshot record associated with the node. Data type: Object

 ```
"linked_to_version": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

linked\_to\_version.link

</td><td>

Call syntax for querying this version record using the Table REST API.Data type: String

</td></tr><tr><td>

linked\_to\_version.value

</td><td>

Sys\_id of the version record.Data type: String

</td></tr><tr><td>

main

</td><td>

Flag that indicates whether the associated snapshot was published.

 Valid values:

-   true: Snapshot was published.
-   false: Snapshot was not published.

</td></tr><tr><td>

main\_id

</td><td>

Unique ID of the newly created main node.Data type: String

</td></tr><tr><td>

main\_id\_encoded

</td><td>

Encoded ID of the newly created main node.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the CDM node.Data type: String

</td></tr><tr><td>

node

</td><td>

Sys\_id of the shared component node.Data type: String

</td></tr><tr><td>

node\_path

</td><td>

Path to the new linked node created when adding the shared component. Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the node.Possible values: New

 Data type: String

</td></tr><tr id="cdm_dep-sys_created_by-row"><td>

sys\_created\_by

</td><td>

User name of the user that create the CDM node. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_deps-sys_created_on-row"><td>

sys\_created\_on

</td><td>

Date and time when the CDM node was created.Format: YYYY-mm-DD hh:mm:ss

 Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="sys_id-node-editor-entry">

Sys\_id of the node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr id="cdm_dep-sys_updated_by-row"><td>

sys\_updated\_by

</td><td>

User name of the user that last updated the CDM node. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_dep-sys_updated_on-row"><td>

sys\_updated\_on

</td><td>

Date and time when the CDM node was last updated.Format: YYYY-mm-DD hh:mm:ss

 Data type: String

</td></tr><tr><td>

type

</td><td>

Node type.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to update the application "App1" with the shared component "paymentService-V1.1" under the shared library "OracleG-Library-10" within the "Chset-20" changeset.

```
"https://instance-name.service-now.com/api/sn_cdm/applications/shared_components?sharedComponentName=paymentService-V1.1&sharedLibraryName=OracleG-Library-10&changesetNumber=Chset-20&versionName=sComp3-v2.shc&appName=App1" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Response:

```
"result": {
  "changeset_id": {
    "value": "7343d0f71b771110636e0fe0604bcb0b",
    "link": "https://instance-name.service-now.com/api/now/table/sn_cdm_changeset/7343d0f71b771110636e0fe0604bcb0b"
  },
  "node_path": "!2!3!&`",
  "description": null,
  "sys_updated_on": "2022-12-22 18:52:38",
  "type": "sn_cdm_node_linked_shared_component",
  "sys_class_name": "sn_cdm_node",
  "sys_id": "339314b71b771110636e0fe0604bcba3",
  "sys_updated_by": ”admin",
  "previous_version": {
    "value": "a9ce80bf1b371110636e0fe0604bcb10",
    "link": "https://instance-name.service-now.com/api/now/table/sn_cdm_node/a9ce80bf1b371110636e0fe0604bcb10" 
  },
  "sys_created_on": "2022-12-22 18:52:38",
  "value": null,
  "effective_from": null,
  "linked_to": "146", 
  "sys_created_by": ”admin",
  "restricted_to": null,
  "linked_to_version": {
    "value": "54115c371b771110636e0fe0604bcb77",
    "link": "https://instance-name.service-now.com/api/now/table/sn_cdm_snapshot/54115c371b771110636e0fe0604bcb77"
  },
  "level": "2",
  "conflict_type": null,
  "main_id": "166",
  "effective_to": null,
  "secure_value": null,
  "node_classifier": "/application/components",
  "main_id_encoded": "&`",
  "name": "Component_A",
  "position": null,
  "reason_for_conflict": null,
  "system_folder": false,
  "status": "updated",
  "conflict": false
} 
```

