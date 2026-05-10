---
title: CdmPoliciesApi
description: The CdmPoliciesApi provides endpoints that enable you to manage policy mappings of deployables in Configuration Data Management \(CDM\). Policies that are properly mapped to a deployable are executed when a snapshot of the deployable is validated.Deletes the mapping of a specified policy to a deployable.Returns the resolved inputs for a specified policy mapping of a deployable.Maps a specified policy to a deployable.Updates the additionalDeployablesInput input variable of a Configuration Data Management \(CDM\) policy mapping.Updates a specified input variable for a Configuration Data Management \(CDM\) policy mapping.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# CdmPoliciesApi

The CdmPoliciesApi provides endpoints that enable you to manage policy mappings of deployables in Configuration Data Management \(CDM\). Policies that are properly mapped to a deployable are executed when a snapshot of the deployable is validated.

You must have one of the following roles to access the endpoints in this API:

-   Scripted REST CDM View ACL
-   Scripted REST CDM Admin ACL

In addition, the Configuration Data Management \(CDM\) plugin must be activated for this API to be available in an instance.

For additional information on policy mappings, see [Map policies to a deployable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-deployable-map-policy-to.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## CdmPoliciesApi - DELETE /sn\_cdm/policies/mappings

Deletes the mapping of a specified policy to a deployable.

The caller of this endpoint must have the CDM Admin role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/policies/mappings`

Default URL: `/api/sn_cdm/policies/mappings`

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

</th></tr></thead><tbody><tr id="appName-policy-row"><td>

appName

</td><td id="appName-policy-entry">

Required. Name of the Configuration Data Management \(CDM\) application for which to remove the mapping to the policy.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr id="deployableName-policy-row"><td>

deployableName

</td><td id="deployableName-policy-entry">

Required. Name of the CDM deployable for which to remove the mapping to the policy.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

policyName

</td><td id="policyName-policy-entry">

Required. Name of the associated policy.Data type: String

Table: Policy \[sn\_pace\_policy\]

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
|400|Bad Request. The **policyName** parameter passed is invalid.|
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

</td></tr></tbody>
</table>### cURL request

The following code example shows how to remove a policy mapping.

```
curl "http://instance.servicenow.com/api/sn_cdm/policies/mappings?deployableName=Development_1&policyName=testALPolicy1&appName=testApp" \ 
--request DELETE \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

For a successful deletion of the mapping, no response is returned other than the HTTP status code.

```
None - results defined by the HTTP status code
```

## CdmPoliciesApi - GET /sn\_cdm/policies/mappings/inputs/resolved

Returns the resolved inputs for a specified policy mapping of a deployable.

For additional information on policy mappings, see [Map policies to a deployable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-deployable-map-policy-to.md) and [Validating and correcting configuration data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-validating-cfg-data.md).

The caller of this endpoint must have the CDM Viewer role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/policies/mappings/inputs/resolved`

Default URL: `/api/sn_cdm/policies/mappings/inputs/resolved`

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

</th></tr></thead><tbody><tr id="appName-policy-row"><td>

appName

</td><td>

Required. Name of the Configuration Data Management \(CDM\) application associated with the deployable for which to return the resolved policy inputs.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr id="deployableName-policy-row"><td>

deployableName

</td><td>

Required. Name of the CDM deployable for which to return the resolved policy.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

policyName

</td><td id="policyName-policy-entry">

Required. Name of the associated policy.Data type: String

Table: Policy \[sn\_pace\_policy\]

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
|400|Bad Request. The **policyName** parameter passed is invalid.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Name-value pair list of all resolved inputs for the specified policy mapping. For example: `{"input_name": "user_1", "input_password": "" }`

 Data type: Object

</td></tr></tbody>
</table>### cURL request

The following example shows how to use this endpoint to obtain the resolved policy inputs.

```
curl "http://instance.servicenow.com/api/sn_cdm/policies/mappings/inputs/resolved?policyName=testALPolicy1&deployableName=Development_1&appName=testApp" \ 
--request GET \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return result:

```
{ 
  "result": { 
    "key1": "someVal", 
    "additionalDeployablesInput": "[{\"id\":\"e7e34a531b501110636e0fe0604bcba9\",\"label\":\"testApp-Development_2\"}]" 
  } 
}
```

## CdmPoliciesApi - POST /sn\_cdm/policies/mappings

Maps a specified policy to a deployable.

The caller of this endpoint must have the CDM Admin role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/policies/mappings`

Default URL: `/api/sn_cdm/policies/mappings`

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
</table><table id="id_ds3_yyg_15b" class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr id="appName-policy-row"><td>

appName

</td><td id="appName-policy-entry">

Required. Name of the Configuration Data Management \(CDM\) application for which to map the policy.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr id="deployableName-policy-row"><td>

deployableName

</td><td id="deployableName-policy-entry">

Required. Name of the CDM deployable for which to map the policy.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr id="policyName-policy-row"><td>

policyName

</td><td id="policyName-policy-entry">

Required. Name of the associated policy.Data type: String

Table: Policy \[sn\_pace\_policy\]

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

<table id="id_b5l_rbh_15b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

description

</td><td>

Description of the mapping.Data type: String

</td></tr><tr><td>

document

</td><td>

Sys\_id of the document.Data type: String

</td></tr><tr><td>

document\_ref

</td><td>

Details of the document\_ref record associated with the node. Data type: Object

```
"document_ref": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

document\_ref.link

</td><td>

Call syntax for querying the deployable record mapped to the policy using the Table REST API.PaCE uses this field to store the reference to the deployable that is mapped to a policy.

Data type: String

</td></tr><tr><td>

document\_ref.sys\_id

</td><td>

Sys\_id of the deployable record mapped to the policy.Data type: String

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

exception

</td><td>

If there's an exception while trying to perform the mapping, the link to the exception record.Data type: String

</td></tr><tr><td>

exception\_allowed

</td><td>

Flag that indicates whether exceptions are allowed for the policy.Possible values:

-   true: Exceptions are allowed.
-   false: Exceptions aren't allowed.

Data type: Boolean

</td></tr><tr><td>

input\_status

</td><td>

Status of the inputs.Possible values:

-   invalid
-   valid

Data type: String

</td></tr><tr><td>

last\_updated\_by

</td><td>

Details of the user that last updated the policy mapping. Data type: Object

```
"last_updated_by": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

last\_updated\_by.link

</td><td>

Call syntax for querying the user record using the Table REST API.Data type: String

</td></tr><tr><td>

last\_updated\_by.sys\_id

</td><td>

Sys\_id of the user record.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

number

</td><td>

Unique number that identifies the mapping. This value provides a human-readable identifier for the mapping.Data type: String

</td></tr><tr><td>

policy

</td><td>

Details of the policy record associated with the mapping. Data type: Object

```
"policy": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

policy.link

</td><td>

Call syntax for querying the policy record mapped to the policy using the Table REST API.Data type: String

</td></tr><tr><td>

policy.sys\_id

</td><td>

Sys\_id of the policy record.Data type: String

Table: Policy \[sn\_pace\_policy\]

</td></tr><tr><td>

reason

</td><td>

Description of the reason for the current state.Data type: String

</td></tr><tr><td>

state

</td><td>

Current state of the mapping.Possible values:

-   active
-   inactive

Data type: String

</td></tr><tr><td>

sys\_class\_name

</td><td>

Table name of the policy mapping.Data type: String

</td></tr><tr id="sys_created_by-policies-row"><td>

sys\_created\_by

</td><td id="sys_created_by-policies-entry">

Name of the user that created the mapping.Data type: String

</td></tr><tr id="sys_created_on-policies-row"><td>

sys\_created\_on

</td><td id="sys_created_onpolicies-entry">

Date and time when the mapping was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr id="sys_id-policies-row"><td>

sys\_id

</td><td id="sys_id-policies-entry">

Sys\_id of the mapping.Data type: String

Table: Policy Mapping \[sn\_pace\_policy\_mapping\]

</td></tr><tr id="sys_updated_by-policies-row"><td>

sys\_updated\_by

</td><td id="sys_updated_by-policies-entry">

Name of the user that updated the mapping.Data type: String

</td></tr><tr id="sys_updated_on-policies-row"><td>

sys\_updated\_on

</td><td id="sys_updated_on-policies-entry">

Date and time when the mapping was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>### cURL request

This code example shows how to map a specific policy to a deployable.

```
curl "http://instance.servicenow.com/api/sn_cdm/policies/mappings?appName=testApp&deployableName=Development_1&policyName=testALPolicy1" \ 
--request POST \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
{ 
  "result": { 
    "exception": null, 
    "reason": null, 
    "exception_allowed": "--", 
    "document": "0be34a531b501110636e0fe0604bcb21", 
    "input_status": "valid", 
    "description": null, 
    "sys_updated_on": "2022-06-30 14:07:37", 
    "sys_class_name": "sn_cdm_pace_policy_mapping", 
    "sys_id": "ea24469f1b101110636e0fe0604bcbed", 
    "number": "MAP0001001", 
    "last_updated_by": { 
      "value": "48630e131b501110636e0fe0604bcb53", 
      "link": "https://instance.servicenow.com/api/now/table/sys_user/48630e131b501110636e0fe0604bcb53" 
    }, 
    "sys_updated_by": "admin", 
    "sys_created_on": "2022-06-30 14:07:37", 
    "document_ref": { 
      "value": "0be34a531b501110636e0fe0604bcb21", 
      "link": "https://instance.servicenow.com/api/now/table/sn_cdm_deployable/0be34a531b501110636e0fe0604bcb21" 
    }, 
    "state": "active", 
    "sys_created_by": "admin", 
    "policy": { 
      "value": "12a3c2531b501110636e0fe0604bcb9b", 
      "link": "https://instance.servicenow.com/api/now/table/sn_pace_policy/12a3c2531b501110636e0fe0604bcb9b" 
    } 
  } 
}
```

## CdmPoliciesApi - PUT /sn\_cdm/policies/mappings/inputs/additional-deployables

Updates the additionalDeployablesInput input variable of a Configuration Data Management \(CDM\) policy mapping.

The additionalDeployablesInput input variable contains the additional deployables you can assign to an existing policy mapping. They are similar to mapping inputs, but they have a specific array structure.

For additional information on policy mappings, see [Map policies to a deployable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-deployable-map-policy-to.md).

The caller of this endpoint must have the CDM Admin role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/policies/mappings/inputs/additional-deployables`

Default URL: `/api/sn_cdm/policies/mappings/inputs/additional-deployables`

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

Required. List of deployables to add to the additionalDeployablesInput input variable.Data type: Array of Objects

 ```
"additionalDeployables": [
  {
    "appName": "String", 
    "deployableName": "String"
  }
]
```

</td></tr><tr><td>

additionalDeployables.appName

</td><td>

Required. Name of the CDM application to which the deployable is associated.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr><td>

additionalDeployables.deployableName

</td><td>

Required. Name of the CDM deployable to add to the additionalDeployablesInput input variable.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr id="appName-policy-row"><td>

appName

</td><td>

Required. Name of the CDM application for which to update the additionalDeployablesInput input variable.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr id="deployableName-policy-row"><td>

deployableName

</td><td>

Required. Name of the CDM deployable for which to update the additionalDeployablesInput input variable.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

policyName

</td><td id="policyName-policy-entry">

Required. Name of the associated policy.Data type: String

Table: Policy \[sn\_pace\_policy\]

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
|400|Bad Request. The **policyName** parameter passed is invalid.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_jx1_px2_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

io\_definition

</td><td>

Details about the associated PaCE IO definition record.For additional information on PaCE, see [Policy as Code Engine \(PaCE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-managing-policies.md).

Data type: Object

```
"io_definition": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

io\_definition.link

</td><td>

Call syntax for querying this PaCE IO definition record using the Table REST API.Data type: String

</td></tr><tr><td>

io\_definition.value

</td><td>

Sys\_id of the PaCE IO definition record. Data type: String

Table: IO Mapping \[sn\_pace\_io\_mapping\]

</td></tr><tr><td>

is\_unused

</td><td>

Flag that indicates whether the mapping input variable is unused.Possible values:

-   true: Associated mapping input variable isn't currently used.
-   false: Associated mapping input variable is currently used.

Data type: Boolean

</td></tr><tr><td>

mapped\_value

</td><td>

Current value of the mapping input variable.Data type: Array of Objects or String

</td></tr><tr><td>

policy\_mapping

</td><td>

Details about the PaCE policy-mapping record.For additional information on PaCE, see [Policy as Code Engine \(PaCE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-managing-policies.md).

Data type: Object

```
"policy_mapping": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

policy\_mapping.link

</td><td>

Call syntax for querying the policy mapping record using the Table REST API.Data type: String

</td></tr><tr><td>

policy\_mapping.value

</td><td>

Sys\_id of the PaCE policy-mapping record.Data type: String

Table: Policy Mapping \[sn\_pace\_policy\_mapping\]

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the mapping input variable.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time when the mapping input variable was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the associated mapping record.Data type: String

Table: IO Mapping \[sn\_pace\_io\_mapping\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that updated the mapping input variable.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time when the mapping input variable was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>### cURL request

The following example shows how to add deployables to an additionalDeployablesInput input variable.

```
curl "https://instance.servicenow.com/api/sn_cdm/policies/mappings/inputs/additional-deployables?additionalDeployables=%5B%7B%22appName%22%3A%20%22testApp%22%2C%20%22deployableName%22%3A%22Development_2%22%7D%5D&policyName=testALPolicy1&deployableName=Development_1&appName=testApp" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'admin':'admin
```

Return result:

```
{ 
  "result": { 
    "sys_id": "6bb746171b501110636e0fe0604bcb1c", 
    "policy_mapping": { 
      "value": "6bb746171b501110636e0fe0604bcb1b", 
      "link": "https://instance.servicenow.com/api/now/table/sn_cdm_pace_policy_mapping/6bb746171b501110636e0fe0604bcb1b" 
    }, 
    "sys_updated_by": "ameya", 
    "sys_created_on": "2022-06-30 14:23:15", 
    "io_definition": { 
      "value": "4d0b061b1b501110636e0fe0604bcb2f", 
      "link": "https://instance.servicenow.com/api/now/table/sn_pace_io_definition/4d0b061b1b501110636e0fe0604bcb2f" 
    }, 
    "mapped_value": "[{\"id\":\"e7e34a531b501110636e0fe0604bcba9\",\"label\":\"testApp-Development_2\"}]", 
    "sys_updated_on": "2022-06-30 14:53:21", 
    "sys_created_by": "ameya", 
    "is_unused": false 
  } 
} 
```

## CdmPoliciesApi - PUT /sn\_cdm/policies/mappings/inputs

Updates a specified input variable for a Configuration Data Management \(CDM\) policy mapping.

For additional information on policy mappings, see [Map policies to a deployable](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-family/cdm-deployable-map-policy-to.md).

The caller of this endpoint must have the CDM Admin role.

### URL format

Versioned URL: `/api/sn_cdm/{api_version}/policies/mappings/inputs`

Default URL: `/api/sn_cdm/policies/mappings/inputs`

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

</th></tr></thead><tbody><tr id="appName-policy-row"><td>

appName

</td><td>

Required. Name of the CDM application for which to update the policy mapping inputs.Data type: String

Table: CDM Application \[sn\_cdm\_application\]

</td></tr><tr id="deployableName-policy-row"><td>

deployableName

</td><td>

Required. Name of the CDM deployable for which to update the policy mapping inputs.Data type: String

Table: CDM Deployable \[sn\_cdm\_deployable\]

</td></tr><tr><td>

inputName

</td><td>

Required. Name of the input variable to update.Data type: String

Table: IO Mapping \[sn\_pace\_io\_mapping\]

</td></tr><tr><td>

inputValue

</td><td>

Required. Value to assign to the input variable.Data type: Dependant on the input variable. You can find the data type in the IO Mapping \[sn\_pace\_io\_mapping\] table.

</td></tr><tr><td>

policyName

</td><td id="policyName-policy-entry">

Required. Name of the associated policy.Data type: String

Table: Policy \[sn\_pace\_policy\]

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
|400|Bad Request. The **policyName** parameter passed is invalid.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters

<table id="id_tny_nx2_c5b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

io\_definition

</td><td>

Details about the associated PaCE IO definition record.For additional information on PaCE, see [Policy as Code Engine \(PaCE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-managing-policies.md).

Data type: Object

```
"io_definition": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

io\_definition.link

</td><td>

Call syntax for querying this PaCE IO definition record using the Table REST API.Data type: String

</td></tr><tr><td>

io\_definition.value

</td><td>

Sys\_id of the PaCE IO definition record. Data type: String

Table: IO Mapping \[sn\_pace\_io\_mapping\]

</td></tr><tr><td>

is\_unused

</td><td>

Flag that indicates whether the mapping input variable is unused.Possible values:

-   true: Associated mapping input variable isn't currently used.
-   false: Associated mapping input variable is currently used.

Data type: Boolean

</td></tr><tr><td>

mapped\_value

</td><td>

Current value of the mapping input variable.Data type: Array of Objects or String

</td></tr><tr><td>

policy\_mapping

</td><td>

Details about the PaCE policy-mapping record.For additional information on PaCE, see [Policy as Code Engine \(PaCE\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/policy-as-code-engine-pace/pace-managing-policies.md).

Data type: Object

```
"policy_mapping": {
  "link": "String",
  "value": "String"
}
```

</td></tr><tr><td>

policy\_mapping.link

</td><td>

Call syntax for querying the policy mapping record using the Table REST API.Data type: String

</td></tr><tr><td>

policy\_mapping.value

</td><td>

Sys\_id of the PaCE policy-mapping record.Data type: String

Table: Policy Mapping \[sn\_pace\_policy\_mapping\]

</td></tr><tr><td>

sys\_created\_by

</td><td>

Name of the user that created the mapping input variable.Data type: String

</td></tr><tr><td>

sys\_created\_on

</td><td>

Date and time when the mapping input variable was created.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the associated mapping record.Data type: String

Table: IO Mapping \[sn\_pace\_io\_mapping\]

</td></tr><tr><td>

sys\_updated\_by

</td><td>

Name of the user that updated the mapping input variable.Data type: String

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time when the mapping input variable was last updated.Data type: String

Format: yyyy-mm-dd hh:mm:ss

</td></tr></tbody>
</table>### cURL request

The following example shows how to update the key1 input variable associated with the testALPolicy.

```
curl "http://instance.servicenow.com/api/sn_cdm/policies/mappings/inputs?policyName=testALPolicy1&appName=testApp&inputValue=value1&inputName=key1&deployableName=Development_1" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--user 'username':'password'
```

Return results:

```
{ 
  "result": { 
    "sys_id": "631b861b1b501110636e0fe0604bcb6f", 
    "policy_mapping": { 
      "value": "6bb746171b501110636e0fe0604bcb1b", 
      "link": "https://instance.servicenow.com/api/now/table/sn_cdm_pace_policy_mapping/6bb746171b501110636e0fe0604bcb1b" 
    }, 
    "sys_updated_by": "admin", 
    "sys_created_on": "2022-06-30 14:38:00", 
    "io_definition": { 
      "value": "fe1b061b1b501110636e0fe0604bcb90", 
      "link": "https://instance.servicenow.comm/api/now/table/sn_pace_io_definition/fe1b061b1b501110636e0fe0604bcb90" 
    }, 
    "mapped_value": "someVal", 
    "sys_updated_on": "2022-06-30 14:39:21", 
    "sys_created_by": "admin", 
    "is_unused": false 
  } 
}
```

