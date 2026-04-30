---
title: Agent Mapping API
description: The Agent Mapping API provides an endpoint to map external agent IDs from Contact Center as a Service \(CCaaS\) systems to internal agent IDs in the ServiceNow AI Platform.Maps an external agent ID from a Contact Center as a Service \(CCaaS\) system to an internal agent ID in the ServiceNow AI Platform.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-02-10"
reading_time_minutes: 3
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Agent Mapping API

The Agent Mapping API provides an endpoint to map external agent IDs from Contact Center as a Service \(CCaaS\) systems to internal agent IDs in the ServiceNow AI Platform.

This API requires the External Agent Management Util Pack \(sn\_external\_agent\) plugin. To call this API, you must have the interaction\_agent role.

For more information about integrating with CCaaS systems, see [Integrating with contact centers](https://www.servicenow.com/docs/access?context=contactcenter-integration&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US).

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Agent Mapping - PUT /sn\_ct\_ctr\_it\_core/agent\_mapping/agent/\{agentId\}/inboundId/\{inboundId\}

Maps an external agent ID from a Contact Center as a Service \(CCaaS\) system to an internal agent ID in the ServiceNow AI Platform.

Call this endpoint when an agent logs in or out of the CCaaS system to update their active status. This endpoint creates or updates records in the External Agent Mapping \[external\_agent\_mapping\] table with the following data:

-   External CCaaS agent ID
-   Provider channel identity associated with the inbound ID
-   Agent's active status in the CCaaS system
-   Reference to the User \[sys\_user\] record for the agent

### URL format

Default URL: `/api/sn_ct_ctr_it_core/agent_mapping/agent/{agentId}/inboundId/{inboundId}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agentId

</td><td>

Sys\_id of the internal agent.Data type: String

Table: User \[sys\_user\]

</td></tr><tr><td>

inboundId

</td><td>

Inbound ID from the provider channel identity record for the CCaaS system.Data type: String

Table: Provider Channel Identity \[sys\_cs\_provider\_application\]

Field: Inbound ID

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the agent is currently logged in to the CCaaS system.Valid values:

-   true: The agent is logged in.
-   false: The agent is logged out.

Default: true

Data type: Boolean

</td></tr><tr><td>

external\_agent\_id

</td><td>

Required. External agent ID from the CCaaS system.Data type: String

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

<table><thead><tr><th>

Status code

</th><th>

Description

</th></tr></thead><tbody><tr><td>

200

</td><td>

OK. Existing agent mapping record updated.

</td></tr><tr><td>

201

</td><td>

Created.New agent mapping record created.

</td></tr><tr><td>

400

</td><td>

Bad request.The agent ID or inbound ID provided in the request is invalid.

</td></tr></tbody>
</table>### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

result

</td><td>

Result object containing information about the request.Data type: Object

</td></tr><tr><td>

result.mappingIds

</td><td>

Sys\_ids of any created or updated records in the External Agent Mapping \[external\_agent\_mapping\] table.Data type: Array of strings

</td></tr><tr><td>

result.message

</td><td>

Message explaining the outcome of the request.Data type: String

</td></tr><tr><td>

result.status

</td><td>

Status of the request.Possible values:

-   Success
-   Failure

Data type: String

</td></tr></tbody>
</table>### cURL request

This example maps an internal agent with sys\_id `da419c1fc312310015519f2974d3ae15` to the corresponding ID `12345` from the external CCaaS system.

```
curl "https://instance.service-now.com/api/sn_ct_ctr_it_core/agent_mapping/agent/da419c1fc312310015519f2974d3ae15/inboundId/ServiceNowVoice" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{\"external_agent_id\":\"12345\"}" \ 
--user 'username':'password'
```

Response body:

```
{
  "result": { 
    "message": "Agent Id mapping record inserted", 
    "status": "success", 
    "mappingIds": [ 
      "128b74fcc3931a50325a4ad9d00131c3" 
    ] 
  } 
}
```

### cURL request

This example sets the **active** parameter to `false` to indicate that the agent is logged out of the CCaaS system.

```
curl "https://instance.service-now.com/api/sn_ct_ctr_it_core/agent_mapping/agent/da419c1fc312310015519f2974d3ae15/inboundId/ServiceNowVoice" \ 
--request PUT \ 
--header "Accept:application/json" \ 
--header "Content-Type:application/json" \ 
--data "{"external_agent_id":"12345", "active":"false"}" \ 
--user 'username':'password'
```

Response body:

```
{ 
  "result": { 
    "message": "Agent Id mapping record updated", 
    "status": "success", 
    "mappingIds": [ 
      "cea77cebebef9e10a341fc7acad0cdc2" 
    ] 
  } 
}
```

