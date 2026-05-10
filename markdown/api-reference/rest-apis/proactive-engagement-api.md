---
title: Proactive Engagement API
description: The Proactive Engagement API provides an endpoint for creating digital experience issues.Creates an experience issue when an issue is detected on the user's endpoint. Updates the Experience Issues \[sn\_pren\_experience\_issue\] table.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Proactive Engagement API

The Proactive Engagement API provides an endpoint for creating digital experience issues.

This API is available as a custom scripted REST API. It requires the Proactive Engagement \(proactive-engagement\) plugin and sn\_pren.experience\_issue\_create role. This API belongs to the `sn_pren` namespace.

Use the Proactive Engagement API to create an experience issue when an issue is detected on a user’s instance. The created experience issue drives engagement with the user and helps them self-resolve the issue.

To use this API, ensure the following tables are populated with records:

-   Issue Registry Template \[sn\_pren\_issue\_registry\_template\]
-   Issue Registry \[sn\_pren\_issue\_registry\]
-   Resolution \[sn\_pren\_resolution\]
-   Notification Content \[sn\_pren\_notification\_content\]
-   Provider \[sn\_pren\_provider\]

For more information, see [Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/proactive-engagement/proactive-engagement-landing-page.md)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Proactive Engagement - CREATE /api/sn\_pren/self\_remediation/experience\_issue/create

Creates an experience issue when an issue is detected on the user's endpoint. Updates the Experience Issues \[sn\_pren\_experience\_issue\] table.

### URL format

Default URL: `/api/sn_pren/self_remediation/experience_issue/create`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

endpoint

</td><td>

Required. Configuration item \(CI\) and user information used to detect issue details. **Note:** All parameters within this object are optional. You must pass at least one parameter within the object to identify the user or device."

Data type: Object

```
"endpoint": {
  "CI": "String",
  "email": "String",
  "user_id": "String",
  "user_name": "String"
}
```

</td></tr><tr><td>

endpoint.CI

</td><td>

Sys\_id of the CI device on which the issue was detected.Data type: String

Table: Computer \[cmdb\_ci\_computer\]

</td></tr><tr><td>

endpoint.email

</td><td>

Email address of the user for whom the issue was detected.Data type: String

</td></tr><tr><td>

endpoint.user\_id

</td><td>

Sys\_id of the user for whom the issue was detected.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

endpoint.user\_name

</td><td>

User name of the user for whom the issue was detected.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

experience\_id

</td><td>

User-defined ID to assign to the created issue.Data type: Number

Default: An ID is automatically generated.

</td></tr><tr><td>

input\_parameters

</td><td>

Parameters to pass to the action that will be executed on the device. The input parameters sent are passed to the configured resolution-remedial action such as a sub flow, flow action, or CI action. Data type: Object

```
"input_parameters": {
  "process_id": "String"
}
```

</td></tr><tr><td>

input\_parameters.process\_id

</td><td>

Sys\_id of the process to terminate or restart. Data type: String

</td></tr><tr><td>

investigative\_details

</td><td>

Details that could be useful for a manual investigation if the Power Usage Effectiveness \(PUE\) resolution fails. The investigative details are copied over to the incident which is created as a fallback when the PUE resolution fails.Data type: Object

```
"investigative_details": {
  "cpu_usage": "String",
  "processes_running": "String",
  "available_memory": "String"
  }
```

</td></tr><tr><td>

investigative\_details.cpu\_usage

</td><td>

CPU usage on the device. Data type: Number \(parsed as a string\)

</td></tr><tr><td>

investigative\_details.processes\_running

</td><td>

Number of processes running on the device.Data type: Number \(parsed as a string\)

</td></tr><tr><td>

investigative\_details.available\_memory

</td><td>

Available memory on the device.Data type: Number \(parsed as a string\)

</td></tr><tr><td>

issue\_code

</td><td>

Required. Issue code to associate with the problem. The issue code must be available and deployed in the instance. The API returns an error if an empty or invalid issue is provided.Data type: String

Table: Issue Registry \[sn\_pren\_issue\_registry\]

</td></tr><tr><td>

provider

</td><td>

Required. Unique code for the provider. This code must match the **provider\_code** field in the sn\_pren\_provider table on the instance.Data type: String

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

</td></tr></tbody>
</table><table class="rest_api_response_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content-Type

</td><td id="content_type-entry-RESTAPI">

Data format of the request body. Supported types: **application/json** or **application/xml**. Default: **application/json**

</td></tr></tbody>
</table>### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

<table id="table_wrm_33x_4zb"><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

An experience issue was created successfully.

</td></tr><tr><td>

400

</td><td>

Invalid request. Provide endpoint details. An empty **endpoint** object was sent in the request.

</td></tr><tr><td>

400

</td><td>

Invalid issue code, please provide a valid issue code. An empty **issue\_code** was sent in the request.

</td></tr><tr><td>

400

</td><td>

Invalid provider, please provide a valid provider. An empty provider was sent in the request.

</td></tr><tr><td>

400

</td><td>

Invalid issue code or provider, please provide valid details. Issue can't be detected in the instance. Verify **issue\_code** and **provider** details.

</td></tr><tr><td>

400

</td><td>

Issue code does not have a proper resolution. A valid resolution is not configured in the PUE framework for the issue identified.

</td></tr><tr><td>

400

</td><td>

Could not resolve user from endpoint details, please provide valid details. This error is returned if the PUE framework ID is unable to identify the user from the given endpoint details.

</td></tr><tr><td>

400

</td><td>

An experience issue is being resolved with given issue code for specified user. The specified experience issue is currently in an in-progress or open state.

</td></tr><tr><td>

400

</td><td>

Existing experience issue with given **experience\_id** is still under execution or is closed. This error occurs when an experience issue is in a chaining scenario. For instance, if a new **issue\_code** key is sent with an existing **experience\_id**, and the earlier experience issue is running or is in closed state.

The experience issue with this experience\_id must be in action\_wait state to send a new issue\_code with the previous experience\_id.

</td></tr><tr><td>

400

</td><td>

Error occurred while creating experience issue. This indicates a technical error.

</td></tr></tbody>
</table>### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

experienceId

</td><td>

Experience ID of the created experience issue. Generated from the **experience\_id** request parameter.If the **experience\_id** parameter is not passed, the resultant ID is always the sys\_id of the created record.

Table: Experience Issues \[sn\_pren\_experience\_issue\]

</td></tr></tbody>
</table>### cURL request

The following example creates an experience issue for user Abel Tuter. The issue code in the body allows Proactive Engagement to identify the resolution from the Issue Registry Template and engage with the end-user via Virtual Agent to help them self-solve the issue.

```
curl  "http://instance.servicenow.com//api/sn_srf/self_remediation/experience_issue/create" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
--data “{
  "endpoint": {
    "CI": "d049b28e936aa1106f98f6db5cba10d5",
    "user_id": "62826bf03710200044e0bfc8bcbe5df1",
    "user_name": "abel.tuter",
    "email": ""
  },
  "issue_code": "100",
  "provider": "sn",
  "experience_id": "09ed4830f393739df33",
  "input_parameters": {
    "process_id": "10644"
  },
  "investigative_details": {
    "cpu usage": "78%",
    "processes running": "35",
    "available memory": "23%"
  }
}”\

```

The response body returns the experience ID, indicating that the issue creation was successful.

```
{ 
  "result": { 
    "experience_id": “09ed4830f393739df33”
  } 
}
```

