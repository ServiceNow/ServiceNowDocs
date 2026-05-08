---
title: Digital Product Release API
description: The Digital Product Release API provides endpoints to manage releases and policy compliance.Retrieves release bundle details.Gets policy execution details by product for the current phase of a release.Creates an enhancement for a product or service.Creates a release.Creates a key date for a release.Executes mapped policies for the current phase of a release.Adds related tasks to a release.Creates a release calendar.Completes the current phase of a release.Creates a release readiness target or a set of recurring release readiness targets.Changes the readiness target for a release.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 35
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Digital Product Release API

The Digital Product Release API provides endpoints to manage releases and policy compliance.

This API requires the Digital Product Release \(sn\_dpr\) application, which is available on the ServiceNow Store. For more information, see Digital Product Release.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Digital Product Release - GET /sn\_dpr/digital\_product\_release/bundle/\{sysId\}

Retrieves release bundle details.

This endpoint can be extended to customize the fields and aggregated data returned in the response body. The default functionality of this endpoint is defined by the getReleaseBundleDetails\(\) method in the ReleaseBundleSNC script include. To customize the functionality, override the getReleaseBundleDetails\(\) method in the ReleaseBundle script include, which extends ReleaseBundleSNC. By default, aggregated data for enhancements, policies, release states, and task counts can be included in the response body.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin
-   sn\_dpr\_model.release\_coordinator
-   sn\_dpr\_model.release\_user

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/bundle/{sysId}`

Default URL: `/api/sn_dpr/digital_product_release/bundle/{sysId}`

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

sysId

</td><td>

Sys\_id of the release bundle.Table: Release Bundle \[sn\_dpr\_model\_release\_bundle\]

Data type: String

</td></tr></tbody>
</table><table class="rest_api_query_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sendAggregation

</td><td>

Flag that indicates whether to include aggregated data for enhancements, policies, release states, and task counts in the response body.Data type: Boolean

Valid values:

-   true: Return aggregates for enhancements, policies, release states, and task counts.
-   false: Don't return aggregates.

Default: false

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Authorization|Basic or bearer token for authentication.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

aggregates

</td><td>

Aggregated data for enhancements, policies, release states, and task counts. This parameter is only included in the response body if the **sendAggregation** query parameter is set to `true` in the request.

```
"aggregates": {
   "enhancementAggregate": {Object},
   "policyAggregate": {Object},
   "releaseAggregate": {Object},
   "taskAggregate": {Object}
}
```

Data type: Object

</td></tr><tr><td>

aggregates.enhancementAggregate

</td><td>

Lists the number of enhancements in each state.Data type: Object

```
"enhancementAggregate": {
   "Closed": Number,
   "Open": Number
}
```

</td></tr><tr><td>

aggregates.policyAggregate

</td><td>

Lists the number of policies in each execution status. Data type: Object

```
"policyAggregate": {
   "Executed": Number,
   "Pending": Number
}
```

</td></tr><tr><td>

aggregates.releaseAggregate

</td><td>

Lists the number of releases in each state. States are only included in this object if at least one release is in that state.Data type: Object

```
"releaseAggregate": {
   "Cancelled": Number,
   "Completed": Number,
   "Draft": Number,
   "In Progress": Number,
   "Pending": Number,
   "Restarting": Number,
   "Review": Number 
}
```

</td></tr><tr><td>

aggregates.taskAggregate

</td><td>

Lists the number of tasks that are approved and not approved.Data type: Object

```
"taskAggregate": {
   "approval": Number,
   "nonApproval": Number
}
```

</td></tr><tr><td>

name

</td><td>

Name of the release bundle.Data type: String

</td></tr><tr><td>

owner

</td><td>

Owner of the release bundle.Data type: String

</td></tr><tr><td>

releases

</td><td>

Data about the releases included in the bundle.```
"releases": {
   "count": Number,
   "list": [Array]
}
```

Data type: Object

</td></tr><tr><td>

releases.count

</td><td>

Number of releases included in the bundle.Data type: Number

</td></tr><tr><td>

releases.list

</td><td>

List of sys\_ids of releases included in the bundle.Table: Release \[sn\_dpr\_model\_release\]

Data type: Array

</td></tr><tr><td>

sysId

</td><td>

Sys\_id of the release bundle.Table: Release Bundle \[sn\_dpr\_model\_release\_bundle\]

Data type: String

</td></tr></tbody>
</table>### cURL request

This example retrieves details about a specified release bundle, including aggregated data for enhancements, policies, release states, and task counts.

```
curl -X GET \ "https://instance.service-now.com/api/sn_dpr/v1/digital_product_release/bundle/9d0d0b4c874b1110dba83d5ebf867de2?sendAggregation=true" \
--header "Accept: application/json" \ 
--header "Authorization: Basic <base64encoded-credentials>"
```

Response body.

```
{
   "sysId": "9d0d0b4c874b1110dba83d5ebf867de2",
   "name": "Release Bundle Q4",
   "owner": "jane.doe",
   "releases": {
      "count": 2,
      "list": ["rel1", "rel2"]
   },
   "aggregates": {
      "releaseAggregate": {
         "In Progress": 1,
         "Completed": 1
      },
      "taskAggregate": {
         "approval": 3,
         "nonApproval": 5
      },
      "policyAggregate": {
         "Executed": 2,
         "Pending": 1
      },
      "enhancementAggregate": {
         "Open": 1,
         "Closed": 1
      }
   }
}
```

## Digital Product Release - GET /sn\_dpr/digital\_product\_release/releases/\{releaseId\}/policies/status

Gets policy execution details by product for the current phase of a release.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin
-   sn\_dpr\_model.release\_coordinator
-   sn\_dpr\_model.release\_user

Before calling this endpoint, the release state must be **In Progress** and the current phase state must also be **In Progress**. You can view release information in the Digital Product Release Workspace in the **Releases** tab.

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/releases/{releaseId}/policies/status`

Default URL: `/api/sn_dpr/digital_product_release/releases/{releaseId}/policies/status`

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

releaseId

</td><td>

Sys\_id of the release.Table: Release \[sn\_dpr\_model\_release\]

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

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Object containing a compliance summary and product policy details.Data type: Object

```
"result": {
   "overallSummary": {Object},
   "products": [Array]
}
```

</td></tr><tr><td>

result.overallSummary

</td><td>

Policy compliance summary for the current release phase.Data type: Object

```
"overallSummary": {
   "compliant": Boolean,
   "compliantCount": Number,
   "currentPhase": "String",
   "nonCompliantCount": Number,
   "timestamp": "String",
   "totalCount": Number
}
```

</td></tr><tr><td>

result.overallSummary.compliant

</td><td>

Flag that indicates whether all evaluated policies for the current release phase are compliant.Valid values:

-   true: All evaluated policies are compliant.
-   false: Not all evaluated policies are compliant.

Data type: Boolean

</td></tr><tr><td>

result.overallSummary.compliantCount

</td><td>

Number of compliant policies.Data type: Number

</td></tr><tr><td>

result.overallSummary.currentPhase

</td><td>

Name of the current release phase.Data type: String

</td></tr><tr><td>

result.overallSummary.nonCompliantCount

</td><td>

Number of non-compliant policies.Data type: Number

</td></tr><tr><td>

result.overallSummary.timestamp

</td><td>

Date and time that policy compliance was last evaluated.Data type: String

</td></tr><tr><td>

result.overallSummary.totalCount

</td><td>

Total number of policies evaluated.Data type: Number

</td></tr><tr><td>

result.products

</td><td>

List of product-level compliance results. Each object in the array represents a product.

Data type: Array

```
"products": [
   {
      "policyExecutionDetails": [Array],
      "productId": "String",
      "productName": "String",
      "productVersion": "String",
      "summary": {Object}      
   }
]
```

</td></tr><tr><td>

result.products.policyExecutionDetails

</td><td>

List of executed policies with compliance results.Each object in the array represents a policy.

Data type: Array

```
"policyExecutionDetails": [
   {
      "executionOutput": "Check sum OK; 0 violations. Execution log id: e23-9a.",
      "lastRunAt": "2025-09-26T08:30:00Z",
      "name": "Policy Name 1",
      "policyId": "policyVersionSysId1",
      "reason": "All checks passed",
      "status": "compliant"  
   }
]
```

</td></tr><tr><td>

result.products.policyExecutionDetails.executionOutput

</td><td>

Output message produced by the policy execution.Data type: String

</td></tr><tr><td>

result.products.policyExecutionDetails.lastRunAt

</td><td>

Date and time the policy was last evaluated for compliance.Data type: String

</td></tr><tr><td>

result.products.policyExecutionDetails.name

</td><td>

Display name of the policy.Data type: String

</td></tr><tr><td>

result.products.policyExecutionDetails.policyId

</td><td>

Sys\_id of the policy.Table: Policy \[sn\_pace\_policy\]

Data type: String

</td></tr><tr><td>

result.products.policyExecutionDetails.reason

</td><td>

Message explaining the reason the policy is compliant or non-compliant.Data type: String

</td></tr><tr><td>

result.products.policyExecutionDetails.status

</td><td>

Compliance state for the policy.Valid values:

-   compliant
-   non\_compliant
-   not\_run

Data type: String

</td></tr><tr><td>

result.products.productId

</td><td>

Sys\_id of the product.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

result.products.productName

</td><td>

Display name of the product.Data type: String

</td></tr><tr><td>

result.products.productVersion

</td><td>

Version associated with the product for the current release.Data type: String

</td></tr><tr><td>

result.products.summary

</td><td>

Compliance results for the product.Data type: Object

```
"summary": {
   "compliant": Boolean,
   "compliantCount": Number,
   "nonCompliantCount": Number,
   "totalCount": Number
}
```

</td></tr><tr><td>

result.products.summary.compliant

</td><td>

Flag that indicates whether all policies for the product are compliant.Valid values:

-   true: All policies are compliant.
-   false: Not all policies are compliant.

Data type: Boolean

</td></tr><tr><td>

result.products.summary.compliantCount

</td><td>

Number of compliant policies.Data type: Number

</td></tr><tr><td>

result.products.summary.nonCompliantCount

</td><td>

Number of non-compliant policies.Data type: Number

</td></tr><tr><td>

result.products.summary.totalCount

</td><td>

Total number of policies evaluated for the product.Data type: Number

</td></tr></tbody>
</table>### cURL request

This example gets policy execution details for the current phase of the specified release.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/releases/d4982eeb474b621027d48b41516d4385/policies/status" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "overallSummary": {
         "compliant": false,
         "compliantCount": 3,
         "nonCompliantCount": 2,
         "totalCount": 5,
         "currentPhase": "Phase Name",
         "timestamp": "2025-09-26T09:15:00Z"
      },
      "products": [
         {
            "productId": "f8fe5fd40a0a0b9100f91d64df145295",
            "productName": "Payments Service",
            "productVersion": "v2.4.1",
            "summary": {
               "compliant": false,
               "compliantCount": 1,
               "nonCompliantCount": 1,
               "totalCount": 2
            },
            "policyExecutionDetails": [
               {
                  "name": "Policy Name 1",
                  "policyId": "f6783cc843590210ab16fc4bbcb8f223",
                  "status": "compliant",
                  "lastRunAt": "2025-09-26T08:30:00Z",
                  "executionOutput": "Check sum OK; 0 violations. Execution log id: e23-9a.",
                  "reason": "All checks passed"
               },
               {
                  "name": "Policy Name 2",
                  "policyId": "152bb04c43590210ab16fc4bbcb8f2a7",
                  "status": "non_compliant",
                  "lastRunAt": "2025-09-26T08:32:00Z",
                  "executionOutput": "Validation failed at step 3: required configuration missing.",
                  "reason": "Missing required configuration 'payments.retry_limit'"
               }
            ]
         }
      ]
   }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/product\_enhancement

Creates an enhancement for a product or service.

To access this endpoint, the caller must have the sn\_dpr\_model.product\_manager role.

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/product_enhancement`

Default URL: `/api/sn_dpr/digital_product_release/product_enhancement`

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

description

</td><td>

Description of the enhancement.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the enhancement.Data type: String

</td></tr><tr><td>

priority

</td><td>

Priority of the enhancement.Valid values:

-   high
-   medium
-   low

Default: medium

Data type: String

</td></tr><tr><td>

productFeatureSysId

</td><td>

Sys\_id of the product feature to associate with the enhancement.Table: Product Feature \[sn\_dpr\_model\_product\_feature\]

Data type: String

</td></tr><tr><td>

productSysId

</td><td>

Required. Sys\_id of the product or service to associate with the enhancement.Table: Application Model \[cmdb\_application\_product\_model\] or Service Model \[cmdb\_service\_product\_model\]

Data type: String

</td></tr><tr><td>

releaseSysId

</td><td>

Sys\_id of the release to add the enhancement.The release must be associated with the version provided in the **versionSysId** parameter.

Table: Release \[sn\_dpr\_model\_release\]

Data type: String

</td></tr><tr><td>

versionSysId

</td><td>

Sys\_id of the product version or service version to associate with the enhancement.The version must be for the same product or service provided in the **productSysId** parameter.

Table: Software Model \[cmdb\_software\_product\_model\] or Service Offering Model \[cmdb\_service\_offering\_model\]

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
|201|Created. The enhancement was successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_fv1_gmm_fhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "sysId": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.sysId

</td><td>

Sys\_id of the created enhancement.Table: Product Enhancement \[sn\_dpr\_model\_product\_enhancement\]

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a product enhancement.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/product_enhancement" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"name\":\"Offline streaming\", 
   \"productSysId\":\"de8e9c0dfff8f2108289ffffffffff61\", 
   \"priority\":\"high\", 
   \"description\":\"Enhancement description\", 
   \"versionSysId\":\"da4b608dff7cf2108289ffffffffffc2\", 
   \"releaseSysId\":\"9a4b608dff7cf2108289ffffffffffc3\", 
   \"productFeatureSysId\":\"192d2905ff7436108289ffffffffff3f\" 
}" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "error": false,
      "sysId": "76417985ff7436108289ffffffffff5f"
   }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release

Creates a release.

A release can be created as an independent release, or as a primary release that includes child releases. This endpoint can also be used to move an existing release from the Draft state to In Progress.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release`

Default URL: `/api/sn_dpr/digital_product_release/release`

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

autoCreateIncludedVersions

</td><td>

List of child release versions to automatically create.Data type: Array

```
"autoCreateIncludedVersions": [
   { 
      "product": "String", 
      "version": "String"
   } 
]
```

</td></tr><tr><td>

autoCreateIncludedVersions.product

</td><td>

Sys\_id of the product to use for the version.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

autoCreateIncludedVersions.version

</td><td>

Name of the version.Data type: String

</td></tr><tr><td>

autoCreateVersionName

</td><td>

Name of the version to automatically create.Data type: String

</td></tr><tr><td>

draftReleaseId

</td><td>

Sys\_id of the draft release.Use this parameter to move a release from the Draft state to In Progress.

Table: Release \[sn\_dpr\_model\_release\]

Data type: String

</td></tr><tr><td>

includedVersions

</td><td>

List of sys\_ids of existing product versions to include in the release.Table: System Component Model \[cmdb\_sw\_component\_model\]

Data type: Array

</td></tr><tr><td>

isDraftRelease

</td><td>

Flag that indicates whether to create the release in the Draft state.

 Valid values:

-   true: The release is created with the state set to Draft.
-   false: The release is created with the state set to In Progress.

 Default: False

 Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Required. Name of the release.Data type: String

</td></tr><tr><td>

productId

</td><td>

Required. Sys\_id of the product.Table: Product Model \[cmdb\_model\]

Data type: String

</td></tr><tr><td>

productVersion

</td><td>

Sys\_id of the product version.Table: System Component Model \[cmdb\_sw\_component\_model\]

Data type: String

</td></tr><tr><td>

releaseCalendar

</td><td>

Sys\_id of the release calendar.Table: Release Calendar \[sn\_dpr\_model\_release\_calendar\]

Data type: String

</td></tr><tr><td>

releaseDate

</td><td>

Release date in the format yyyy-MM-dd.Using this parameter creates a record in the Release Readiness Target \[sn\_dpr\_model\_release\_target\] table.

Data type: String

</td></tr><tr><td>

releaseDescription

</td><td>

Description of the release.Data type: String

</td></tr><tr><td>

releaseOwner

</td><td>

Required. Sys\_id of the release owner.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

releaseTarget

</td><td>

Sys\_id of the release readiness target.Table: Release Readiness Target \[sn\_dpr\_model\_release\_target\]

Data type: String

</td></tr><tr><td>

templateId

</td><td>

Sys\_id of the template to use for the release.Table: Release Template \[sn\_dpr\_model\_release\_template\]

Data type: String

</td></tr><tr><td>

validatesVersion

</td><td>

Flag that indicates whether the release validates a version.Valid values:

-   true: The release validates a version.
-   false: The release doesn't validate a version.

Default: False

Data type: Boolean

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
|201|Created. The release was successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON\)

<table id="table_fv1_gmm_fhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "message": "String",
   "progressId": "String",
   "releaseId": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Message containing details about the success or failure of the API request.Data type: String

</td></tr><tr><td>

result.progressId

</td><td>

Sys id of the tracker for the creation progress of the child release versions listed in the **autoCreateIncludedVersions** request parameter.Table: Progress Worker \[sys\_progress\_worker\]

Data type: String

</td></tr><tr><td>

result.releaseId

</td><td>

Sys\_id of the created primary release.Table: Release \[sn\_dpr\_model\_release\]

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a release with included versions.

```
curl "http://instance.service-now.com/api/sn_dpr/v1/digital_product_release/release" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"name\": \"Patch Q4\", 
  \"releaseTarget\": \"8071e5f8ff687a10509cffffffffffd9\", 
  \"releaseOwner\": \"6816f79cc0a8016401c5a33be04be441\", 
  \"releaseDescription\": \"Q4 release\", 
  \"productVersion\": \"\", 
  \"templateId\": \"c83134a4ff643a10509cffffffffffb5\", 
  \"releaseDate\": \"\", 
  \"releaseCalendar\": \"\", 
  \"includedVersions\": [ 
    \"39fd3f66ff503610509cffffffffff09\" 
  ], 
  \"productId\": \"c65c372bfb9d5610fdacfe7405efdcd7\", 
  \"autoCreateVersionName\": \"1.2\", 
  \"autoCreateIncludedVersions\": [ 
    { 
      \"product\": \"de66ea3833e966103e8361a9ed5c7b4e\", 
      \"version\": \"1.1\" 
    } 
  ] 
}" \ 
--user 'username':'password'
```

Response body.

```
{
  "result": { 
    "error": false, 
    "message": "", 
    "releaseId": "af90e98dff3c3210509cffffffffffc9", 
    "progressId": "f7902d01ffbc3210509cffffffffff7b" 
  } 
}
```

### cURL request

This example moves an existing release from the Draft state to In Progress.

```
curl "http://instance.service-now.com/api/sn_dpr/v1/digital_product_release/release" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"name\": \"Q4 2025 Product Release\", 
  \"releaseTarget\": \"077e1ffb97bc4e107bc2341de053afe2\", 
  \"releaseOwner\": \"6816f79cc0a8016401c5a33be04be441\", 
  \"releaseDescription\": \"\", 
  \"productVersion\": \"0ff12581ffbc3210509cffffffffff15\", 
  \"templateId\": \"648c6ca8ffe03a10509cffffffffff11\", 
  \"releaseDate\": \"\", 
  \"releaseCalendar\": \"\", 
  \"includedVersions\": [], 
  \"productId\": \"\", 
  \"autoCreateVersionName\": \"\", 
  \"autoCreateIncludedVersions\": [], 
  \"draftReleaseId\": \"83f12581ffbc3210509cffffffffff16\" 
}" \ 
--user 'username':'password'
```

Response body.

```
{ 
  "result": { 
    "error": false, 
    "message": "", 
    "releaseId": "83f12581ffbc3210509cffffffffff16" 
  } 
}
```

### cURL request

This example creates an independent release.

```
curl "http://instance.service-now.com/api/sn_dpr/v1/digital_product_release/release" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"name\": \"Q2 2026 patch\", 
  \"productVersion\": null, 
  \"releaseTarget\": \"008b84a1ffe4ba10509cffffffffff2c\", 
  \"releaseDescription\": \"\", 
  \"releaseOwner\": \"6816f79cc0a8016401c5a33be04be441\", 
  \"productId\": \"012c6d20ff203210229bffffffffff25\", 
  \"autoCreateVersionName\": \"2.4\", 
  \"templateId\": \"648c6ca8ffe03a10509cffffffffff11\", 
  \"releaseDate\": \"\", 
  \"releaseCalendar\": \"\", 
  \"isDraftRelease\": false, 
  \"validatesVersion\": true 
}" \ 
--user 'username':'password'
```

Response body.

```
{ 
  "result": { 
    "error": false, 
    "message": "", 
    "releaseId": "c6f52181ffbc3210509cffffffffffc0" 
  } 
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/key\_date

Creates a key date for a release.

Key dates are used to track deadlines, milestones, and other important events during the release.

Before calling this endpoint, a timeline-oriented release must be created. A timeline-oriented release has fixed deadlines and follows a strict schedule, while a stage-oriented release is primarily focused on completing objectives and features rather than meeting due dates.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin
-   sn\_dpr\_model.release\_coordinator

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release/{releaseId}/key_date`

Default URL: `/api/sn_dpr/digital_product_release/release/{releaseId}/key_date`

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

releaseId

</td><td>

Sys\_id of the release.Table: Release \[sn\_dpr\_model\_release\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assignedTo

</td><td>

Sys\_id of the user assigned to the key date.The user must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin
-   sn\_dpr\_model.release\_coordinator
-   sn\_dpr\_model.release\_user

Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

description

</td><td>

Description of the key date.Data type: String

</td></tr><tr><td>

duedate

</td><td>

Required. Due date that the event or objective must be completed by. The due date must be between the release planned start and end dates.

Format: yyyy-MM-dd

Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the key date.Data type: String

</td></tr><tr><td>

state

</td><td>

Required. State of the key date.Valid values:

-   archived
-   missed
-   upcoming

Data type: String

</td></tr><tr><td>

type

</td><td>

Required. Type of key date.Valid values:

-   deadline
-   important\_date
-   key\_event
-   milestone

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
|201|Created. The key date was successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_fv1_gmm_fhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "keyDateSysId": "String",
   "message": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.keyDateSysId

</td><td>

Sys\_id of the created key date.Table: Release Key Date \[sn\_dpr\_model\_release\_key\_date\]

Data type: String

</td></tr><tr><td>

result.message

</td><td>

Message containing details about the success or failure of the API request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a project launch date for a specified release.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release/eb7dd11d97b402107bc2341de053af34/key_date" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{ 
    \"name\": \"Project Launch\", 
    \"type\": \"milestone\", 
    \"dueDate\": \"2025-11-01\", 
    \"state\": \"upcoming\", 
    \"description\": \"Launching the new project phase.\", 
    \"assignedTo\": \"62826bf03710200044e0bfc8bcbe5df1\" 
}" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "error": false,
      "message": "Release key date created successfully",
      "keyDateSysId": "eb0b0905ff7036108289ffffffffff6d"
   }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/policies/run

Executes mapped policies for the current phase of a release.

To access this endpoint, the caller must have the sn\_dpr\_model.product\_manager role.

Before calling this endpoint, the release state must be **In Progress** and the current phase state must also be **In Progress**. You can view release information in the Digital Product Release Workspace in the **Releases** tab.

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release/{releaseId}/policies/run`

Default URL: `/api/sn_dpr/digital_product_release/release/{releaseId}/policies/run`

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

releaseId

</td><td>

Sys\_id of the release.Table: Release \[sn\_dpr\_model\_release\]

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
|201|Created. The release phase policies are scheduled to be run.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_fv1_gmm_fhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "errorCode": "String",
   "message": "String",
   "policyExecutionScheduled": Boolean
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.errorCode

</td><td>

HTTP status code for the request.Data type: String

</td></tr><tr><td>

result.message

</td><td>

Message containing details about the success or failure of the API request.Data type: String

</td></tr><tr><td>

result.policyExecutionScheduled

</td><td>

Flag that indicates whether the release phase policies are scheduled to be run.Valid values:

-   true: Release phase policies are scheduled to be run.
-   false: Release phase policies aren't scheduled to be run.

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

This example executes the mapped policies for the current phase of the specified release.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release/d4982eeb474b621027d48b41516d4385/policies/run" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "error": false,
      "errorCode": "",
      "message": "Policy execution scheduled.",
      "policyExecutionScheduled": true
   }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release/\{releaseId\}/related\_task

Adds related tasks to a release.

You can view release information in the Digital Product Release Workspace in the Releases tab. Related tasks for a release are shown in the Release Scope section of a release record.

**Important:** Before calling this endpoint, there must be existing task records that can be added as related tasks for the release. The records must be in tables that extend the Task \[task\] table, but not in the Task table itself. In the **sn\_dpr\_model.release\_related\_task\_types** system property, list the tables that contain your task records.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release/{releaseId}/related_task`

Default URL: `/api/sn_dpr/digital_product_release/release/{releaseId}/related_task`

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

releaseId

</td><td>

Sys\_id of the release.Table: Release \[sn\_dpr\_model\_release\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

taskIds

</td><td>

Required. List of task sys\_ids to add as related tasks for the release. The task records must be from tables listed in the **sn\_dpr\_model.release\_related\_task\_types** system property. For more information, see Digital Product Release properties.

Data type: Array

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
|201|Created. The related tasks were successfully added to the release.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_fv1_gmm_fhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "message": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Message containing details about the success or failure of the API request.Data type: String

</td></tr></tbody>
</table>### cURL request

This example adds two related tasks to a release.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release/eb7dd11d97b402107bc2341de053af34/related_task" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"taskIds\": [\"36836028532023004247ddeeff7b12f1\", \"bc84b11dff5c32108289ffffffffff12\"]}" \
--user 'username':'password'
```

Response body.

```
{
   "result": {
      "error": false,
      "message": "Successfully created the mappings between the release and all the tasks."
   }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release\_calendar

Creates a release calendar.

To access this endpoint, the caller must have the sn\_dpr\_model.release\_calendar\_admin role.

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release_calendar`

Default URL: `/api/sn_dpr/digital_product_release/release_calendar`

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

description

</td><td>

Description of the release calendar.Data type: String

</td></tr><tr><td>

name

</td><td>

Required. Name of the release calendar.Data type: String

</td></tr><tr><td>

releaseAdmin

</td><td>

Required. Sys\_id of the release calendar owner.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

schedules

</td><td>

Comma-separated list of schedule sys\_ids to use for the release calendar. For example, `"sysId1,sysId2,sysId3"`.Table: Schedule \[cmn\_schedule\]

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Only supports **application/json**.|
|Authorization|Basic or bearer token for authentication.|
|Content-Type|Data format of the request body. Only supports **application/json**.|

|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|201|Created. The release calendar was successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|
|401|Unauthorized. The user credentials are incorrect or have not been passed.|

### Response body parameters \(JSON\)

<table id="table_fv1_gmm_fhc"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "message": "String",
   "releaseCalendarId": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Message containing details about the success or failure of the API request.Data type: String

</td></tr><tr><td>

result.releaseCalendarId

</td><td>

Sys\_id of the created release calendar.Table: Release Calendar \[sn\_dpr\_model\_release\_calendar\]

Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a release calendar.

```
curl 'https://instance.service-now.com/api/sn_dpr/v1/digital_product_release/release_calendar' \ 
--request POST \
--header 'Accept:application/json' \
--header 'Content-Type: application/json' \ 
--header 'Authorization: Basic <base64encoded-credentials>' \ 
--data '{ 
    "name": "Q1 2025 Release Calendar123", 
    "releaseAdmin": "dc6770ae3b97a210532fb50f23e45a33", 
    "description": "Calendar for Q1 releases" 
}'
```

Response body.

```
{
   "result": {
      "error": false,
      "message": "",
      "releaseCalendarId": "5f6702c13bbc3a50532fb50f23e45a2b"
   }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release\_id/\{releaseId\}/complete\_phase

Completes the current phase of a release.

**Note:** The current phase is only set to **Completed** if all policies for the phase are compliant.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin
-   sn\_dpr\_model.release\_coordinator

Before calling this endpoint, the release state must be **In Progress** and the current phase state must also be **In Progress**. You can view release information in the Digital Product Release Workspace in the **Releases** tab.

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release_id/{releaseId}/complete_phase`

Default URL: `/api/sn_dpr/digital_product_release/release_id/{releaseId}/complete_phase`

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

releaseId

</td><td>

Sys\_id of the release.Table: Release \[sn\_dpr\_model\_release\]

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
|201|Created. The release phase was successfully completed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. The elements included in this object depend on whether the request succeeded or failed.Data type: Object

Success object.

```
"result": {
   "message": "String",
   "phaseSysId": "String",
   "status": "String",
}
```

Error object.

```
"result": {
   "error": Boolean,
   "message": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.This parameter is only returned if the request failed so the only possible value is `true`.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Message containing details about the success or failure of the API request.Data type: String

</td></tr><tr><td>

result.phaseSysId

</td><td>

Sys\_id of the release phase.Table: Release Phase \[sn\_dpr\_model\_release\_phase\]

Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the API request. This parameter is only returned if the request was successful so the only possible value is `success`.

Data type: String

</td></tr></tbody>
</table>### cURL request

This example completes the current phase of the specified release.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release_id/d4982eeb474b621027d48b41516d4385/complete_phase" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "status": "success",
    "message": "Release phase is marked as complete",
    "phaseSysId": "2498222f474b621027d48b41516d4342"
  }
}
```

### cURL request

This example shows an error response when an invalid release sys\_id is provided.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release_id/a/complete_phase" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

Error response.

```
{
  "result": {
    "error": true,
    "message": "Release ID is invalid"
  }
}
```

## Digital Product Release - POST /sn\_dpr/digital\_product\_release/release\_target

Creates a release readiness target or a set of recurring release readiness targets.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release_target`

Default URL: `/api/sn_dpr/digital_product_release/release_target`

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

description

</td><td>

Description of the readiness target.Data type: String

</td></tr><tr><td>

endDate

</td><td>

End date for a recurring readiness target. Required if **isRecurring** is `true`.Data type: String

</td></tr><tr><td>

isRecurring

</td><td>

Required. Flag that indicates whether the readiness target is recurring.Valid values:

-   true: The target is recurring.
-   false: The target is a single date.

Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Required. Name of the release readiness target.Data type: String

</td></tr><tr><td>

releaseAdmin

</td><td>

Required. Sys\_id of the readiness target owner.Table: User \[sys\_user\]

Data type: String

</td></tr><tr><td>

releaseCalendar

</td><td>

Required. Sys\_id of the release calendar for the readiness target.Table: Release Calendar \[sn\_dpr\_model\_release\_calendar\]

Data type: String

</td></tr><tr><td>

repeats

</td><td>

Sets the schedule for a recurring readiness target. Required if **isRecurring** is `true`.Data type: Object

```
"repeats": {
   "daysOfWeek": Number,
   "every": Number,
   "type": "String"
}
```

</td></tr><tr><td>

repeats.daysOfWeek

</td><td>

Number of working days in a week.Data type: Number

</td></tr><tr><td>

repeats.every

</td><td>

Number of intervals between each date. Used with **repeats.type** to define the frequency the target recurs.In this example, the target recurs every two weeks.

```
"repeats": {
   "every": 2,
   "type": "weekly"
}
```

Data type: Number

</td></tr><tr><td>

repeats.type

</td><td>

Type of interval between each date. Used with **repeats.every** to define the frequency the target recurs.Valid values:

-   weekly
-   monthly

Data type: String

</td></tr><tr><td>

scheduleSysId

</td><td>

Sys\_id of the schedule to use for the release target.Table: Schedule \[cmn\_schedule\]

Data type: String

</td></tr><tr><td>

startDate

</td><td>

Required. Date for the readiness target, or the first date of a recurring readiness target.Data type: String

</td></tr><tr><td>

targetsWithOverlappingScheduleDetails

</td><td>

List of dates for a recurring readiness target.Data type: Array

```
"targetsWithOverlappingScheduleDetails": [ 
   { 
      "active": Boolean, 
      "date": "String" 
   }
]
```

</td></tr><tr><td>

targetsWithOverlappingScheduleDetails.active

</td><td>

Flag that indicates whether the readiness target recurrence is active.Valid values:

-   true: Active.
-   false: Inactive.

Data type: Boolean

</td></tr><tr><td>

targetsWithOverlappingScheduleDetails.date

</td><td>

Date for the readiness target recurrence.Data type: String

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
|201|Created. Release target\(s\) successfully created.|
|400|Bad Request. A bad request type or malformed request was detected.|

### Response body parameters \(JSON\)

<table id="table_ndx_qsy_j3c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "count": Number,
   "error": Boolean,
   "message": "String"
}
```

</td></tr><tr><td>

result.count

</td><td>

Number of release targets created by the API request.Data type: Number

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Error message. This parameter is empty for successful requests.Data type: String

</td></tr></tbody>
</table>### cURL request

This example creates a set of four release readiness targets, with a target recurring every week on Friday.

```
curl "http://instance.service-now.com/api/sn_dpr/digital_product_release/release_target" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"name\": \"Weekly Friday patch\", 
  \"releaseAdmin\": \"6816f79cc0a8016401c5a33be04be441\", 
  \"isRecurring\": true, 
  \"description\": \"\", 
  \"startDate\": \"2025-10-24\", 
  \"releaseCalendar\": \"d3d1f3b4ff60ba10509cffffffffffa8\", 
  \"endDate\": \"2025-11-19\", 
  \"repeats\": { 
    \"type\": \"weekly\", 
    \"every\": 1, 
    \"daysOfWeek\": 5 
  }, 
  \"scheduleSysId\": \"b862d589ff3c3210509cffffffffff97\", 
  \"targetsWithOverlappingScheduleDetails\": [ 
    { 
      \"active\": true, 
      \"date\": \"2025-10-24\" 
    }, 
    { 
      \"active\": true, 
      \"date\": \"2025-10-31\" 
    }, 
    { 
      \"active\": true, 
      \"date\": \"2025-11-07\" 
    }, 
    { 
      \"active\": true, 
      \"date\": \"2025-11-14\" 
    } 
  ] 
}" \ 
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "error": false,
    "message": "",
    "count": 4
  }
}
```

### cURL request

This example creates a release readiness target for a specified date.

```
curl "http://instance.service-now.com/api/sn_dpr/digital_product_release/release_target" \ 
--request POST \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{ 
  \"name\": \"Fourth Thursday patch\", 
  \"releaseAdmin\": \"6816f79cc0a8016401c5a33be04be441\", 
  \"isRecurring\": false, 
  \"description\": \"Last Thursday of October\", 
  \"startDate\": \"2025-10-30\", 
  \"releaseCalendar\": \"d3d1f3b4ff60ba10509cffffffffffa8\" 
}" \ 
--user 'username':'password' 
```

Response body.

```
{
  "result": {
    "error": false,
    "message": "",
    "count": 1
  }
}
```

## Digital Product Release - PUT /sn\_dpr/digital\_product\_release/release/\{sysId\}/retarget

Changes the readiness target for a release.

The new readiness target can be an existing readiness target that is already defined, or an out-of-band date \(a one-time readiness target not tied to the standard release calendar\). To set an out-of-band date, the **sn\_dpr.out\_of\_band\_release\_allowed** system property must be set to `true`.

The release phase duration is adjusted to reflect the new readiness target.

Before calling this endpoint, the release state must be **In Progress** or **Pending**.

To access this endpoint, the caller must have one of the following roles.

-   sn\_dpr\_model.product\_manager
-   sn\_dpr\_model.release\_admin

### URL format

Versioned URL: `/api/sn_dpr/{api_version}/digital_product_release/release/{sysId}/retarget`

Default URL: `/api/sn_dpr/digital_product_release/release/{sysId}/retarget`

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

sysId

</td><td>

Sys\_id of the release.Table: Release \[sn\_dpr\_model\_release\]

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

outOfBand

</td><td>

Flag that indicates whether the readiness target is an out-of-band date \(a one-time readiness target not tied to the standard release calendar\).This parameter is required if **releaseTarget ** is not used.

Valid values:

-   true: The readiness target is out-of-band.
-   false: The readiness target is already defined and tied to the standard release calendar.

Default: False

Data type: Boolean

</td></tr><tr><td>

releaseCalendar

</td><td>

Sys\_id of the release calendar to use for the readiness target. Required if using **outOfBand**.Table: Release Calendar \[sn\_dpr\_model\_release\_calendar\]

Data type: String

</td></tr><tr><td>

releaseDate

</td><td>

Date for the readiness target. Required if using **outOfBand**.Data type: String

</td></tr><tr><td>

releaseTarget 

</td><td>

Sys\_id of the release readiness target.Use this parameter to select an existing readiness target. Either this parameter or **outOfBand** is required to set the new target.

Table: Release Readiness Target \[sn\_dpr\_model\_release\_target\]

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
|200|Successful. The request was successfully processed.|
|400|Bad Request. A bad request type or malformed request was detected.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_ndx_qsy_j3c"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the API request. Data type: Object

```
"result": {
   "error": Boolean,
   "message": "String"
}
```

</td></tr><tr><td>

result.error

</td><td>

Flag that indicates whether there is an error with the API request.Possible values:

-   true: Error.
-   false: No error.

Data type: Boolean

</td></tr><tr><td>

result.message

</td><td>

Error message. This parameter is empty for successful requests.Data type: String

</td></tr></tbody>
</table>### cURL request

This example updates the release readiness target using an existing readiness target.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release/9b2e7ec9476c8e105b8e0dcfe16d43d4/retarget" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"releaseTarget\": \"3f6668e95427fd10f877ac7ac399daa6\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "error": false,
    "message": ""
  }
}
```

### cURL request

This example updates the release readiness target using an out-of-band readiness target.

```
curl "https://instance.service-now.com/api/sn_dpr/digital_product_release/release/9b2e7ec9476c8e105b8e0dcfe16d43d4/retarget" \
--request PUT \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"outOfBand\": true,
   \"releaseCalendar\": \"fcb2eaa09f4302105c534d837a0a1c2b\",
   \"releaseDate\": \"2026-10-23\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "error": false,
    "message": ""
  }
}
```

