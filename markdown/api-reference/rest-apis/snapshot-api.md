---
title: CdmSnapshotApi
description: The CdmSnapshotApi provides endpoints that enable you to publish, unpublish, and re-validate snapshots in Configuration Data Management \(CDM\).Publishes a specified unpublished snapshot.Unpublishes a previously published snapshot.Validates a specified unpublished snapshot.Publishes a specified unpublished snapshot.Unpublishes a previously published snapshot.Validates a specified unpublished snapshot against its mapped policies.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 21
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmSnapshotApi

The CdmSnapshotApi provides endpoints that enable you to publish, unpublish, and re-validate snapshots in Configuration Data Management \(CDM\).

You publish a snapshot so that it can be exported, enabling the Continuous Integration and Continuous Delivery \(CICD\) pipeline to access and use the associated configuration data. Exporters can only execute on published snapshots. When snapshots are no longer needed, you can unpublish them to reduce the confusion as to whether the snapshot is viable anymore.

You must have one of the following roles to access this API:

-   Scripted REST CDM View ACL \(sn\_cdm.cdm.viewer\)
-   Scripted REST CDM Editor ACL \(sn\_cdm.cdm\_editor\)

In addition, the Configuration Data Management \(CDM\) plugin must be activated for this API to be available in an instance.

For additional information on snapshots, see View snapshots.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmSnapshotAPI - POST /sn\_cdm/snapshots/\{snapshot\_id\}/publish

Publishes a specified unpublished snapshot.

Before a snapshot can be published, it must be validated. You can use the [CdmSnapshotAPI - POST /sn\_cdm/snapshots/\{snapshot\_id\}/validate](snapshot-api.md#) endpoint to validate snapshots or have them automatically validated when you do a commit. A deployable must be connected to a service to publish its snapshots. Also, if the snapshot has already been published, the request will fail.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/snapshots/{snapshot_id}/publish`

Default URL: `/api/sn_cdm/snapshots/{snapshot_id}/publish`

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

snapshot\_id

</td><td>

Sys\_id of the snapshot record to process.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

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

### Response body parameters \(JSON or XML\)

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

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to publish the snapshot with the sys\_id of 3a168d9dc342301054c1582e1340dd68.

```
curl "http://instance.servicenow.com/api/sn_cdm/snapshots/3a168d9dc342301054c1582e1340dd68/publish"\ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

The following shows both a success and failure response to the publish request.

```
// Example of a successful response
{ 
  "" 
}

// Example of an error response
{
  "error": {
    "message": "Error: Unexpected error occurred in publish request.Error:Snapshot not found",
    "detail": ""
  },
  "status": "failure"
}
```

## CdmSnapshotAPI - POST /sn\_cdm/snapshots/\{snapshot\_id\}/unpublish

Unpublishes a previously published snapshot.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/snapshots/{snapshot_id}/unpublish`

Default URL: `/api/sn_cdm/snapshots/{snapshot_id}/unpublish`

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

snapshot\_id

</td><td>

Sys\_id of the snapshot record to process.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

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

### Response body parameters \(JSON or XML\)

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

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to unpublish the snapshot with the sys\_id of 3a168d9dc342301054c1582e1340dd68.

```
curl "http://instance.servicenow.com/api/sn_cdm/snapshots/3a168d9dc342301054c1582e1340dd68/unpublish"\ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

The following shows both a success and failure response to the unpublish request.

```
// Example of a successful response
{ 
  "" 
}

// Example of an error response
{
  "error": {
    "message": "Error: Unexpected error occurred in publish request.Error:Snapshot not found",
    "detail": ""
  },
  "status": "failure"
}
```

## CdmSnapshotAPI - POST /sn\_cdm/snapshots/\{snapshot\_id\}/validate

Validates a specified unpublished snapshot.

The validation is performed as an asynchronous process. Calling this endpoint only starts the validation process. The return results from this call only indicate whether the validation process started, not the results of the validation itself. To find out if the snapshot has validated, use the Table API to locate the snapshot and check its validation status.

**Note:** You cannot validate a published snapshot.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/snapshots/{snapshot_id}/validate`

Default URL: `/api/sn_cdm/snapshots/{snapshot_id}/validate`

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

snapshot\_id

</td><td>

Sys\_id of the snapshot record to process.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

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
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. The specified snapshot is already published or cannot be located.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

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

status

</td><td>

Error status of the request.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to validate the snapshot with the sys\_id of 3a168d9dc342301054c1582e1340dd68.

```
curl "http://instance.servicenow.com/api/sn_cdm/snapshots/3a168d9dc342301054c1582e1340dd68/validate"\ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

The following shows both a success and failure response to the validate request.

```
// Example of a successful response
{ 
  "" 
}

// Example of an error response
{
  "error": {
    "message": "Invalid Snapshot id:test",
    "detail": ""
  },
  "status": "failure"
}
```

## CdmSnapshotApi - PUT /sn\_cdm/snapshots/publish

Publishes a specified unpublished snapshot.

Before a snapshot can be published, it must be validated. You can use the [CdmSnapshotApi - PUT /sn\_cdm/snapshots/validate](snapshot-api.md#) endpoint to validate snapshots or have them automatically validated when you do a commit. A deployable must be connected to a service to publish its snapshots. Also, if the snapshot has already been published, the request will fail.

The caller of this endpoint must have the CDM Editor role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/snapshots/publish`

Default URL: `/api/sn_cdm/snapshots/publish`

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
</table><table id="id_evn_23g_15b" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the Configuration Data Management \(CDM\) application for which to create the snapshot.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

deployableName

</td><td>

Required. Name of the CDM deployable for which to create the snapshot.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the snapshot.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

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

<table id="id_lrr_frg_15b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cdm\_application\_id

</td><td>

Details about the CDM application associated with the snapshot.Data type: Object

```
"cdm_application_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_application\_id.link

</td><td>

Call to use to access the CDM application record using the REST Table API. Data type: String

</td></tr><tr><td>

cdm\_application\_id.value

</td><td>

Sys\_id of the associated CDM application record.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

cdm\_deployable\_id

</td><td>

Details about the CDM deployable associated with the snapshot.Data type: Object

```
"cdm_deployable_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_deployable\_id.link

</td><td>

Call syntax for querying this deployable record using the Table REST API.Data type: String

</td></tr><tr><td>

cdm\_deployable\_id.value

</td><td>

Sys\_id of the deployable record.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

changeset\_id

</td><td>

Details about the changeset associated with the snapshot.Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

changeset\_id.link

</td><td>

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr><td>

changeset\_id.value

</td><td>

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

description

</td><td>

Brief description of the snapshot.Data type: String

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

last\_published

</td><td>

Date and time that the snapshot was last published.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

last\_validated

</td><td>

Date and time that the snapshot was last validated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

name

</td><td>

Name of the snapshot.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the snapshot. This value provides a human-readable identifier for the mapping.Data type: String

</td></tr><tr><td>

published

</td><td>

Flag that indicates whether the snapshot was published.Possible values:

-   true: Snapshot was published.
-   false: Snapshot wasn't published.

Data type: Boolean

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the snapshot.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time when the snapshot was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the snapshot.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that updated the snapshot.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time when the snapshot was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

validation

</td><td>

Current validation state of the snapshot. Possible values:

-   execution\_error
-   failed
-   in\_progress
-   not\_validated
-   passed
-   passed\_with\_exception
-   requested

Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to publish a snapshot.

```
curl "http://instance.servicenow.com/api/sn_cdm/snapshots/publish?deployableName=Development_1&name=Development_1-v1.dpl&appName=testApp" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
 
{ 
  "result": { 
    "changeset_id": { 
      "value": "d4b9446e53001110a1d3ddeeff7b126c", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/d4b9446e53001110a1d3ddeeff7b126c" 
    }, 
    "cdm_deployable_id": { 
      "value": "6dc517a953b70110a1d3ddeeff7b129b", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_deployable/6dc517a953b70110a1d3ddeeff7b129b" 
    }, 
    "description": null, 
    "cdm_application_id": { 
      "value": "62b517a953b70110a1d3ddeeff7b128c", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_application/62b517a953b70110a1d3ddeeff7b128c" 
    }, 
    "published": true, 
    "sys_updated_on": "2022-06-30 12:57:02", 
    "last_published": "2022-06-30 12:57:02", 
    "number": "SNAP0001002", 
    "sys_id": "9017fc2e53801110a1d3ddeeff7b12d7", 
    "sys_updated_by": "admin", 
    "sys_created_on": "2022-06-15 14:19:38", 
    "name": "Development_1-v2.dpl", 
    "last_validated": "2022-06-30 12:56:07", 
    "validation": "passed", 
    "sys_created_by": "admin" 
  } 
}
```

## CdmSnapshotApi - PUT /sn\_cdm/snapshots/unpublish

Unpublishes a previously published snapshot.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/snapshots/unpublish`

Default URL: `/api/sn_cdm/snapshots/unpublish`

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

Required. Name of the Configuration Data Management \(CDM\) application for which to create the snapshot.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

deployableName

</td><td>

Required. Name of the CDM deployable for which to create the snapshot.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the snapshot.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

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

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cdm\_application\_id

</td><td>

Details about the CDM application associated with the snapshot.Data type: Object

```
"cdm_application_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_application\_id.link

</td><td>

Call to use to access the CDM application record using the REST Table API. Data type: String

</td></tr><tr><td>

cdm\_application\_id.value

</td><td>

Sys\_id of the associated CDM application record.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

cdm\_deployable\_id

</td><td>

Details about the CDM deployable associated with the snapshot.Data type: Object

```
"cdm_deployable_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_deployable\_id.link

</td><td>

Call syntax for querying this deployable record using the Table REST API.Data type: String

</td></tr><tr><td>

cdm\_deployable\_id.value

</td><td>

Sys\_id of the deployable record.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

changeset\_id

</td><td>

Details about the changeset associated with the snapshot.Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

changeset\_id.link

</td><td>

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr><td>

changeset\_id.value

</td><td>

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

description

</td><td>

Brief description of the snapshot.Data type: String

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

last\_published

</td><td>

Date and time that the snapshot was last published.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

last\_validated

</td><td>

Date and time that the snapshot was last validated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

name

</td><td>

Name of the snapshot.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the snapshot. This value provides a human-readable identifier for the mapping.Data type: String

</td></tr><tr><td>

published

</td><td>

Flag that indicates whether the snapshot was published.Possible values:

-   true: Snapshot was published.
-   false: Snapshot wasn't published.

Data type: Boolean

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the snapshot.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time when the snapshot was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the snapshot.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that updated the snapshot.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time when the snapshot was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

validation

</td><td>

Current validation state of the snapshot. Possible values:

-   execution\_error
-   failed
-   in\_progress
-   not\_validated
-   passed
-   passed\_with\_exception
-   requested

Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to unpublish a snapshot.

```

```

Return results:

```

```

## CdmSnapshotApi - PUT /sn\_cdm/snapshots/validate

Validates a specified unpublished snapshot against its mapped policies.

The validation is performed as an asynchronous process. Calling this endpoint only starts the validation process. The return results from this call only indicate whether the validation process started, not the results of the validation itself. To find out if the snapshot has validated, use the Table API to locate the snapshot and check its validation status.

**Note:** You cannot validate a published snapshot.

The caller of this endpoint must have the CDM Editor role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/snapshots/validate`

Default URL: `/api/sn_cdm/snapshots/validate`

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
</table><table id="id_x2b_qvg_15b" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

appName

</td><td>

Required. Name of the Configuration Data Management \(CDM\) application for which to create the snapshot.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

deployableName

</td><td>

Required. Name of the CDM deployable for which to create the snapshot.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

name

</td><td>

Required. Name of the snapshot.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

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
|400|Bad Request. The specified snapshot is already published or cannot be located.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_dsl_5vg_15b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cdm\_application\_id

</td><td>

Details about the CDM application associated with the snapshot.Data type: Object

```
"cdm_application_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_application\_id.link

</td><td>

Call to use to access the CDM application record using the REST Table API. Data type: String

</td></tr><tr><td>

cdm\_application\_id.value

</td><td>

Sys\_id of the associated CDM application record.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

cdm\_deployable\_id

</td><td>

Details about the CDM deployable associated with the snapshot.Data type: Object

```
"cdm_deployable_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_deployable\_id.link

</td><td>

Call syntax for querying this deployable record using the Table REST API.Data type: String

</td></tr><tr><td>

cdm\_deployable\_id.value

</td><td>

Sys\_id of the deployable record.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

changeset\_id

</td><td>

Details about the changeset associated with the snapshot.Data type: Object

```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

changeset\_id.link

</td><td>

Call syntax for querying this changeset record using the Table REST API.Data type: String

</td></tr><tr><td>

changeset\_id.value

</td><td>

Unique identifier of the changeset record.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

description

</td><td>

Brief description of the snapshot.Data type: String

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

last\_published

</td><td>

Date and time that the snapshot was last published.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

last\_validated

</td><td>

Date and time that the snapshot was last validated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

name

</td><td>

Name of the snapshot.Data type: String

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the snapshot. This value provides a human-readable identifier for the mapping.Data type: String

</td></tr><tr><td>

published

</td><td>

Flag that indicates whether the snapshot was published.Possible values:

-   true: Snapshot was published.
-   false: Snapshot wasn't published.

Data type: Boolean

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the snapshot.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time when the snapshot was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the snapshot.Data type: String

Table: CDM Snapshot \[sn\_cdm\_snapshot\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that updated the snapshot.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time when the snapshot was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

validation

</td><td>

Current validation state of the snapshot. Possible values:

-   execution\_error
-   failed
-   in\_progress
-   not\_validated
-   passed
-   passed\_with\_exception
-   requested

Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to validate a snapshot.

```
curl "http://instance.servicenow.com/api/sn_cdm/snapshots/validate?name=Development_1-v2.dpl&deployableName=Development_1&appName=testApp" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

Return results:

```
{ 
  "result": { 
    "changeset_id": { 
      "value": "d4b9446e53001110a1d3ddeeff7b126c", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/d4b9446e53001110a1d3ddeeff7b126c" 
    }, 
    "cdm_deployable_id": { 
      "value": "6dc517a953b70110a1d3ddeeff7b129b", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_deployable/6dc517a953b70110a1d3ddeeff7b129b" 
    }, 
    "description": null, 
    "cdm_application_id": { 
      "value": "62b517a953b70110a1d3ddeeff7b128c", 
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_application/62b517a953b70110a1d3ddeeff7b128c" 
    }, 
    "published": false, 
    "sys_updated_on": "2022-06-30 12:57:02", 
    "last_published": "2022-06-30 12:57:02", 
    "number": "SNAP0001002", 
    "sys_id": "9017fc2e53801110a1d3ddeeff7b12d7", 
    "sys_updated_by": "admin", 
    "sys_created_on": "2022-06-15 14:19:38", 
    "name": "Development_1-v2.dpl", 
    "last_validated": "2022-06-30 12:56:07", 
    "validation": "passed", 
    "sys_created_by": "admin" 
  } 
} 
```

