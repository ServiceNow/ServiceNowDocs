---
title: Reassign Assessment - PATCH /\{userId\}
description: Reassigns an assessment instance to a different user. Use this endpoint when you need to transfer ownership of an in-progress assessment from the current assignee to another user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/api-reference/rest-apis/reassignassessment-PATCH-userId.html
release: australia
product: REST APIs
classification: rest-apis
topic_type: reference
last_updated: "2019-10-16"
reading_time_minutes: 3
breadcrumb: [Reassign Assessment API, REST API reference, API reference, API implementation and reference]
---

# Reassign Assessment - PATCH /\{userId\}

Reassigns an assessment instance to a different user. Use this endpoint when you need to transfer ownership of an in-progress assessment from the current assignee to another user.

The assessment must be in the “Open” state to be reassigned. This endpoint updates the primary owner on the assessment instance persona record, effectively changing who is responsible for completing the assessment.

Common use cases include:

-   Transferring assessment responsibility when an employee changes roles or leaves the organization.
-   Correcting an incorrectly assigned assessment.
-   Delegating assessment completion to a more appropriate team member.

**Note:** The requesting user must have write access to the assessment’s persona assignment record to perform the reassignment.

## URL format

Versioned URL: `PATCH /api/sn_smart_asmt/{api_version}/instance/asmt/{asmtInstanceId}/user/{userId}`

Default URL: `PATCH /api/sn_smart_asmt/instance/asmt/{asmtInstanceId}/user/{userId}`

## Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

api\_version

</td><td id="version-entry-RESTAPI">

Optional. Version of the endpoint to access. For example, `v1` or `v2`. Only specify this value to use an endpoint version other than the latest. Data type: String

</td></tr><tr><td>

asmtInstanceId

</td><td>

Required. Sys\_id of the assessment instance to reassign.Table: Assessment Instance \[sn\_smart\_asmt\_instance\]

Maximum length: 32

Data type: String

</td></tr><tr><td>

userId

</td><td>

Required. Sys\_id of the user to whom the assessment will be reassigned. Table: User \[sys\_user\]

Maximum length: 32

Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

## Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

|Header|Description|
|------|-----------|
|Accept|Data format of the response body. Supported values: application/json, application/xml, text/xml. Default: application/json.|
|Authorization|Authentication credentials. Use Basic authentication with base64-encoded username:password, or an OAuth 2.0 bearer token.|
|Content-Type|Not required for this endpoint as there is no request body, but if provided, supported values are: application/json, application/xml, text/xml.|

|Header|Description|
|------|-----------|
|Content-Type|Data format of the response body. Matches the Accept header value or defaults to application/json.|
|X-Is-Logged-In|Flag that indicates whether the requesting user is logged in. Possible values: true, false.|
|X-Transaction-ID|Unique identifier for the transaction, useful for debugging and support requests.|

## Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-api-explorer/c_RESTAPI.md).

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

Success. The assessment was successfully reassigned to the specified user. No response body is returned.

</td></tr><tr><td>

400

</td><td>

Bad Request. The request is missing required path parameters. Possible error messages:

-   `Assessment id is not passed.`
-   `User id is not passed.`

</td></tr><tr><td>

403

</td><td>

Forbidden. The requesting user doesn't have authorization to reassign this assessment. This occurs when the user lacks write access to the assessment’s persona assignment record.Error message: `User not authorized to reassign.`

</td></tr><tr><td>

404

</td><td>

Not Found. The specified resource doesn't exist. Possible error messages:

-   `Assessment instance not found.`
-   `User not found.`
-   `Persona assignment record for assessor is not available for the assessment.`

</td></tr><tr><td>

406

</td><td>

Not acceptable. The reassignment can't be completed due to business rule constraints. Possible error messages:

-   `Assessment can’t be reassigned as it's not in {state_name} state` - Assessment must be in Open state.
-   `Assessment can’t be reassigned as it's already assigned to the current user`
-   `Unable to reassign the assessment` - Generic failure during update.

</td></tr></tbody>
</table>## Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Object

</td><td>

Return object containing results of the reassignment.```
{
  "error": {Object},
  "status": "String"
}
```

</td></tr><tr><td>

error

</td><td>

Object containing error details.Data type: Object

```
"error": {
  "detail": "String",
  "message": "String"
  }
```

</td></tr><tr><td>

error.message

</td><td>

Human-readable description of the error that occurred. Examples:

-   `Assessment ID isn't passed.`
-   `User not authorized to reassign.`
-   `Assessment instance not found.`

 Data type: String

</td></tr><tr><td>

error.detail

</td><td>

Additional details about the error, if available. May be empty.Data type: String

</td></tr><tr><td>

status

</td><td>

Indicates the outcome of the request. Possible values: `"failure"` \(when an error occurs\). Successful responses \(HTTP 200\) return an empty body with no status field.

</td></tr></tbody>
</table>## cURL request

This PATCH example reassigns the assessment with ID `4d812fed47f8835060b5e65d416d431a` to the user with ID `62826bf03710200044e0bfc8bcbe5df1`.

```
curl "https://testsae.service-now.com/api/sn_smart_asmt/instance/asmt/4d812fed47f8835060b5e65d416d431a/user/62826bf03710200044e0bfc8bcbe5df1" \
--request PATCH \
--header "Accept:application/json" \
--user 'admin':'admin'
```

Response:

```
{
  "error": {
    "message": "Assessment can't be reassigned as it is already assigned to the current user",
    "detail": ""
  },
  "status": "failure"
}
```

**Parent Topic:**[Reassign Assessment API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/reassign-assessment-api.md)

