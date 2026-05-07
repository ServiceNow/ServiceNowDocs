---
title: User Role Inheritance API
description: The User Role Inheritance API provides endpoints that allow you to see the roles that a specific user inherited.Returns a specified user's granted and inherited roles.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-05-06"
reading_time_minutes: 2
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# User Role Inheritance API

The User Role Inheritance API provides endpoints that allow you to see the roles that a specific user inherited.

This API requires the Contextual Security: Role Management V2 REST API \(com.glide.role\_management.inh\_count.rest\_api\) plugin, automatically activated on new instances starting with the Jakarta release, or the Contextual Security: Role Management Enhancements REST API plugin, automatically activated starting with the Geneva release. The Contextual Security: Role Management V2 REST API is dependent on the Contextual Security: Role Management V2 \(com.glide.role\_management.inh\_count\) plugin.

A user’s role can be directly granted, inherited from other roles, or inherited from groups. You must have the user\_admin role to access this API.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## User Role Inheritance - GET /global/user\_role\_inheritance

Returns a specified user's granted and inherited roles.

### URL format

Versioned URL: `/api/global/{api_version}/user_role_inheritance`

Default URL: `/api/global/user_role_inheritance`

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
</table>|Name|Description|
|----|-----------|
|user\_sysid|Required. Sys\_id of the user for which to return role information.|

|Name|Description|
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
|401|Unauthorized. The user credentials are incorrect or have not been passed.|
|404|Not found. The requested item wasn't found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

from\_group

</td><td>

List of roles that are inherited from groups that have roles.Data type: Array

</td></tr><tr><td>

from\_role

</td><td>

List of roles that are either granted directly or inherited from other roles.Data type: Array

</td></tr><tr><td>

user\_name

</td><td>

Full name of user.Data type: String

</td></tr></tbody>
</table>### Sample cURL request

```
curl "https://instance.service-now.com/api/global/user_role_inheritance?user_sysid=62826bf03710200044e0bfc8bcbe5df1" \
--request GET \
--header "Accept:application/json" \
--user "username":"password"

```

```
{
  "result": {
    "user_name": "abel.tuter",
    "from_group": [
      "[Azure Operators]/sn_azure.operator",
      "[Azure Operators]/sn_azure.operator/sn_azure.user"
    ],
    "from_role": [
      "/snc_internal",
      "/cloud_user",
      "/cloud_user/pa_viewer",
      "/cloud_user/sn_azure.user",
      "/cloud_user/aws_user"
    ]
  }
}
```

