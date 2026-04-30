---
title: CdmChangesetsApi
description: The CdmChangesetsApi provides endpoints that enable you to manage changesets.Deletes a specified changeset.Retrieves all changesets associated with a Configuration Data Management \(CDM\) application or a specified changeset record.Retrieves the node changes within a specified changeset.Returns the current status of the specified changeset commit request.Returns the list of deployables that are associated with a specified changeset.Returns a list of shared components that are associated with a specified changeset.Returns the list of deployables that are associated with a specified changeset.Commits the specified changeset. Once committed, the changeset is persisted into the CDM tables within the associated instance.Creates a new changeset in the open state for a specified CDM application or shared library.Updates and commits a specified changeset.
locale: en-US
release: zurich
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 40
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmChangesetsApi

The CdmChangesetsApi provides endpoints that enable you to manage changesets.

Using these endpoints you can:

-   Create new changesets.
-   Deploy changesets.
-   Retrieve lists of or individual changesets.
-   Retrieves the node changes within a changeset.
-   Retrieve a list of applications or deployables that are impacted by a changeset.
-   Delete changesets.
-   Return a list of shared components that are associated with a specified changeset.

The create changesets endpoints use an asynchronous queuing implementation. With this type of implementation, you first call the create changeset request endpoint. This endpoint queues your request and returns a commit identifier. You then use this commit identifier to call the appropriate status endpoint to obtain the status of the create request.

You must have one of the following roles to access this API:

-   Scripted REST CDM View ACL \(sn\_cdm.cdm.viewer\)
-   Scripted REST CDM Editor ACL \(sn\_cdm.cdm\_editor\)

In addition, the Configuration Data Management \(CDM\) plugin must be activated for this API to be available in an instance.

For additional information on changesets, see [Changesets and version control in CDM](https://www.servicenow.com/docs/access?context=cdm-changesets-version-control&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmChangesetsApi - DELETE /sn\_cdm/changesets

Deletes a specified changeset.

The caller must have the CDM Editor role to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets`

Default URL: `/api/sn_cdm/changesets`

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

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

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

The following code example shows how to remove a changeset.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets?changesetNumber=Chset-760" \ 
--request DELETE \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

For a successful deletion of the changeset, no response is returned other than the HTTP status code.

```
None - results defined by the HTTP status code
```

## CdmChangesetsApi - GET /sn\_cdm/changesets

Retrieves all changesets associated with a Configuration Data Management \(CDM\) application or a specified changeset record.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets`

Default URL: `/api/sn_cdm/changesets`

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

Required. Name of the CDM application whose changesets you want returned. This must be an active application.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

number

</td><td>

Changeset number.If you pass this value, only the specified changeset is returned. It must be a changeset that is associated with the CDM application specified in the **appName** parameter.

Data type: String

Default: None - return all changesets associated with the CDM application or the ones specified by the **state** parameter.

Table: CDMChangeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

state

</td><td>

State of the changesets to return. Only return the changesets associated with the specified CDM application for the specified state.Valid values:

-   Blocked
-   Checking for conflict
-   Commit failed
-   Commit in progress
-   Committed
-   Open

Data type: String

Default: Return all changesets for all states

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

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-autoValidate-row"><td>

auto\_validate

</td><td>

Flag that indicates whether the changesets created upon commit are validated.Valid values:

-   true: Validate the changesets.
-   false: Don't validate the changesets.

Data type: Boolean

</td></tr><tr><td>

cdm\_application

</td><td>

Details of the CDM application associated with the changeset. Data type: Object

```
"cdm_application": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

cdm\_application.link

</td><td>

Query to use to call the Table REST endpoint to retrieve the associated CDM application.Data type: String

</td></tr><tr><td>

cdm\_application.value

</td><td>

Sys\_id of the associated CDM application.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

committed\_at

</td><td id="committed_at-changeset-entry">

Date and time that the changeset was last committed.Data type: String

Format: YYYY-mm-DD hh:mm:ss

</td></tr><tr><td>

committed\_by

</td><td>

Details about the user that committed the changeset.Data type: Object

```
"committed_by": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

committed\_by.link

</td><td>

Call to obtain the record of the user that committed the changeset using the REST Table API.Data type: String

</td></tr><tr><td>

committed\_by.value

</td><td>

Sys\_id of the user who committed the changeset.Data type: String

</td></tr><tr><td>

description

</td><td>

Brief description of the purpose of the changeset.Data type: String

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

last\_conflict\_detection\_time

</td><td>

Amount of time since the last conflict detection was run. Conflict detection is performed whenever a changeset is committed.Data type: Number

Unit: Milliseconds

</td></tr><tr><td>

last\_updated

</td><td>

Date and time when a change was made to the associated configuration data through this changeset.Format: YYYY-mm-DD hh:mm:ss

Data type: String

</td></tr><tr><td>

number

</td><td>

Unique changeset number.Data type: String

</td></tr><tr><td>

publish\_option

</td><td>

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

</td></tr><tr><td>

state

</td><td>

Current state of the changeset.Possible values:

-   Blocked
-   Checking for conflict
-   Commit failed
-   Commit in progress
-   Committed
-   Open

Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td id="sys_created_by-changeset-entry">

User name of the user that created the changeset. For example, able.tuter.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td id="sys_created_on-changeset-entry">

Date and time when the changeset was created.Data type: String

Format: YYYY-mm-DD hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td id="sys_id-changeset-entry">

Sys\_id of the changeset.Data type: String

Table: CDMChangeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

sys\_updated\_by

</td><td id="sys_updated_by-changeset-entry">

User name of the user that last updated the changeset. For example, able.tuter.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td id="sys_updated_on-changeset-entry">

Date and time when the changeset was last updated.Data type: String

Format: YYYY-mm-DD hh:mm:ss

</td></tr><tr><td>

title

</td><td>

Title of the changeset.Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to retrieve a specific changeset.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets?appName=testApp&changesetNumber=Chset-946&state=committed" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
{ 
  "result": [ 
    { 
      "description": "Auto generated for deletion of CDM Deployable Dep-12022-06-29 13:09:46", 
      "cdm_application": { 
        "value": "62b517a953b70110a1d3ddeeff7b128c", 
        "link": "http://instance.servicenow.com/api/now/table/sn_cdm_application/62b517a953b70110a1d3ddeeff7b128c" 
      }, 
      "sys_updated_on": "2022-06-29 13:09:47", 
      "title": "Auto generated for deletion of CDM Deployable Dep-12022-06-29 13:09:46", 
      "number": "Chset-946", 
      "sys_id": "955d6c0f53141110a1d3ddeeff7b1233", 
      "sys_updated_by": "admin", 
      "committed_at": "2022-06-29 13:09:46", 
      "sys_created_on": "2022-06-29 13:09:46", 
      "committed_by": { 
        "value": "6816f79cc0a8016401c5a33be04be441", 
        "link": "http://instance.servicenow.com/api/now/table/sys_user/6816f79cc0a8016401c5a33be04be441" 
      }, 
      "state": "committed", 
      "auto_validate": true, 
      "publish_option": "publish_none", 
      "last_conflict_detection_time": "1656508187450", 
      "sys_created_by": "admin", 
      "last_updated": "2022-06-29 13:09:46" 
    } 
  ] 
} 
```

## CdmChangesetsApi - GET /sn\_cdm/changesets/activity

Retrieves the node changes within a specified changeset.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/activity`

Default URL: `/api/sn_cdm/changesets/activity`

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

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

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

changeset\_id

</td><td>

Details of the requested changeset. Data type: Object

 ```
"changeset_id": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

changeset\_id.link

</td><td>

Query to use to call the Table REST endpoint to retrieve the associated changeset.Data type: String

</td></tr><tr><td>

changeset\_id.value

</td><td>

Sys\_id of the associated changeset.Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

conflict

</td><td>

Flag that indicates whether there is a conflict in the associated changeset.Valid values:

-   true: Conflict detected.
-   false: No conflict found.

Data type: Boolean

</td></tr><tr><td>

created

</td><td>

Date and time when the node was created.Format: YYYY-mm-DD hh:mm:ss

Data type: String

</td></tr><tr><td>

created\_by

</td><td>

User name of the user that create the node. For example, able.tuter.Data type: String

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

name\_path

</td><td>

Node path name.Data type: String

</td></tr><tr><td>

new\_name

</td><td>

Current name of the node.Data type: String

</td></tr><tr><td>

new\_value

</td><td>

Current value of the node. For leaf nodes and array literals.Data type: String

</td></tr><tr><td>

old\_name

</td><td>

Previous name of the node.Data type: String

</td></tr><tr><td>

old\_value

</td><td>

Previous value of the node. For leaf nodes and array literals.Data type: String

</td></tr><tr><td>

updated

</td><td>

Date and time when the node was last updated.Format: YYYY-mm-DD hh:mm:ss

Data type: String

</td></tr><tr><td>

updated\_by

</td><td>

User name of the user that last updated the node. For example, able.tuter.Data type: String

</td></tr><tr><td>

secure

</td><td>

Flag that indicates whether the associated leaf node was secured.Valid values:

-   true: Node was secured.
-   false: Node was not secured.

Data type: Boolean

</td></tr><tr><td>

type

</td><td>

Node type.

Possible values:

-   sn\_cdm\_node\_collection
-   sn\_cdm\_node\_component
-   sn\_cdm\_node\_folder
-   sn\_cdm\_node\_cdi
-   sn\_cdm\_node\_variable

Data type: String

</td></tr></tbody>
</table>### cURL request

This code example shows how to retrieve the node changes for a specific changeset.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/activity?changesetNumber=Chset-783" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
{ 
  "result": [ 
    { 
      "sys_id": "ed5d6c0f53141110a1d3ddeeff7b1233", 
      "changeset_id": "955d6c0f53141110a1d3ddeeff7b1233", 
      "new_value": null, 
      "new_state": "Deleted", 
      "new_name": "Dep-1", 
      "new_type": "Deployable", 
      "new_encrypted": false, 
      "updated_on": "2022-06-29 13:09:46", 
      "updated_by": "admin", 
      "resolution_method": "", 
      "conflict": null, 
      "path": "deployables/Dep-1", 
      "created_by": null, 
      "created_on": null, 
      "old_value": null, 
      "old_state": "Superseded", 
      "old_name": "Dep-1", 
      "old_type": "Deployable", 
      "old_encrypted": false 
    } 
] 
} 
```

## CdmChangesetsApi - GET /sn\_cdm/changesets/commit-status/\{commit\_id\}

Returns the current status of the specified changeset commit request.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/commit-status/{commit_id}`

Default URL: `/api/sn_cdm/changesets/commit-status/{commit_id}`

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

commit\_id

</td><td>

Sys\_id for the commit request whose status to return. This value is returned by the [CdmChangesetsApi - POST /sn\_cdm/changesets/\{changeset\_id\}/commit](changesets-api.md#) endpoint.

Data type: String

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

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="cdm_apps-request_id-row"><td>

commit\_id

</td><td>

Commit request record sys\_id. Same as that passed into the endpoint.Data type: String

</td></tr><tr><td>

errors

</td><td>

Description of the error\(s\) encountered during upload.Data type: String

</td></tr><tr><td>

output

</td><td>

Description of the uploaded data or if an error occurred during the upload, an error message describing the error that was encountered.Data type: Object

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

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

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

-   committed
-   completed
-   error
-   in\_progress
-   new
-   ready

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

Current processing state of the commit request.Possible values:

-   NOT\_PROCREED
-   PROCESSED

Data type: String

</td></tr><tr id="cdm_apps-export_id-row"><td>

request\_id

</td><td>

Request ID. Same as that passed into the endpoint and **commit\_id**.Data type: String

</td></tr><tr id="cdm_apps-state-row"><td>

state

</td><td>

Current state of the specified commit.Possible values:

-   completed
-   error
-   in\_progress
-   new
-   ready

Data type: String

Table: Value from state column of the CDM Request Queue \[sn\_cdm\_request\_queue\] table.

</td></tr><tr><td>

type

</td><td>

Type of request.Possible values:

-   commit
-   export
-   upload\_and\_commit

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to obtain the status of the specified commit.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/commit-status/bf506e69537c3010a1d3ddeeff7b12c0"\ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

The following shows examples of a success and error response.

```

// Successful response 

{ 
  "result": { 
    "type": "commit", 
    "state": "completed", 
    "output": { 
      "sys_id": "4a4407e953124110da35ddeeff7b1235", 
      "number": "Chset-1207", 
      "title": "admin064407e953124110da35ddeeff7b1235", 
      "description": "A description of my changeset provided during creation", 
      "committed_at": "2022-03-17 22:19:33", 
      "committed_by": "6816f79cc0a8016401c5a33be04be441", 
      "sys_created_by": "admin", 
      "state": "committed", 
      "publish_option": "publish_none", 
      "auto_validate": false, 
      "snapshot_name": null, 
      "snapshot_description": null, 
      "cdm_application": "DemoApp", 
      "last_conflict_detection_time": null 
    }, 
    "processing_state": "PROCESSED", 
    "commit_id": "9cd583e953124110da35ddeeff7b128a" 
  } 
} 

 

// Example of an error response 

{ 
  "result": { 
    "state": "error", 
    "errors": "Invalid requestId '9cd583e953124110da35ddeeff7b128'", 
    "commit_id": "9cd583e953124110da35ddeeff7b128" 
  } 
} 


```

## CdmChangesetsApi - GET /sn\_cdm/changesets/impacted-deployables

Returns the list of deployables that are associated with a specified changeset.

The CDM Viewer role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/impacted-deployables`

Default URL: `/api/sn_cdm/changesets/impacted-deployables`

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

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

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

<table id="id_lcm_5dn_qtb"><thead><tr><th>

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

The following code example shows how to retrieve the impacted deployables for a specified changeset.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/impacted-deployables?changesetNumber=Chset-783" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
{ 
  "result": [ 
    { 
      "cmdb_ci": { 
        "value": "75c5d7a953b70110a1d3ddeeff7b12a2", 
        "link": "http://instance.servicenow.com/api/now/table/cmdb_ci_service_auto/75c5d7a953b70110a1d3ddeeff7b12a2" 
      }, 
      "cdi_count": "2", 
      "snapshot_version_counter": "3", 
      "description": null, 
      "sys_updated_on": "2022-06-29 16:19:05", 
      "environment_type": "Development", 
      "node": { 
        "value": "a1c517a953b70110a1d3ddeeff7b129b", 
        "link": "http://instance.servicenow.com/api/now/table/sn_cdm_node/a1c517a953b70110a1d3ddeeff7b129b" 
      }, 
      "sys_id": "6dc517a953b70110a1d3ddeeff7b129b", 
      "sys_updated_by": "admin", 
      "cdm_app": { 
        "value": "62b517a953b70110a1d3ddeeff7b128c", 
        "link": "http://instance.servicenow.com/api/now/table/sn_cdm_application/62b517a953b70110a1d3ddeeff7b128c" 
      }, 
      "sys_created_on": "2022-05-31 13:03:23", 
      "cdi_usage": "0.02", 
      "name": "Development_1", 
      "state": "active", 
      "sys_created_by": "admin" 
    } 
  ] 
}
```

## CdmChangesetsApi - GET /sn\_cdm/changesets/impacted-shared-components

Returns a list of shared components that are associated with a specified changeset.

The CDM Viewer role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/impacted-shared-components`

Default URL: `/api/sn_cdm/changesets/impacted-shared-components`

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

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

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

|Header|Description|
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

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cdm\_shared\_\_library

</td><td>

Sys\_id of the shared library under which the component resides.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the CDM shared component.Data type: String

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

name

</td><td>

Name of the CDM shared component.Data type: String

</td></tr><tr><td>

node

</td><td>

Sys\_id of the shared component node.Data type: String

Table: CDM Node \[sn\_cdm\_node\]

</td></tr><tr><td>

node\_main

</td><td>

Sys\_id of the main\_id of the shared component node record.Data type: String

Table: CDM Node Main \[sn\_cdm\_node\_main\]

</td></tr><tr><td>

state

</td><td>

Current state of the shared component.Possible values:

-   active
-   deleted

Data type: String

</td></tr><tr id="cdm_dep-sys_created_by-row"><td>

sys\_created\_by

</td><td>

User name of the user that create the CDM shared component. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_deps-sys_created_on-row"><td>

sys\_created\_on

</td><td>

Date and time when the CDM shared component was created.Format: YYYY-mm-DD hh:mm:ss

Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the shared component.Data type: String

Table: CDM Shared Component \[sn\_cdm\_shared\_component\]

</td></tr><tr id="cdm_dep-sys_updated_by-row"><td>

sys\_updated\_by

</td><td>

User name of the user that last updated the CDM shared component. For example, able.tuter.Data type: String

</td></tr><tr id="cdm_dep-sys_updated_on-row"><td>

sys\_updated\_on

</td><td>

Date and time when the CDM shared component was last updated.Format: YYYY-mm-DD hh:mm:ss

 Data type: String

</td></tr><tr><td>

version\_counter

</td><td>

Number of versions created for the shared component.Data type: Integer

</td></tr></tbody>
</table>### cURL request

The following code example shows how to retrieve the impacted shared components for changeset = "Chset-20".

```
curl "https://instance.servicenow.com/sn_cdm/changesets/impacted-shared-components?changesetNumber=Chset-20" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password' 

```

Response:

```
{
  "result": [
    {
      "version_counter": "1",
      "description": null,
      "cdm_shared_library": "acb905e097b3991052687b890353afcd",
      "sys_updated_on": "2022-12-12 20:28:49",
      "node": "3cb945e097b3991052687b890353af0d",
      "sys_id": "34b945e097b3991052687b890353af20",
      "sys_updated_by": "john.jones",
      "node_main": "74b945e097b3991052687b890353af0d",
      "sys_created_on": "2022-12-12 20:28:39",
      "name": "logonService-V2.1",
      "state": "active",
      "sys_created_by": "john.jones"
    },
    {
      "version_counter": "1",
      "description": null,
      "cdm_shared_library": "acb905e097b3991052687b890353afcd",
      "sys_updated_on": "2022-12-12 20:28:49",
      "node": "b0b945e097b3991052687b890353af11",
      "sys_id": "30b945e097b3991052687b890353af21",
      "sys_updated_by": "john.jones",
      "node_main": "f8b945e097b3991052687b890353af10",
      "sys_created_on": "2022-12-12 20:28:39",
      "name": "logonService-V2.2",
      "state": "active",
      "sys_created_by": "john.jones"
    },
    {
      "version_counter": "1",
      "description": null,
      "cdm_shared_library": "acb905e097b3991052687b890353afcd",
      "sys_updated_on": "2022-12-12 20:28:49",
      "node": "6cb905e097b3991052687b890353afd3",
      "sys_id": "b4b945e097b3991052687b890353af21",
      "sys_updated_by": "john.jones",
      "node_main": "a4b905e097b3991052687b890353afd3",
      "sys_created_on": "2022-12-12 20:28:39",
      "name": "paymentService-V1.0",
      "state": "active",
      "sys_created_by": "john.jones"
    },
    {
      "version_counter": "1",
      "description": null,
      "cdm_shared_library": "acb905e097b3991052687b890353afcd",
      "sys_updated_on": "2022-12-12 20:28:49",
      "node": "e0b905e097b3991052687b890353aff1",
      "sys_id": "3cb945e097b3991052687b890353af21",
      "sys_updated_by": "john.jones",
      "node_main": "2cb905e097b3991052687b890353aff0",
      "sys_created_on": "2022-12-12 20:28:39",
      "name": "paymentService-V1.1",
      "state": "active",
      "sys_created_by": "john.jones"
    }
  ]
}
```

## CdmChangesetsApi - GET /sn\_cdm/changesets/\{changeset\_id\}/impacted-deployables

Returns the list of deployables that are associated with a specified changeset.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/{changeset_id}/impacted-deployables`

Default URL: `/api/sn_cdm/changesets/{changeset_id}/impacted-deployables`

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

changeset\_id

</td><td>

Sys\_id of the changeset record to process.Data type: String

Table:CDM Changeset \[sn\_cdm\_changeset\]

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

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

changeset\_id

</td><td>

Sys\_id of the last changeset associated with the deployable node.Data type: String

</td></tr><tr><td>

conflict

</td><td>

Flag that indicates whether the associated deployable is in conflict.Possible values:

-   0: Not in conflict.
-   1: Conflicted - refer to the **conflict\_type** return result for additional information.

Data type: Number

</td></tr><tr><td>

conflict\_type

</td><td>

Type of deployable conflict.Possible values:

-   corrupted\_node
-   deleted\_node
-   duplicated\_node
-   incomplete\_deleted\_parent
-   incomplete\_deleted\_ref
-   incomplete\_renamed\_ref
-   invalid\_include
-   orphaned\_descendant
-   related\_conflict
-   unlinked\_include
-   unrenamed\_include
-   updated\_node

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the deployable node.Data type: String

</td></tr><tr><td>

effective\_from

</td><td>

Timestamp when the node is valid. This value is `null` until you commit a changeset in which the node was created.Data type: Number

</td></tr><tr><td>

effective\_to

</td><td>

Timestamp when the node is no longer valid. If this value is `null`, the node stays in affect until it is replaced with a new version.Data type: Number

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

level

</td><td>

Depth of the node starting from the application level, which is 0.Data type: Number

</td></tr><tr><td>

linked\_to

</td><td>

ID of the reference node within a collection and component.For example, the following node snippet shows a link between the collection collA and the component compA. For this example, the **linkedTo** value is `1`:

```
{ 
components : {compA:{} //MainId: 1}, 

Collections : { collA : {  
   compA :{} //Include, linkedTo: 1 
    } 
  } 
} 
```

Data type: String

</td></tr><tr><td>

main\_id

</td><td>

Unique identifier of the deployable node. This value is generated when the node is created and used to identify the deployable node.Data type: Number

</td></tr><tr><td>

main\_id\_encoded

</td><td>

Encoded value of the **mainId** return results, using Radix 57 string representation.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the deployable.Data type: String

</td></tr><tr><td>

node\_classifier

</td><td>

Node classification, such as Development, Production, or Test. In the format:

-   /application/deployables/env:Development
-   /application/deployables/env:Production
-   /application/deployables/env:Test

Data type: String

</td></tr><tr><td>

position

</td><td>

Deployable node position. Only applicable to arrays.For example, for the array:

```
node1:{
  arrayNode: [{}, "literal1", "literal2", []] }
```

\{\} is position 1000,

"literal1" is position 2000,

"literal2" is position 3000,

\[\] is position 4000

Data type: Number

</td></tr><tr><td>

previous\_version

</td><td>

Sys\_id of the previous version of the associated deployable node.Data type: String

</td></tr><tr><td>

restricted\_to

</td><td>

List of sys\_ids of the users that are allowed to access the associated deployable node. This value is `null` if all groups can access the deployable.Data type: String

Table: CDM Restricted Groups \[sn\_cdm\_restricted\_groups\]

</td></tr><tr><td>

secure\_value

</td><td>

Secure value of the CDI or variable. Only returned for leaf nodes and array literals. This is the same as the **value** return result, but is encrypted.Data type: String

</td></tr><tr><td>

status

</td><td>

Status of deployable node or the status of a failed request.Possible values:

-   deleted
-   failure \(passed if endpoint call fails.\)
-   new
-   superseded
-   updated
-   valid

Data type: String

</td></tr><tr><td>

system\_folder

</td><td>

Flag that indicates whether the associated folder is a system folder.Possible values:

-   0: Not a system folder.
-   1: System folder.

Data type: Number

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the impacted deployable.Data type: String

</td></tr><tr><td>

type

</td><td>

Node type, such as sn\_cdm\_node\_deployable. This value enables you to determine whether the node is a component, config data item \(CDI\), or deployable. This value is generated when the node is created.Data type: String

</td></tr><tr><td>

value

</td><td>

Value of the CDI or variable. Only returned for leaf nodes and array literals. If this information is encrypted, it is returned in the **secure\_value** return result.For example, if this node is the CDI `nodeA:{cdi1: 1}`, the **value** return result is `1`. If it is an array node such as `node1: {arrayNode: [{}, "literal1", "literal2", []]}`, the **value** return result is `literal1`.

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to request the deployables that are associated with the changeset whose sys\_id is bf506e69537c3010a1d3ddeeff7b12c0.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/bf506e69537c3010a1d3ddeeff7b12c0/impacted-deployables"\ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password' 
```

The following shows both a successful and an error response for this endpoint.

```
// Successful response
{
  "result": [
    {
      "sys_id": "833527a953924110da35ddeeff7b12c1",
      "type": "sn_cdm_node_deployable",
      "main_id": "150",
      "main_id_encoded": "&M",
      "node_path": "!&@!&D!&M",
      "level": 2,
      "status": "valid",
      "node_classifier": "/application/deployables/env:Development",
      "position": null,
      "restricted_to": null,
      "changeset_id": "cb3527a953924110da35ddeeff7b12c0",
      "previous_version": "e8946f6953924110da35ddeeff7b1264",
      "effective_from": "1647563806950",
      "effective_to": null,
      "name": "Development_1",
      "description": "dev deployable decription",
      "value": null,
      "secure_value": null,
      "system_folder": "0",
      "linked_to": null,
      "conflict": "0",
      "conflict_type": null
    },
    {
      "sys_id": "a245e7a953924110da35ddeeff7b1223",
      "type": "sn_cdm_node_deployable",
      "main_id": "153",
      "main_id_encoded": "&P",
      "node_path": "!&@!&D!&P",
      "level": 2,
      "status": "valid",
      "node_classifier": "/application/deployables/env:Test",
      "position": null,
      "restricted_to": null,
      "changeset_id": "ea45e7a953924110da35ddeeff7b1222",
      "previous_version": "9505ef6953924110da35ddeeff7b121a",
      "effective_from": "1647563821422",
      "effective_to": null,
      "name": "Test_1",
      "description": "test deployable decription",
      "value": null,
      "secure_value": null,
      "system_folder": "0",
      "linked_to": null,
      "conflict": "0",
      "conflict_type": null
    }
  ]
} 

// Example of an error response
{
  "error": {
    "message": "Error: Unexpected error occurred in create request.Error:Application not found",
    "detail": ""
  },
  "status": "failure"
}
```

## CdmChangesetsApi - POST /sn\_cdm/changesets/\{changeset\_id\}/commit

Commits the specified changeset. Once committed, the changeset is persisted into the CDM tables within the associated instance.

The system updates the application to persist the changes to the configuration data within the changeset. The changeset state changes to **Committed**. The system then generates a snapshot of each deployable that is affected by the changeset.

This endpoint returns the ID of the commit request. Use this ID to call the [CdmChangesetsApi - GET /sn\_cdm/changesets/commit-status/\{commit\_id\}](changesets-api.md#) endpoint to obtain the current status of the changeset commit.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/{changeset_id}/commit`

Default URL: `/api/sn_cdm/changesets/{changeset_id}/commit`

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

changeset\_id

</td><td>

Sys\_id of the changeset record to process.Data type: String

Table:CDM Changeset \[sn\_cdm\_changeset\]

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

autoValidate

</td><td>

Flag that indicates whether the snapshots created upon commit are validated, meaning any associated policies are run against the snapshot.Valid values:

-   true: Validate the snapshots.
-   false: Do not validate the snapshots.

Default: false

</td></tr><tr><td>

publishOption

</td><td>

Publish option for the associated configuration snapshots. Valid values:

-   publish\_none: Do not publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

**Note:** This option is only available if the value for the **autoCommit** parameter is true.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

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

Bad Request. Error: &lt;Error message&gt;Validate that the **changeset\_id** parameter that you passed in was correct.

Ensure that you have the required roles to access this endpoint.

</td></tr><tr><td>

500

</td><td>

Internal Server Error Error: Invalid boolean value.If you passed in the **autoValidate** parameter, verify that it is a boolean value.

</td></tr></tbody>
</table>### Response body parameters

<table id="id_bgt_byy_ztb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

commit\_id

</td><td>

Sys\_id of the commit request. Use this ID when calling the [CdmChangesetsApi - GET /sn\_cdm/changesets/commit-status/\{commit\_id\}](changesets-api.md#) endpoint to check the status of the commit request.

Data type: String

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

Status of the commit. Only returned when an error occurs.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to call this endpoint to commit a changeset record.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/29e24001533030104bacddeeff7b120c/commit?publishOption=publish_valid"\ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

The following shows the response for a successful changeset commit request.

```
// Successful response
{ 
  "result": { 
    "commit_id": "64b5f79f5379301096edddeeff7b12eb" 
  } 
}

// Example of an error response
{
  "error": {
    "message": "Error: Unexpected error occurred in commit request.Error:Failed to insert request in queue",
    "detail": ""
  },
  "status": "failure"
}
```

## CdmChangesetsApi - POST /sn\_cdm/changesets/create

Creates a new changeset in the open state for a specified CDM application or shared library.

The CDM Editor role is required to access this endpoint.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/create/`

Default URL: `/api/sn_cdm/changesets/create/`

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

</td><td id="appName-changesets-entry">

Required. Name of the CDM application or shared library to associate with this changeset. This must be an active application or shared library.Data type: String

</td></tr><tr><td>

description

</td><td>

Changeset description. Enter something that will allow others to understand the purpose of the changeset.Data type: String

 Default: None

</td></tr><tr><td>

returnFields

</td><td>

Comma separated list of fields in the CDM Changeset \[sn\_cdm\_changeset\] table to return as part of the response.Data type: String

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

Bad Request. Error: &lt;Error message&gt;Ensure that the specified CDM application or shared library exists and in the active state.

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

auto\_validate

</td><td>

Flag that indicates whether auto validation was performed.

 Possible values:

-   true: Auto validation was performed.
-   false: Auto validation was not preformed.

 Data type: Boolean

</td></tr><tr><td>

cdm\_application

</td><td>

Details about the CDM application associated with the changeset.Data type: Object

 ```
"cdm_application": { 
  "link": "String",
  "value": "String"
}
```

For example: `{"value": "<sysId>", "link": "http://localhost:8081/api/now/table/*’}"`

</td></tr><tr><td>

cdm\_application.link

</td><td>

URL of the associated CDM application.Data type: String

</td></tr><tr><td>

cdm\_application.value

</td><td>

Sys\_id of the associated CDM application.Data type: String

</td></tr><tr><td>

committed\_at

</td><td>

Date and time that the changeset was committed to the associated repository.Data type: String

</td></tr><tr><td>

committed\_by

</td><td>

Sys\_id of the entity that created the changeset.Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the changeset as passed when the endpoint was called.Data type: String

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

last\_conflict\_detection\_time

</td><td>

Last time conflict detection ran.Data type: Number

 Unit: Milliseconds

</td></tr><tr><td>

number

</td><td>

Unique identifier for the new changeset.Data type: String

</td></tr><tr><td>

publish\_option

</td><td>

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

</td></tr><tr><td>

snapshot\_description

</td><td>

Description of the snapshot associated with the changeset.Data type: String

</td></tr><tr><td>

state

</td><td>

State of the changeset creation.Possible values:

-   Blocked
-   Checking for conflict
-   Commit failed
-   Commit in progress
-   Committed
-   Open

 Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the changeset creation. Only returned when an error occurs.Possible values: failure

 Data type: String

</td></tr><tr><td>

sys\_created\_by

</td><td>

Sys\_id of the entity that created the changeset record.Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the new changeset.Data type: String

</td></tr><tr><td>

title

</td><td>

Title of the changeset associated with the application. Typically auto-generated by the system.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to create a changeset associated with the App Service1 CDM application.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/create?appName=App%20Service1&description=Sample%20Description \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \
--user 'username':'password' 
```

The following shows the response for a successful creation of the changeset.

```
// Example of a successful response
{   
"result": { 
    "sys_id": "42748779c370301054c1582e1340ddcd",
    "number": "Chset-8",
    "title": "admin2021-06-18 10:06:46",
    "description": null,
    "committed_at": "",
    "committed_by": null,
    "sys_created_by": "admin",
    "state": "open",
    "publish_option": "publish_none",
    "auto_validate": false,
    "snapshot_name": null,
    "snapshot_description": null,
    "cdm_application": "App%20Service1" 
  } 
}

// Example of an error response
{
  "error": {
    "message": "Error: Unexpected error occurred in create request.Error:Application not found",
    "detail": ""
  },
  "status": "failure"
}
```

### cURL request

The following example shows how to create a changeset for the shared library "javalib".

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/create?sharedLibraryName=javalib&description=description of changeset" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user 'username':'password'  
```

Response:

```

```

## CdmChangesetsApi - PUT /sn\_cdm/changesets/commit

Updates and commits a specified changeset.

The system updates the application to persist the changes to the configuration data within the changeset. The changeset state changes to **Committed**. The system then generates a snapshot of each deployable that is affected by the changeset.

This endpoint returns the ID of the commit request. Use this ID to call the [CdmChangesetsApi - GET /sn\_cdm/changesets/commit-status/\{commit\_id\}](changesets-api.md#) endpoint to obtain the current status of the changeset commit.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/changesets/{changeset_id}/commit`

Default URL: `/api/sn_cdm/changesets/{changeset_id}/commit`

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

autoValidate

</td><td id="autoValidate-changeset-entry">

Flag that indicates whether the snapshots created during the commit are validated, meaning any associated policies are run against the snapshot.Valid values:

-   true: Validate the snapshots.
-   false: Don't validate the snapshots.

Data type: Boolean

Default: false

</td></tr><tr><td>

changesetNumber

</td><td id="changesetNumber-changeset-entry">

Required. Unique identifier of the associated changeset, such as "Chset-10".

Data type: String

Table: CDM Changeset \[sn\_cdm\_changeset\]

</td></tr><tr><td>

publishOption

</td><td>

Publish option for the associated configured snapshots.

Valid values:

-   publish\_none: Don't publish any snapshots.
-   publish\_valid: Publish only those snapshots that pass validation after the commit.

For additional information on publishing snapshots, see [Publish or unpublish a snapshot](https://www.servicenow.com/docs/access?context=cdm-snapshot-publish&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

Data type: String

Default: publish\_none

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

Bad Request. Error: &lt;Error message&gt;Validate that the **changeset\_id** parameter that you passed in was correct.

 Ensure that you have the required roles to access this endpoint.

</td></tr><tr><td>

500

</td><td>

Internal Server Error: Invalid boolean value.If you passed in the **autoValidate** parameter, verify that it is a boolean value.

</td></tr></tbody>
</table>### Response body parameters

<table id="id_cjx_1yy_ztb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

commit\_id

</td><td>

Sys\_id of the commit request. Use this ID when calling the [CdmChangesetsApi - GET /sn\_cdm/changesets/commit-status/\{commit\_id\}](changesets-api.md#) endpoint to check the status of the commit request.

Data type: String

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

Status of the commit. Only returned when an error occurs.Possible values: failure

Data type: String

</td></tr></tbody>
</table>### cURL request

The follow code example shows how to use this endpoint to update a changeset.

```
curl "http://instance.servicenow.com/api/sn_cdm/changesets/commit?changesetNumber=Chset-146" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
{ 
  "result": { 
    "commit_id": "cca8190f53141110a1d3ddeeff7b129e" 
  } 
}
```

