---
title: Help Request API
description: The Help Request API provides an endpoint to track supervisor help actions.Creates or updates a supervisor help action.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Help Request API

The Help Request API provides an endpoint to track supervisor help actions.

This API records supervisor help for agents working on interactions, including the help start and end time and the type of help. For more information about help requests, see [Agent help request for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/agent-help-request-for-voice-calls.md).

This API requires the Interactions Management plugin \(com.glide.interaction\). The calling user must have the interaction\_integration\_user role.

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Help Request - POST /now/helprequest/action/create\_or\_update

Creates or updates a supervisor help action.

Call this endpoint when a supervisor accepts an interaction help request. A record to track the help is created in the Supervisor Help Action \[supervisor\_help\_action\] table. Call this endpoint again when the supervisor completes their help to update the help action record with the end time.

### URL format

Versioned URL: `/api/now/{api_version}/helprequest/action/create_or_update`

Default URL: `/api/now/helprequest/action/create_or_update`

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

action

</td><td>

Type of assistance provided by the supervisor. Required when creating a supervisor help action.Valid values \(case sensitive\):

-   barge\_in
-   coach
-   monitor
-   observe

For additional information about supervisor actions, see [Monitoring calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/call-monitoring.md).

Data type: String

</td></tr><tr><td>

action\_sys\_id

</td><td>

Sys\_id of the supervisor help action. Required when updating a single specified supervisor help action, but can be excluded to bulk update all supervisor help actions for an interaction.

Table: Supervisor Help Action \[supervisor\_help\_action\]

Data type: String

</td></tr><tr><td>

end\_time

</td><td>

Date and time the supervisor ended assistance.**Note:** To update a single specified supervisor help action with an end time, a valid value must be provided for this parameter. However, when bulk updating all supervisor help actions for an interaction, excluding this parameter sets the current time as the end time.

Data type: String

</td></tr><tr><td>

help\_request

</td><td>

Sys\_id of the interaction help request.Table: Interaction Help Request \[interaction\_help\_request\]

Data type: String

</td></tr><tr><td>

interaction

</td><td>

Required. Sys\_id of the interaction.Table: Interaction \[interaction\]

Data type: String

</td></tr><tr><td>

start\_time

</td><td>

Date and time the supervisor started assistance.Default: Creation date and time of the supervisor help action record.

Data type: String

</td></tr></tbody>
</table>### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-entry-RESTAPI">

Data format of the response body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

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

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Details about the result of the API request.Data type: Object

```
"result": {
   "action_sys_id": "String",
   "message": "String",
   "success": Boolean  
}
```

</td></tr><tr><td>

result.action\_sys\_id

</td><td>

Sys\_id of the created or updated supervisor help action.Table: Supervisor Help Action \[supervisor\_help\_action\]

Data type: String

</td></tr><tr><td>

result.message

</td><td>

Message with details about the success or failure of the API request.Data type: String

</td></tr><tr><td>

result.success

</td><td>

Flag that indicates whether the API request was successful.Possible values:

-   true: Success
-   false: Failure

Data type: Boolean

</td></tr></tbody>
</table>### cURL request

This example creates a supervisor help action.

```
curl "https://instance.service-now.com/api/now/helprequest/action/create_or_update" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"interaction\": \"d4dec70f3b4bfe101baa9f7e53e45a5d\",
   \"action\": \"coach\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "success": true,
    "message": "Supervisor help action created successfully",
    "action_sys_id": "d25f034f3b4bfe101baa9f7e53e45a9f"
  }
}
```

### cURL request

This example updates a supervisor help action with an end time.

```
curl "https://instance.service-now.com/api/now/helprequest/action/create_or_update" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"interaction\": \"d4dec70f3b4bfe101baa9f7e53e45a5d\",
   \"action_sys_id\": \"d25f034f3b4bfe101baa9f7e53e45a9f\",
   \"end_time\": \"2026-02-18 11:30:00\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "success": true,
    "message": "Supervisor help action updated successfully",
    "action_sys_id": "d25f034f3b4bfe101baa9f7e53e45a9f"
  }
}
```

### cURL request

This example updates all supervisor help actions for an interaction with an end time.

```
curl "https://instance.service-now.com/api/now/helprequest/action/create_or_update" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"interaction\": \"cd87db433bcbfe101baa9f7e53e45a4d\",
   \"end_time\": \"2026-02-18 11:24:18\"
}" \
--user 'username':'password'
```

Response body.

```
{
  "result": {
    "success": true,
    "message": "end_time updated for all supervisor help actions associated with the interaction id: cd87db433bcbfe101baa9f7e53e45a4d"
  }
}
```

