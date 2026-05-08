---
title: CdmVersionApi
description: The CdmVersionApi provides endpoints that enable you to publish, unpublish, and export versions \(snapshots\) in Configuration Data Management \(CDM\) for shared components under shared libraries.Returns the configuration data for a specified shared component within a specified shared library for a specified published version.Publishes a version of a shared component under a specified shared library.Unpublishes a version of a shared component under a specified shared library.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmVersionApi

The CdmVersionApi provides endpoints that enable you to publish, unpublish, and export versions \(snapshots\) in Configuration Data Management \(CDM\) for shared components under shared libraries.

You publish a snapshot so that it can be exported, enabling the Continuous Integration and Continuous Delivery \(CICD\) pipeline to access and use the associated shared components and libraries. Exporters can only execute on published snapshots. When snapshots are no longer needed, you can unpublish them to reduce the confusion as to whether the snapshot is viable anymore.

You must have one of the following roles to access this API:

-   Scripted REST CDM View ACL \(sn\_cdm.cdm.viewer\)
-   Scripted REST CDM Editor ACL \(sn\_cdm.cdm\_editor\)

In addition, the Configuration Data Management \(CDM\) plugin must be activated for this API to be available in an instance.

For additional information on snapshots, see View snapshots.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmVersionApi - GET /sn\_cdm/versions/export

Returns the configuration data for a specified shared component within a specified shared library for a specified published version.

The CDM Editor role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/versions/export`

Default URL: `/api/sn_cdm/versions/export`

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

decryptPassword

</td><td>

Flag that indicates whether to show encoded or decrypted password values.Valid values:

-   true: Decrypt password and show decrypted value.
-   false: Show encrypted password value.

Default: false

</td></tr><tr><td>

sharedComponentName

</td><td>

Required. Name of the shared component whose configuration data to export.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library that contains the component whose configuration data you want to return. The specified application must have the type field set to "shared\_library".Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

substituteVariables

</td><td>

Flag that indicates whether to follow the variables. For information on following the variables, see Validating and correcting configuration data.Valid values:

-   true: Follow the variables.
-   false: Do not follow variables.

Default: true

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

Bad Request. One of the follow problems may have occurred:-   Shared library is not active.
-   Shared component is not active.
-   Version s not published.
-   Parameter is missing in the call.

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

</th></tr></thead><tbody><tr><td>

result

</td><td>

Configuration data in the specified format.

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

The following code example shows how to export the configuration data of the "jdk8" component under the "JavaLib" shared library.

```
curl "http://instance.servicenow.com/api/sn_cdm/shared_libraries/components/exports?sharedLibraryName=JavaLib&componentName=jdk8 
--request POST \  
--header "Accept:application/json" \   
--user 'username':'password'
```

Response:

```
{  
"result": {  
    "sharedComponentA": { "cdi": "val" } 
 }  
} 
```

## CdmVersionApi - PUT /sn\_cdm/versions/publish

Publishes a version of a shared component under a specified shared library.

The CDM Editor role is required to access this endpoint.

**Note:** Snapshots and versions are synonymous in meaning for this implementation.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/versions/publish`

Default URL: `/api/sn_cdm/versions/publish`

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

name

</td><td>

Required. Name of the version of the shared component to publish.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

returnFields

</td><td>

Comma-separated list of fields in the CDM Snapshot \[sn\_cdm\_snapshot\] table to return as part of the response.Data type: String

Default: Returns all non-system fields.

</td></tr><tr><td>

sharedComponentName

</td><td>

Required. Name of the shared component to publish.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library in which the specified component resides. The type field in the associated record must be set to "shared\_library".Data type: String

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

Bad Request. Error occurred during publishing.Possible issues:

-   Version name not found.
-   Component version is already published.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table id="id_rtv_wbb_fwb"><thead><tr><th>

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

This code example shows how to publish the shared component "Development" with the version name of "Development-v1.shc".

```
curl "http://instance.servicenow.com/api/sn_cdm/versions/publish?sharedLibraryName=LibraryJdk&componentName=Development&name=Development-v1.shc" \  
--request PUT\  
--header "Accept:application/json" \  
--user 'username':'password
```

Response:

```
{
  "result": {
    "changeset_id": {
      "value": "1a2bd15c7764a1109ac0cf0bbb5a99fc",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_changeset/1a2bd15c7764a1109ac0cf0bbb5a99fc"
    },
    "cdm_deployable_id": null,
    "cdm_shared_component_node_id": {
      "value": "fe2b155c7764a1109ac0cf0bbb5a995d",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_node/fe2b155c7764a1109ac0cf0bbb5a995d"
    },
    "cdm_shared_component_id": {
      "value": "362b155c7764a1109ac0cf0bbb5a9970",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_shared_component/362b155c7764a1109ac0cf0bbb5a9970"
    },
    "description": null,
    "cdm_application_id": {
      "value": "122bd15c7764a1109ac0cf0bbb5a99fa",
      "link": "http://instance.servicenow.com/api/now/table/sn_cdm_application/122bd15c7764a1109ac0cf0bbb5a99fa"
    },
    "published": true,
    "sys_updated_on": "2023-01-18 14:15:44",
    "last_published": "2023-01-18 09:53:37",
    "sequence_number": "1",
    "number": "SNAP0001110",
    "sys_id": "df2b155c7764a1109ac0cf0bbb5a9949",
    "sys_updated_by": "admin",
    "sys_created_on": "2023-01-18 09:53:36",
    "name": "logonService-V2.1-v1.shc",
    "last_validated": "",
    "validation": "passed",
    "sys_created_by": "admin"
  }
}
```

## CdmVersionApi - PUT /sn\_cdm/versions/unpublish

Unpublishes a version of a shared component under a specified shared library.

The CDM Editor role is required to access this endpoint.

**Note:** Snapshots and versions are synonymous in meaning for this implementation.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/versions/publish`

Default URL: `/api/sn_cdm/versions/publish`

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

name

</td><td>

Required. Name of the version of the shared component to unpublish.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

returnFields

</td><td>

Comma-separated list of fields in the CDM Snapshot \[sn\_cdm\_snapshot\] table to return as part of the response.Data type: String

Default: Returns all non-system fields.

</td></tr><tr><td>

sharedComponentName

</td><td>

Required. Name of the shared component to unpublish.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr><td>

sharedLibraryName

</td><td>

Required. Name of the shared library in which the specified component resides. The type field in the associated record must be set to "shared\_library".Data type: String

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

</td><td id="cdm_apps-sl_req_headers-accept-entry">

Data format of the response body. Supported types:

-   **application/json**
-   **application/xml**
-   **text/xml**

Default: **application/json**

</td></tr></tbody>
</table>|Header|Description|
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

Bad Request. Error occurred during unpublishing.Possible issues:

-   Version name not found.
-   Component version is already published.

</td></tr><tr><td>

500

</td><td id="entry-500-status-code">

Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.

</td></tr></tbody>
</table>### Response body parameters

<table id="id_mbl_2cb_fwb"><thead><tr><th>

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

The following code example shows how to unpublish the "paymentService-V1" shared component from the "OracleG-Library-10" shared library.

```
curl "https://instance-name.service-now.com/api/sn_cdm/versions/unpublish?sharedLibraryName=OracleG-Library-10&sharedComponentName=paymentService-V1.1&name=paymentService-V1.1-v1.shc" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Response:

```
{
  "result": {
    "changeset_id": {
      "value": "1a2bd15c7764a1109ac0cf0bbb5a99fc",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_changeset/1a2bd15c7764a1109ac0cf0bbb5a99fc"
    },
    "cdm_deployable_id": null,
    "cdm_shared_component_node_id": {
      "value": "fe2b155c7764a1109ac0cf0bbb5a995d",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_node/fe2b155c7764a1109ac0cf0bbb5a995d"
    },
    "cdm_shared_component_id": {
      "value": "362b155c7764a1109ac0cf0bbb5a9970",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_shared_component/362b155c7764a1109ac0cf0bbb5a9970"
    },
    "description": null,
    "cdm_application_id": {
      "value": "122bd15c7764a1109ac0cf0bbb5a99fa",
      "link": "http://192.168.0.129:8080/api/now/table/sn_cdm_application/122bd15c7764a1109ac0cf0bbb5a99fa"
    },
    "published": false,
    "sys_updated_on": "2023-01-18 14:15:44",
    "last_published": "2023-01-18 09:53:37",
    "sequence_number": "1",
    "number": "SNAP0001110",
    "sys_id": "df2b155c7764a1109ac0cf0bbb5a9949",
    "sys_updated_by": "admin",
    "sys_created_on": "2023-01-18 09:53:36",
    "name": "logonService-V2.1-v1.shc",
    "last_validated": "",
    "validation": "passed",
    "sys_created_by": "admin"
  }
}
```

