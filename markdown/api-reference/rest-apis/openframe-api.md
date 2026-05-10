---
title: openframe API
description: The openframe API provides endpoints that provide Contact Center as a Service \(CCaaS\) the ability to create and update interaction records without using the Operation Handler.Updates the specified interaction record in the Interaction \[interaction\] table. Contact Center as a Service \(CCaaS\) providers can then use these records to track phone calls.Creates an interaction record in the Interaction \[interaction\] table when an agent accepts a call. Contact Center as a Service \(CCaaS\) providers can then use these records to track phone calls.
locale: en-US
release: australia
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# openframe API

The openframe API provides endpoints that provide Contact Center as a Service \(CCaaS\) the ability to create and update interaction records without using the Operation Handler.

Use this API to create interaction records to track agent phone calls. Once an interaction record is created, the interaction can automatically display in the CSM Configurable Workspace when an agent receives a phone call.

To access this API, the com.sn\_openframe\_store plugin must be installed on the instance and the calling user must have either the sn\_openframe\_api\_user or sn\_openframe\_user role. The openframe API runs in the `sn_openframe` namespace.

For additional information on CSM voice interaction records, see [CSM voice interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-native-voice-record-page.md).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## openframe - PATCH /openframe/voice-interaction/\{interactionSysId\}

Updates the specified interaction record in the Interaction \[interaction\] table. Contact Center as a Service \(CCaaS\) providers can then use these records to track phone calls.

### URL format

Versioned URL: `/api/now/openframe/{api_version}/voice-interaction/{interactionSysId}`

Default URL: `/api/now/openframe/voice-interaction/{interactionSysId}`

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

interactionSysId

</td><td>

Sys\_id of the interaction record to update. This value is returned by the [Create Voice Interaction/POST](openframe-api.md#) endpoint.Data type: String

Table: Interaction \[interaction\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interaction

</td><td id="openframe-interaction-entry">

Required. Details of the voice interaction. At least one parameter must be passed.Data type: Object

```
"interaction": {
  "additionalParams": {Object},
  "callbackPhoneNumber": "String",
  "clientSessionId": "String",
  "inboundId": "String",
  "userPhoneNumber": "String"
}
```

</td></tr><tr><td>

interaction.additionalParams

</td><td id="openframe-interaction_additionalParams-entry">

Name-value pairs of the associated interaction record fields and their respective values.For example:

```
"additionalParams": {
  "direction": "inbound",
  "short_description": "New outbound call",
  "assigned_to": "a8f98bb0eb32010045e1a5115206fe3a"
}
```

Data type: Object

Default: None

</td></tr><tr><td>

interaction.callbackPhoneNumber

</td><td id="openframe-interaction_callbackPhoneNumber-entry">

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops.This value maps to the caller\_phone\_number field in the Interaction \[interaction\] table.

See also the **callerPhoneNumber** property description for [Create Voice Interaction/POST](openframe-api.md#).

Data type: String

Format: E.164

Default: None

</td></tr><tr><td>

interaction.clientSessionId

</td><td id="openframe-interaction_clientSessionId-entry">

Unique identifier of the record in an external system used to track this phone call. This information links the records between the two systems.Data type: String

Default: None

</td></tr><tr><td>

interaction.inboundId

</td><td id="openframe-interaction_inboundId-entry">

Unique identifier of the application provider for the voice service.Table: Inbound ID field in the Provider Channel Application \[sys\_cs\_provider\_application\] table.

Default: None

</td></tr><tr><td>

interaction.userPhoneNumber

</td><td>

Phone number of the user that made the call associated with the voice interaction.Data type: String

Format: E.164

</td></tr><tr><td>

interactionContext

</td><td id="openframe-interactionContext-entry">

Interaction context variables to set. Name-value pairs of the interaction context variables to save in the interaction record. These values are determined by CCaaS.For example:

```
"interactionContext":{
  "devicetype": "genesys",
  "requester_session_language": "en-US"
}
```

Data type: Object

Default: None

</td></tr><tr><td>

phoneLogs

</td><td id="openframe-phoneLogs-entry">

Name-value pairs of the phone logs to create and associate with a call. You can specify any field in the Phone Log \[sn\_open\_frame\_phone\_log\] table.For example:

```
"phoneLogs":[
  {
    "agent": "String",
    "call_id": "String",
    "start_time": "String"
  }
]
```

Data type: Array of Objects

Default: None

</td></tr><tr><td>

relatedRecords

</td><td id="openframe-relatedRecords-entry">

Records related to the call.Data type: Array of Objects

```
"relatedRecords":[
  {
    "documentId": "String",
    "documentTable": "String"
  }
]
```

Default: None

</td></tr><tr><td>

relatedRecords.documentId

</td><td id="openframe-relatedRecords_documentId-entry">

Sys\_id of the related record. Data type: String

Table: Specified in the **relatedRecords.documentTable** parameter.

</td></tr><tr><td>

relatedRecords.documentTable

</td><td id="openframe-relatedRecords_documentTable-entry">

Name of the table that contains the related record.Data type: String

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Status of the record update.Possible values:

-   SUCCESS: The interaction record was successfully updated.
-   FAILURE: The interaction record was not updated.

</td></tr></tbody>
</table>### cURL request

The following code example shows how to update the interaction record with the sys\_id 12961fff7fb2d2102d0cd3cf8c86652b.

```
curl "http://instance.service-now.com/api/now/openframe/voice-interaction/12961fff7fb2d2102d0cd3cf8c86652b" \
--request PATCH \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"interaction\":{
      \"additionalParams\":{
         \"direction\":\"inbound\",
         \"short_description\":\"New Poonam outbound call\",
         \"assigned_to\":\"a8f98bb0eb32010045e1a5115206fe3a\"
      }
   },
   \"interactionContext\":{
      \"devicetype\":\"genesys\",
      \"requester_session_language\":\"en-US\"
   },
   \"phoneLogs\":[
      {
         \"call_id\":\"2323223\",
         \"agent\":\"a8f98bb0eb32010045e1a5115206fe3a\",
         \"start_time\":\"2024-11-04 21:45:00\"
      },
      {
         \"call_id\":\"33535353\",
         \"agent\":\"a8f98bb0eb32010045e1a5115206fe3a\",
         \"start_time\":\"2024-11-04 21:45:00\"
      },
      {
         \"call_id\":\"1997654\",
         \"agent\":\"a8f98bb0eb32010045e1a5115206fe3a\",
         \"start_time\":\"2024-11-04 21:45:00\"
      }
   ],
   \"relatedRecords\":[
      {
         \"documentTable\":\"csm_consumer\",
         \"documentId\":\"59e788fbdb1b1200b6075200cf9619d2\"
      },
      {
         \"documentTable\":\"sys_user\",
         \"documentId\":\"62826bf03710200044e0bfc8bcbe5df1\"
      }
   ]
}" \
--user 'username':'pasword'

```

Response:

```
{
  "result": {
    "status": "SUCCESS"
  }
}

```

## openframe - POST /openframe/voice-interaction

Creates an interaction record in the Interaction \[interaction\] table when an agent accepts a call. Contact Center as a Service \(CCaaS\) providers can then use these records to track phone calls.

Use this endpoint to provide a consistent experience for agents, similar to other native channels such as chat and case, when accepting phone calls.

### URL format

Versioned URL: `/api/now/openframe/{api_version}/voice-interaction`

Default URL: `/api/now/openframe/voice-interaction`

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
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

interaction

</td><td>

Required. Details of the voice interaction. At least one parameter must be passed.Data type: Object

```
"interaction": {
  "additionalParams": {Object},
  "callbackPhoneNumber": "String",
  "clientSessionId": "String",
  "inboundId": "String",
  "userPhoneNumber": "String"
}
```

</td></tr><tr><td>

interaction.additionalParams

</td><td id="openframe-interaction_additionalParams-entry">

Name-value pairs of the associated interaction record fields and their respective values.For example:

```
"additionalParams": {
  "direction": "inbound",
  "short_description": "New outbound call",
  "assigned_to": "a8f98bb0eb32010045e1a5115206fe3a"
}
```

Data type: Object

Default: None

</td></tr><tr><td>

interaction.callbackPhoneNumber

</td><td id="openframe-interaction_callbackPhoneNumber-entry">

Caller's callback phone number. This is the number the agent uses to reach the caller in case the call drops.This value maps to the caller\_phone\_number field in the Interaction \[interaction\] table.

See also the **callerPhoneNumber** property description for [Create Voice Interaction/POST](openframe-api.md#).

Data type: String

Format: E.164

Default: None

</td></tr><tr><td>

interaction.clientSessionId

</td><td id="openframe-interaction_clientSessionId-entry">

Unique identifier of the record in an external system used to track this phone call. This information links the records between the two systems.Data type: String

Default: None

</td></tr><tr><td>

interaction.inboundId

</td><td id="openframe-interaction_inboundId-entry">

Unique identifier of the application provider for the voice service.Table: Inbound ID field in the Provider Channel Application \[sys\_cs\_provider\_application\] table.

Default: None

</td></tr><tr><td>

interaction.userPhoneNumber

</td><td id="openframe-interaction_userPhoneNumber-entry">

Required. Phone number of the user that made the call associated with the voice interaction.Data type: String

Format: E.164

</td></tr><tr><td>

interactionContext

</td><td id="openframe-interactionContext-entry">

Interaction context variables to set. Name-value pairs of the interaction context variables to save in the interaction record. These values are determined by CCaaS.For example:

```
"interactionContext":{
  "devicetype": "genesys",
  "requester_session_language": "en-US"
}
```

Data type: Object

Default: None

</td></tr><tr><td>

phoneLogs

</td><td id="openframe-phoneLogs-entry">

Name-value pairs of the phone logs to create and associate with a call. You can specify any field in the Phone Log \[sn\_open\_frame\_phone\_log\] table.For example:

```
"phoneLogs":[
  {
    "agent": "String",
    "call_id": "String",
    "start_time": "String"
  }
]
```

Data type: Array of Objects

Default: None

</td></tr><tr><td>

relatedRecords

</td><td id="openframe-relatedRecords-entry">

Records related to the call.Data type: Array of Objects

```
"relatedRecords":[
  {
    "documentId": "String",
    "documentTable": "String"
  }
]
```

Default: None

</td></tr><tr><td>

relatedRecords.documentId

</td><td id="openframe-relatedRecords_documentId-entry">

Sys\_id of the related record. Data type: String

Table: Specified in the **relatedRecords.documentTable** parameter.

</td></tr><tr><td>

relatedRecords.documentTable

</td><td id="openframe-relatedRecords_documentTable-entry">

Name of the table that contains the related record.Data type: String

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
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON or XML\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

number

</td><td>

Only returned on success. Interaction number of the newly created voice interaction. Data type: String

</td></tr><tr><td>

status

</td><td>

Status of the record creation.Possible values:

-   SUCCESS: The interaction record was successfully created.
-   FAILURE: The interaction record was not created.

</td></tr><tr><td>

sysId

</td><td>

Only returned on success. Sys\_id of the newly created voice interaction record. Table: Interaction \[interaction\]

</td></tr></tbody>
</table>### cURL request

The following code example shows how to create a new interaction record.

```
curl "http://instance.service-now.com/api/now/openframe/voice-interaction" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"interaction\":{
      \"userPhoneNumber\":\"+1303506536\",
      \"clientSessionId\":\"a545t65678\",
      \"callbackPhoneNumber\":\"+14089965744\",
      \"additionalParams\":{
         \"direction\":\"inbound\",
         \"short_description\":\"New outbound call\",
         \"assigned_to\":\"a8f98bb0eb32010045e1a5115206fe3a\"
      }
   },
   \"interactionContext\":{
      \"devicetype\":\"genesys\",
      \"requester_session_language\":\"en-US\"
   },
   \"phoneLogs\":[
      {
         \"call_id\":\"2323223\",
         \"agent\":\"a8f98bb0eb32010045e1a5115206fe3a\",
         \"start_time\":\"2024-11-04 21:45:00\"
      },
      {
         \"call_id\":\"33535353\",
         \"agent\":\"a8f98bb0eb32010045e1a5115206fe3a\",
         \"start_time\":\"2024-11-04 21:45:00\"
      },
      {
         \"call_id\":\"1997654\",
         \"agent\":\"a8f98bb0eb32010045e1a5115206fe3a\",
         \"start_time\":\"2024-11-04 21:45:00\"
      }
   ],
   \"relatedRecords\":[
      {
         \"documentTable\":\"csm_consumer\",
         \"documentId\":\"59e788fbdb1b1200b6075200cf9619d2\"
      },
      {
         \"documentTable\":\"sys_user\",
         \"documentId\":\"62826bf03710200044e0bfc8bcbe5df1\"
      }
   ]
}" \
--user 'username':'password'

```

Response:

```
{
  "result": {
    "status": "SUCCESS",
    "sysId": "12961fff7fb2d2102d0cd3cf8c86652b",
    "number": "IMS0000052"
  }
}
```

