---
title: Agent Client Collector API
description: The Agent Client Collector API provides endpoints to manage actions on available agents and managing policies.Gets the information of a specified agent.Disables data collection for a specified agent in the up/alive state.Enables data collection for a specified agent in the up/alive state.Runs a discovery check to locate CIs related to an agent. The specified agent must be in alive/up status.Gets a specified check definition with details.Gets a list of check definitions with details.Stops a background check.Gets status of the request with the given ID.Gets the test check status of the given test result.Gets a list of agents with related information.Requests the log of a specified agent with alive/up status.Checks the status of a grab log request.Gets a list of policies that are in published or unpublished draft state.Activates a published policy.Deactivates a published policy.Publishes a draft policy.Gets the sandbox copy of a published policy and provides policy details.Restarts a specified agent with alive/up status.Runs a check against the given configuration item.Enables building test check requests on check definitions.Enables building test check requests on check instances.Updates a selected policy check.Enables changing one or more field values of a specified check parameter.Enables changing one or more field values of a specified check secure parameter.Enables changing one or more field values of a specified check definition.Updates a selected policy check parameter.Updates a selected policy check secure parameter.Updates a sandbox copy of a policy.
locale: en-US
release: yokohama
product: REST APIs
classification: rest-apis
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 77
breadcrumb: [REST API reference, API reference, API implementation and reference]
---

# Agent Client Collector API

The Agent Client Collector API provides endpoints to manage actions on available agents and managing policies.

This API requires the Agent Client Collector Framework \(sn\_agent\) store application and is provided within the `sn_agent` namespace. The endpoints in this API require the agent\_client\_collector\_admin role. For more information, refer to [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).

-   **Agent management endpoints**

    -   Get extensive information of one or more agents. These endpoints are also accessible to users with the agent\_client\_collector\_user role.
        -   [GET /agents/\{agent\_id\}](agnt_clnt_cll-api.md#)
        -   [GET /agents/list](agnt_clnt_cll-api.md#)
    -   Submit a request to grab an agent log and retrieving information about the request progress.
        -   [GET /agents/\{agent\_id\}/log](agnt_clnt_cll-api.md#)
        -   [GET /agents/log/\{request\_id\}/](agnt_clnt_cll-api.md#)
    -   Disable or enable agent data collection.
        -   [GET /agents/\{agent\_id\}/data/off](agnt_clnt_cll-api.md#)
        -   [GET /agents/\{agent\_id\}/data/on](agnt_clnt_cll-api.md#)
    -   Restart an agent with [GET /agents/\{agent\_id\}/restart](agnt_clnt_cll-api.md#).
    -   Run discovery on an agent with [GET /agents/\{agent\_id\}/discovery](agnt_clnt_cll-api.md#).
    For information on performing similar tasks in a script include, see [AccAgentsAPI](https://developer.servicenow.com/go_to_api.do?ID=AccAgentsAPIAPIScoped&v=utah).

-   **Policy management and workflow**

    Use policy management APIs to view details, activate/deactivate a policy, update a policy, and publish a policy.

    To update a policy:

    1.  Get a list of policies and details with [GET /agents/policies/list](agnt_clnt_cll-api.md#). This endpoint requires the agent\_client\_collector\_user role.
        -   To update a policy in the Draft state, use the sys\_ids retrieved from the policies list in the update endpoints.
        -   To update a policy in Published or Published\* state, get an editable sandbox copy with [GET /agents/policy/sandbox\_from\_published/\{policy\_id\}](agnt_clnt_cll-api.md#). Use the sys\_ids from this response to modify properties using an update endpoint.
    2.  Modify policy details using an update endpoint.
        -   [POST /agents/update/policy/\{policy\_id\}](agnt_clnt_cll-api.md#)
        -   [POST /agents/update/check/\{check\_id\}](agnt_clnt_cll-api.md#)
        -   [POST /agents/update/check\_param/\{param\_id\}](agnt_clnt_cll-api.md#)
        -   [POST /agents/update/check\_secure\_param/\{param\_id\}](agnt_clnt_cll-api.md#)
    3.  Publish the policy using [GET /agents/policy/publish/\{policy\_id\}](agnt_clnt_cll-api.md#).
    Once published, the policy becomes Active. This API also includes endpoints for activating or deactivating a published policy:

    -   [GET /agents/policy/activate/\{policy\_id\}](agnt_clnt_cll-api.md#)
    -   [GET /agents/policy/deactivate/\{policy\_id\}](agnt_clnt_cll-api.md#)

**Parent Topic:**[REST API reference](../../../build/applications/concept/api-rest.md)

## Agent Client Collector - GET /agents/\{agent\_id\}

Gets the information of a specified agent.

### URL format

`/api/sn_agent/agents/{agent_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent\_id

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table. For a list of agent IDs and other details, run the GET /agents/list endpoint.

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
|403|The user does not have the agent\_client\_collector\_user role.|
|404|Agent with provided ID not found.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Array&gt;

</td><td>

Array of JSON objects containing extended agent information.```
{
   "agent_id": "String",
   "data_collection": Number,
   "ip_address": "String",
   "is_duplicate": Boolean,
   "is_restart_enabled": Boolean,
   "name": "String",
   "number_of_running_checks": Number,
   "status": Number,
   "up_since": "String",
   "version": "String"
}
```

</td></tr><tr><td>

agent\_id

</td><td id="accAgents-parm-agent-obj-id-entry">

ID of the agent as submitted.Data type: String

</td></tr><tr><td>

data\_collection

</td><td id="accAgents-parm-agent-obj-dataCollect-entry">

Data collection indicates whether scheduled checks are to be run. These checks are a part of the policies scheduled for this agent to run.Possible values:

-   0: On – Checks run as scheduled.
-   1: Off \(manual\) – Checks have been disabled manually.
-   2: Off \(auto\) – Checks have been disabled automatically due to high CPU consumption by the

 Data type: Number

</td></tr><tr><td>

ip\_address

</td><td id="accAgents-parm-agent-obj-ip-entry">

Agent IP address.Data type: String

</td></tr><tr><td>

is\_duplicate

</td><td id="accAgents-parm-agent-obj-dup-entry">

Flag that indicates whether this agent is a duplicate of another. There should be only a single agent on a given host.

 Possible values:

-   true: The agent has the same host as an Alive/Up agent with a different agent ID. Turn off or uninstall the duplicate
-   false: This agent has no duplicates in the Alive/Up state.

 Data type: Boolean

</td></tr><tr><td>

is\_restart\_enabled

</td><td id="accAgents-parm-agent-obj-restart-entry">

Flag that indicates whether restart is enabled. Agent restart is not configurable. It depends on the OS and the version of the OS the agent is running on.

 Possible values:

-   true: Restart is enabled for this agent.
-   false: Restart is disabled for this agent.

 Data type: Boolean

</td></tr><tr><td>

name

</td><td id="accAgents-parm-agent-obj-name-entry">

Name of the agent.Data type: String

</td></tr><tr><td>

number\_of\_running\_checks

</td><td id="accAgents-parm-agent-obj-numChecks-entry">

The number of checks the agent is scheduled to run. These checks are a part of the policies scheduled for this agent to run.Data type: Number

</td></tr><tr><td>

status

</td><td id="accAgents-parm-agent-obj-status-entry">

Status of the agent.Possible values:

-   0: Alive/Up – The agent is active.
-   1: Warning – The agent has not received a keep-alive message in the past few minutes.
-   2: Down – The agent has not received a keep-alive message in a long time.
-   3: Restarting – The agent is restarting.

 Data type: Number

</td></tr><tr><td>

up\_since

</td><td id="accAgents-parm-agent-obj-up-entry">

UTC time since the agent's status became alive/up. The value is in [GlideDateTime](../../../app-store/dev_portal/API_reference/glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) format.Data type: String

</td></tr><tr><td>

version

</td><td id="accAgents-parm-agent-obj-version-entry">

Version of Agent Client Collector the agent is running.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to get agent details.

```
curl "https://instance.service-now.com/api/sn_agent/agents/<agent_id>" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
  "name": "WIN-V26KAP7PI2G",
  "status": 2,
  "agent_id": "074b14e2eb3ce9d4",
  "ip_address": "10.196.55.14",
  "number_of_running_checks": 11,
  "data_collection": 0,
  "is_restart_enabled": true,
  "is_duplicate": false,
  "up_since": "2021-03-31 12:02:17",
  "version": "2.3.0"
}
```

## Agent Client Collector - GET /agents/\{agent\_id\}/data/off

Disables data collection for a specified agent in the up/alive state.

To determine if an agent's data collection is on or off, run the GET /agents/\{agent\_id\} endpoint.

### URL format

`/api/sn_agent/agents/{agent_id}/data/off`

### Supported request parameters

<table id="table_oyt_cd3_dpb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent\_id

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table. For a list of agent IDs and other details, run the GET /agents/list endpoint.

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|Agent not found or isn't in the up/alive state.|

### Response body parameters \(JSON\)

<table id="table_owl_zyc_z4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to turn off agent data collection.

```
curl "https://instance.service-now.com/api/sn_agent/agents/<agent_id>/data/off" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
"message": "Data Collection Disabled For Agent With ID: <agent_id>"
}
```

## Agent Client Collector - GET /agents/\{agent\_id\}/data/on

Enables data collection for a specified agent in the up/alive state.

To determine if an agent's data collection is on or off, run the GET /agents/\{agent\_id\} endpoint.

### URL format

`/api/sn_agent/agents/{agent_id}/data/on`

### Supported request parameters

<table id="table_oyt_cd3_dpb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent\_id

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table. For a list of agent IDs and other details, run the GET /agents/list endpoint.

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|Agent not found or isn't in the up/alive state.|

### Response body parameters \(JSON\)

<table id="table_owl_zyc_z4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to turn on agent data collection.

```
curl "https://instance.service-now.com/api/sn_agent/agents/<agent_id>/data/on" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

Output:

```
{
  "message": "Data Collection Enabled For Agent With ID: <agent_id>"
}
```

## Agent Client Collector - GET /agents/\{agent\_id\}/discovery

Runs a discovery check to locate CIs related to an agent. The specified agent must be in alive/up status.

### URL format

`/api/sn_agent/agents/{agent_id}/discovery`

### Supported request parameters

<table id="table_oyt_cd3_dpb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent\_id

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table. For a list of agent IDs and other details, run the GET /agents/list endpoint.

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|Agent not found or isn't in the up/alive state.|

### Response body parameters \(JSON\)

<table id="table_owl_zyc_z4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to run discovery on an agent with alive/up status.

```
curl "https://instance.service-now.com/api/sn_agent/agents/<agent_id>/discovery" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
  "message": "Running Discovery For Agent With ID: <agent_id>"
}
```

## Agent Client Collector - GET /agents/check\_defs/\{check\_def\_id\}

Gets a specified check definition with details.

### URL format

`/api/sn_agent/agents/check_defs/{check_def_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check\_def\_id

</td><td>

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table. Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

X-Include-Check-Params

</td><td>

Flag that indicates whether existing check parameter details are returned. Information for each standard and secure check parameter is included in a JSON object. Valid values:

-   true: Return check parameter details.
-   false: Do not return check parameter details.

 Data type: Boolean

 Default: False

</td></tr></tbody>
</table>### Headers

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
|404|Check definition was not found with the sys\_id provided.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check

</td><td>

Details of the specified check definition.```
{
 "background": Boolean,
 "check_group": "String",
 "check_type": "String",
 "command": "String",
 "error": "String",
 "name": "String",
 "params": [Array],
 "plugins": [Array],
 "proxy_valid": Boolean,
 "secure_params": [Array],
 "sys_id": "String",
 "timeout": Number
}
```

</td></tr><tr><td>

background

</td><td>

Flag that indicates whether this check definition is a background check. A background check is a check which the agent starts execution of and doesn't wait for it to finish running. Valid values:

-   true: This check definition is a background check.
-   false: This check definition is not a background check.

 Data type: Boolean

</td></tr><tr><td>

check\_group

</td><td>

Group specified for this check definition. Data type: String

</td></tr><tr><td>

check\_type

</td><td>

Type of check. Possible values:

-   Events – Check results are transformed into an Event Management event.
-   Metrics – Values from the check result are transformed to metrics.

 Data type: String

</td></tr><tr><td>

command

</td><td>

Command that the Agent Client Collector executes. Data type: String

</td></tr><tr><td>

error

</td><td>

Message if there is an error. Null otherwise.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the check. Data type: String

</td></tr><tr><td>

params

</td><td>

List of parameter definitions associated with the check definition. These results are only included if the **withParams** parameter is set to true.```
"params": [
  {
    "active": Boolean,
    "default_value": "String",
    "mandatory": Boolean,
    "name": "String",
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

params.active

</td><td>

Flag that indicates whether the check parameter is active. Valid values:

-   true: The check parameter is active.
-   false: The check parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

params.default\_value

</td><td>

Specifies the default value for this check parameter. Data type: String

</td></tr><tr><td>

params.mandatory

</td><td>

Flag that indicates whether the check parameter is required. Valid values:

-   true: The check parameter is required.
-   false: The check parameter is optional.

 Data type: Boolean

</td></tr><tr><td>

params.name

</td><td>

Name of the check parameter. Data type: String

</td></tr><tr><td>

params.sys\_id

</td><td>

Sys\_id of the check parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_param\_def\] table. Data type: String

</td></tr><tr><td>

plugins

</td><td>

List of [Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=acc-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) associated with this check. Data type: Array

</td></tr><tr><td>

proxy\_valid

</td><td>

Flag that indicates whether the check definition policy is set to work as a proxy. Valid values:

-   true: This check definition policy is set to work as a proxy.
-   false: This check definition policy is not set to work as a proxy.

 Data type: Boolean

</td></tr><tr><td>

secure\_params

</td><td>

List of assigned to this check. These results are only included if the **withParams** parameter is set to true.```
"secure_params": [
  {
    "active": Boolean,
    "name": "String",
    "order": Number,
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

secure\_params.active

</td><td>

Flag that indicates whether the secure parameter is active. Valid values:

-   true: The secure parameter is active.
-   false: The secure parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

secure\_params.name

</td><td>

Name of the secure parameter. Data type: String

</td></tr><tr><td>

secure\_params.order

</td><td>

Order in which the parameter is sent to the check command/script. Data type: Number

</td></tr><tr><td>

secure\_params.sys\_id

</td><td>

Sys\_id of the secure parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_secure\_param\_def\] table. Data type: String

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table. Data type: String

</td></tr><tr><td>

timeout

</td><td>

Timeout in seconds. Data type: Number

</td></tr></tbody>
</table>### cURL request

The following example shows how to get information for a specified check definition.

```
curl "https://instance.service-now.com/api/sn_agent/agents/check_defs/94436b237f705300f128134f8dfa91a4" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
  "name": "app.apache.metrics-apache",
  "command": "metrics-apache-graphite.rb -p {{.labels.params_port}} --path {{.labels.params_path}} -h {{.labels.params_host}}",
  "plugins": [
    "monitoring-plugin-common"
  ],
  "timeout": 60,
  "proxy_valid": true,
  "background": false,
  "check_type": "Metrics",
  "check_group": "Apache",
  "sys_id": "94436b237f705300f128134f8dfa91a4",
  "params": [
    {
      "name": "port",
      "active": true,
      "mandatory": true,
      "default_value": "80",
      "sys_id": "58436b237f705300f128134f8dfa91a8"
    },
    {
      "name": "path",
      "active": true,
      "mandatory": true,
      "default_value": "/server-status?auto",
      "sys_id": "98436b237f705300f128134f8dfa91aa"
    },
    {
      "name": "scheme",
      "active": false,
      "mandatory": false,
      "default_value": null,
      "sys_id": "a4e57a96db3bbb4035305c55dc9619f6"
    },
    {
      "name": "host",
      "active": true,
      "mandatory": true,
      "default_value": "127.0.0.1",
      "sys_id": "d4436b237f705300f128134f8dfa91a6"
    },
    {
      "name": "ssl_secure_connection",
      "active": false,
      "mandatory": false,
      "default_value": null,
      "sys_id": "e3b272c4530100106ffeddeeff7b1275"
    }
  ],
  "secure_params": [
    {
      "name": "cred_user_name",
      "active": true,
      "order": 1,
      "sys_id": "2494cd6e53170010f42cddeeff7b1273"
    },
    {
      "name": "cred_password",
      "active": true,
      "order": 2,
      "sys_id": "35948d6e53170010f42cddeeff7b127f"
    }
  ]
}
```

## Agent Client Collector - GET /agents/check\_defs/list

Gets a list of check definitions with details.

### URL format

`/api/sn_agent/agents/check_defs/list`

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

X-Enc-Query

</td><td>

An [encoded query string](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) to filter the check definition result list. Use null for an unfiltered list of check definitions in the system. Data type: String

</td></tr><tr><td>

X-Include-Check-Params

</td><td>

Flag that indicates whether existing check parameter details are returned. Information for each standard and secure check parameter is included in a JSON object. Valid values:

-   true: Return check parameter details.
-   false: Do not return check parameter details.

 Data type: Boolean

 Default: False

</td></tr><tr><td>

X-Limit

</td><td>

Limits the number of returned records. Set to null to use the default value. Data type: Number

 Default: 20,000

</td></tr></tbody>
</table>### Headers

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

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check definitions

</td><td>

List of check definition and details provided as JSON objects.```
[
 {
  "background": Boolean,
  "check_group": "String",
  "check_type": "String",
  "command": "String",
  "name": "String",
  "params": [Array],
  "plugins": [Array],
  "proxy_valid": Boolean,
  "secure_params": [Array],
  "sys_id": "String",
  "timeout": Number 
 }
]
```

 Data type: Array

</td></tr><tr><td>

background

</td><td id="accCkDf-background-desc">

Flag that indicates whether this check definition is a background check. A background check is a check which the agent starts execution of and doesn't wait for it to finish running. Valid values:

-   true: This check definition is a background check.
-   false: This check definition is not a background check.

 Data type: Boolean

</td></tr><tr><td>

check\_group

</td><td id="accCkDf-chkGrp-desc">

Group specified for this check definition. Data type: String

</td></tr><tr><td>

check\_type

</td><td id="accCkDf-chkTyp-desc">

Type of check. Possible values:

-   Events – Check results are transformed into an Event Management event.
-   Metrics – Values from the check result are transformed to metrics.

 Data type: String

</td></tr><tr><td>

command

</td><td id="accCkDf-command-desc">

Command that the Agent Client Collector executes. Data type: String

</td></tr><tr><td>

name

</td><td id="accCkDf-name-desc">

Name of the check. Data type: String

</td></tr><tr><td>

params

</td><td id="accCkDf-p-desc">

List of parameter definitions associated with the check definition. These results are only included if the **withParams** parameter is set to true.```
"params": [
  {
    "active": Boolean,
    "default_value": "String",
    "mandatory": Boolean,
    "name": "String",
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

params.active

</td><td id="accCkDf-p-active-desc">

Flag that indicates whether the check parameter is active. Valid values:

-   true: The check parameter is active.
-   false: The check parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

params.default\_value

</td><td id="accCkDf-p-default-desc">

Specifies the default value for this check parameter. Data type: String

</td></tr><tr><td>

params.mandatory

</td><td id="accCkDf-p-mando-desc">

Flag that indicates whether the check parameter is required. Valid values:

-   true: The check parameter is required.
-   false: The check parameter is optional.

 Data type: Boolean

</td></tr><tr><td>

params.name

</td><td id="accCkDf-p-name-desc">

Name of the check parameter. Data type: String

</td></tr><tr><td>

params.sys\_id

</td><td id="accCkDf-p-id-desc">

Sys\_id of the check parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_param\_def\] table. Data type: String

</td></tr><tr><td>

plugins

</td><td id="accCkDf-plugins-desc">

List of [Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=acc-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) associated with this check. Data type: Array

</td></tr><tr><td>

proxy\_valid

</td><td id="accCkDf-proxy-desc">

Flag that indicates whether the check definition policy is set to work as a proxy. Valid values:

-   true: This check definition policy is set to work as a proxy.
-   false: This check definition policy is not set to work as a proxy.

 Data type: Boolean

</td></tr><tr><td>

secure\_params

</td><td id="accCkDf-sp-desc">

List of assigned to this check. These results are only included if the **withParams** parameter is set to true.```
"secure_params": [
  {
    "active": Boolean,
    "name": "String",
    "order": Number,
    "sys_id": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

secure\_params.active

</td><td id="accCkDf-sp-active-desc">

Flag that indicates whether the secure parameter is active. Valid values:

-   true: The secure parameter is active.
-   false: The secure parameter is inactive.

 Data type: Boolean

</td></tr><tr><td>

secure\_params.name

</td><td id="accCkDf-sp-name-desc">

Name of the secure parameter. Data type: String

</td></tr><tr><td>

secure\_params.order

</td><td id="accCkDf-sp-order-desc">

Order in which the parameter is sent to the check command/script. Data type: Number

</td></tr><tr><td>

secure\_params.sys\_id

</td><td id="accCkDf-sp-id-desc">

Sys\_id of the secure parameter listed in the Check Secure Parameter Definitions \[sn\_agent\_check\_secure\_param\_def\] table. Data type: String

</td></tr><tr><td>

sys\_id

</td><td id="accCkDf-id-desc">

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table. Data type: String

</td></tr><tr><td>

timeout

</td><td id="accCkDf-timeout-desc">

Timeout in seconds. Data type: Number

</td></tr></tbody>
</table>### cURL request

The following example shows how to retrieve a list of two check definitions with parameter values.

```
curl "https://instance.service-now.com/api/sn_agent/agents/check_defs/list" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
  "check_definitions": [
    {
      "name": "checks_api_test",
      "command": "echo hello",
      "plugins": [],
      "timeout": 9,
      "proxy_valid": true,
      "background": false,
      "check_type": "TestCheck",
      "check_group": "computer",
      "sys_id": "7f1f9026dba530106f4810284b96194f",
      "params": [],
      "secure_params": [
        {
          "name": "check_api_test_check_secure_param2",
          "active": true,
          "order": 2,
          "sys_id": "2d30a066dba530106f4810284b9619c1"
        },
        {
          "name": "check_api_test_check_secure_param1",
          "active": true,
          "order": 100,
          "sys_id": "4c20a066dba530106f4810284b9619a8"
        }
      ]
    },
    {
      "name": "checks_api_test222",
      "command": "echo hello1212121",
      "plugins": [],
      "timeout": 60,
      "proxy_valid": true,
      "background": false,
      "check_type": "TestCheck",
      "check_group": "computer",
      "sys_id": "99e12466dba530106f4810284b961976",
      "params": [
        {
          "name": "check_api_test_check_param_222",
          "active": true,
          "mandatory": false,
          "default_value": "test_test_test",
          "sys_id": "44026466dba530106f4810284b9619b2"
        }
      ],
      "secure_params": []
    }
  ]
}
```

## Agent Client Collector - GET /agents/exec/background/stop/\{request\_id\}

Stops a background check.

To start a background check, use the POST /agents/check\_defs/\{check\_def\_id\}/run API.

### URL format

`/api/sn_agent/agents/exec/background/stop/{request_id}`

### Supported request parameters

|Name|Description|
|----|-----------|
|request\_id|The ID of a background check request generated by running the POST /agents/check\_defs/\{check\_def\_id\}/run API.|

|Name|Description|
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
|404|The request with the ID provided is not found.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|None| |

### cURL request

The following example shows how to stop a background check.

```
curl "https://instance.service-now.com/api/sn_agent/agents/exec/background/stop/02359174db2a30108a0751f4f3961997" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

## Agent Client Collector - GET /agents/exec/run/\{request\_id\}

Gets status of the request with the given ID.

### URL format

`/api/sn_agent/agents/exec/run/{request_id}`

### Supported request parameters

|Name|Description|
|----|-----------|
|request\_id|The ID of a background check request generated by running the POST /agents/check\_defs/\{check\_def\_id\}/run API.|

|Name|Description|
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
|202|Message with provided ID indicating that the request is in progress.|
|400|Error in the arguments provided in the request body.|
|404|The request with the ID provided is not found.|
|408|Execution timeout for the request with the ID provided.|
|500|Error checking the status or the request with the ID provided.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Request status.Possible values:

-   done – Check is successful.
-   failure – Check has failed. See error message for details.
-   mid\_flow – Request output is being handled by the MID server.
-   processing – Check is in progress.
-   timeout – Check processing exceeded time limit set in the runCheckForCis\(\) method.

 Data type: String

</td></tr><tr><td>

err\_msg

</td><td>

Error message if any.Possible values:

-   No agents found for relevant CIs.
-   No background check request with given ID.
-   No request with given ID.
-   No test result with given ID.
-   Request timeout.

 Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to get the status of a request.

```
curl "https://instance.service-now.com/api/sn_agent/agents/exec/run/12fed13cdb2a30108a0751f4f3961981" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

## Agent Client Collector - GET /agents/exec/test/\{test\_result\_id\}

Gets the test check status of the given test result.

### URL format

`/api/sn_agent/agents/exec/test/{test_result_id}`

### Supported request parameters

|Name|Description|
|----|-----------|
|test\_result\_id|A test result ID generated by creating a test check request.|

|Name|Description|
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
|202|Message with provided ID indicating that the request is in progress.|
|404|The request with the ID provided is not found.|
|408|Execution timeout for the request with the ID provided.|
|500|Error checking the status of the request with the ID provided.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

status

</td><td>

Status of the test results.Possible values:

-   0: Pending
-   1: In progress
-   2: Complete
-   3: No test result with given ID

 Data type: String

</td></tr><tr><td>

output

</td><td>

Output describing the status.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how get result status of a completed test check request.

```
curl "https://instance.service-now.com/api/sn_agent/agents/check_instances/99e12466dba530106f4810284b961976/test" \
--request POST \
--header "Accept:application/json" \
--user 'username':'password'
```

## Agent Client Collector - GET /agents/list

Gets a list of agents with related information.

### URL format

`/api/sn_agent/agents/list`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

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

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

X-Enc-Query

</td><td>

Encoded query on the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

X-Limit

</td><td>

Restricts results to a maximum number of agents. Use null or undefined for both if they are not required.Default/Max: 20,000Data type: Number

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|403|The user does not have the agent\_client\_collector\_user role.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Array&gt;

</td><td>

Array of JSON objects containing extended agent information.```
[
 {
   "agent_id": "String",
   "data_collection": Number,
   "ip_address": "String",
   "is_duplicate": Boolean,
   "is_restart_enabled": Boolean,
   "name": "String",
   "number_of_running_checks": Number,
   "status": Number,
   "up_since": "String",
   "version": "String"
 }
]
```

</td></tr><tr><td>

agent\_id

</td><td id="accAgents-parm-agent-obj-id-entry">

ID of the agent as submitted.Data type: String

</td></tr><tr><td>

data\_collection

</td><td id="accAgents-parm-agent-obj-dataCollect-entry">

Data collection indicates whether scheduled checks are to be run. These checks are a part of the policies scheduled for this agent to run.Possible values:

-   0: On – Checks run as scheduled.
-   1: Off \(manual\) – Checks have been disabled manually.
-   2: Off \(auto\) – Checks have been disabled automatically due to high CPU consumption by the

 Data type: Number

</td></tr><tr><td>

ip\_address

</td><td id="accAgents-parm-agent-obj-ip-entry">

Agent IP address.Data type: String

</td></tr><tr><td>

is\_duplicate

</td><td id="accAgents-parm-agent-obj-dup-entry">

Flag that indicates whether this agent is a duplicate of another. There should be only a single agent on a given host.

 Possible values:

-   true: The agent has the same host as an Alive/Up agent with a different agent ID. Turn off or uninstall the duplicate
-   false: This agent has no duplicates in the Alive/Up state.

 Data type: Boolean

</td></tr><tr><td>

is\_restart\_enabled

</td><td id="accAgents-parm-agent-obj-restart-entry">

Flag that indicates whether restart is enabled. Agent restart is not configurable. It depends on the OS and the version of the OS the agent is running on.

 Possible values:

-   true: Restart is enabled for this agent.
-   false: Restart is disabled for this agent.

 Data type: Boolean

</td></tr><tr><td>

name

</td><td id="accAgents-parm-agent-obj-name-entry">

Name of the agent.Data type: String

</td></tr><tr><td>

number\_of\_running\_checks

</td><td id="accAgents-parm-agent-obj-numChecks-entry">

The number of checks the agent is scheduled to run. These checks are a part of the policies scheduled for this agent to run.Data type: Number

</td></tr><tr><td>

status

</td><td id="accAgents-parm-agent-obj-status-entry">

Status of the agent.Possible values:

-   0: Alive/Up – The agent is active.
-   1: Warning – The agent has not received a keep-alive message in the past few minutes.
-   2: Down – The agent has not received a keep-alive message in a long time.
-   3: Restarting – The agent is restarting.

 Data type: Number

</td></tr><tr><td>

up\_since

</td><td id="accAgents-parm-agent-obj-up-entry">

UTC time since the agent's status became alive/up. The value is in [GlideDateTime](../../../app-store/dev_portal/API_reference/glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) format.Data type: String

</td></tr><tr><td>

version

</td><td id="accAgents-parm-agent-obj-version-entry">

Version of Agent Client Collector the agent is running.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to restrict results by query and number. The query returns all agents that are not in the down state with a maximum of two results.

```
curl "https://instance.service-now.com/api/sn_agent/agents/list" \
--request GET \
--header "Accept:application/json" \
--header "X-Enc-Query: agent_extended_info.status!=2" \
--header "X-Limit: 2" \
--user 'username':'password'
```

Output:

```
{
   "agents": [
     {
       "name": "007-175",
       "status": 0,
        "agent_id": "007-175",
       "ip_address": "11.222.63.66",
        "number_of_running_checks": 0,
       "data_collection": 0,
       "is_restart_enabled": false,
       "is_duplicate": false,
       "up_since": "2021-03-24 14:36:45",
       "version": "2.4.0"
     },
     {
       "name": "win2016-dc-64bit",
       "status": 0,
       "agent_id": "007-64",
       "ip_address": "10.222.333.42",
       "number_of_running_checks": 1,
       "data_collection": 0,
       "is_restart_enabled": true,
       "is_duplicate": false,
       "up_since": "2021-03-24 11:04:38",
       "version": "2.4.0"
     }
   ]
}
```

### cURL request

The following example shows how to list every agent in the system. This example uses no query and no maximum number of results.

```
curl "https://instance.service-now.com/api/sn_agent/agents/list" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

## Agent Client Collector - GET /agents/\{agent\_id\}/log

Requests the log of a specified agent with alive/up status.

**Note:** To retrieve the log and check its progress, pass the request ID returned to the GET /agents/log/\{request\_id\}/ endpoint.

### URL format

`/api/sn_agent/agents/{agent_id}/log`

### Supported request parameters

<table id="table_oyt_cd3_dpb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent\_id

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table. For a list of agent IDs and other details, run the GET /agents/list endpoint.

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|Agent not found or isn't in the up/alive state.|

### Response body parameters \(JSON\)

<table id="table_vpf_zyc_z4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request\_id

</td><td>

Sys\_id of a request in the Agent Client Collector Requests \[sn\_agent\_request\] table. You can use this ID to retrieve the log and check its progress with the GET /agents/log/\{request\_id\}/ endpoint.

 Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to get a log request ID.

```
curl "https://instance.service-now.com/api/sn_agent/agents/<sys_id>/log" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
"request_id": "<sys_id>"
```

## Agent Client Collector - GET /agents/log/\{request\_id\}/

Checks the status of a grab log request.

Detects changes in the log retrieving request sent with GET /api/sn\_agent/agents/\{agent\_id\}/log.

### URL format

`/api/sn_agent/agents/log/{request_id}/`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

request\_id

</td><td>

Sys\_id of a request in the Agent Client Collector Requests \[sn\_agent\_request\] table. For the request id, run GET /api/sn\_agent/agents/\{agent\_id\}/log.

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
|200|Request status is done and the grabbed log is ready.|
|202|Grab log request with provided ID is still in progress.|
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|Grab log request with provided ID not found.|
|408|Grab log request timed out.|
|500|Grab log request encountered an error.|

### Response body parameters \(JSON\)

|Properties|Description|
|----------|-----------|
|output|Information describing the status.|

### cURL request

The following example shows how to use a request ID to get the status of a grab log request.

```
curl "https://instance.service-now.com/api/sn_agent/agents/log/<request_ID>" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
  "output": "SensuSnReadFile OK: {\"component\":\"agent\",\"level\":\"info\",\"msg\":\"Agent Protection: cpu of all checks: 0%\",\"time\":\"2021-04-05T00:21:41-07:00\"},...
}
```

## Agent Client Collector - GET /agents/policies/list

Gets a list of policies that are in published or unpublished draft state.

### URL format

`/api/sn_agent/agents/policies/list`

### Supported request parameters

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|None| |

### Headers

The following request and response headers apply to this HTTP action only, or apply to this action in a distinct way. For a list of general headers used in the REST API, see [Supported REST API headers](c_RESTAPI.md).

<table id="table_d1q_x5w_dpb" class="rest_api_request_headers"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Accept

</td><td id="accept-JSON-only-entry-RESTAPI">

Data format of the response body. Only supports **application/json**.

</td></tr><tr><td>

X-Enc-Query

</td><td>

Optional. Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

X-Include-Check-Params

</td><td>

Optional. Flag that indicates whether to return check instances and their parameters in the results.Valid values:

-   true: Includes check instances and their parameters in the results.
-   false: Do not include check instances and their parameters in the results.

 Default: false

 Data type: Boolean

</td></tr><tr><td>

X-Include-Checks-And-Agents

</td><td>

Optional. Flag that indicates whether to include check instances and agents in the results.Valid values:

-   true: Includes check instances and agents in the results.
-   false: Do not include checks and agents in the results.

 Default: false

 Data type: Boolean

</td></tr></tbody>
</table>|Header|Description|
|------|-----------|
|None| |

### Status codes

The following status codes apply to this HTTP action. For a list of possible status codes used in the REST API, see [REST API HTTP response codes](c_RESTAPI.md).

|Status code|Description|
|-----------|-----------|
|200|Successful. The request was successfully processed.|
|403|The user does not have the agent\_client\_collector\_user role.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policies

</td><td>

List of policies retrieved. Includes checks and agent in results if queried using specific request headers. For information on policies, see [default checks and policies](https://www.servicenow.com/docs/access?context=agent-policies-checks&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).```
{
  "policies": [
    {
      "active": Boolean,
      "agent_ids": "String",
      "checks": [Array],
      "cred_alias": "String",
      "credential_alias": "String",
      "filter": "String",
      "interval": "Number",
      "monitored_ci_group": "String",
      "monitored_ci_script": "String",
      "monitored_ci_type_filter": Boolean,
      "monitored_ci_type_group": Boolean,
      "monitored_ci_type_script": "String",
      "name": "String",
      "params": [Array],
      "publish_status": "String",
      "secure_params": [Array],
      "sys_id": "String",
      "sys_updated_on": "String",
      "table": "String"
    }
  ]
}
```

 Data type: Array

</td></tr><tr><td>

policies.active

</td><td>

Flag that indicates whether the policy is active.Valid values:

-   true: Policy is active.
-   false: Policy isn't active.

Data type: Boolean

</td></tr><tr><td>

policies.agent\_ids

</td><td>

Unique ID of an agent. These results only display if the **X-Include-Checks-And-Agents** header parameter is set to true.For extended information of an agent, run the ID in the [GET /agents/\{agent\_id\}](agnt_clnt_cll-api.md#) endpoint.

Data type: String

Table: In the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.

</td></tr><tr><td>

policies.checks

</td><td>

List of objects defining checks listed in the Check Instances \[sn\_agent\_check\] table. These results only display if the **X-Include-Checks-And-Agents** or **X-Include-Check-Params** header parameter is set to true.Data type: Array of Objects

```
"checks": [
   {
     "active": Boolean,
     "auto_generate": Boolean,
     "check_type": "String"
     "command_prefix": "String",
     "command": "String",
     "event_status_change_threshold": Number,
     "event_status_repair_threshold": Number,
     "interval": Number,
     "name": "String",
     "sys_id": "String",
     "timeout": "String"
   }
]
```

Table:

</td></tr><tr><td>

policies.checks.active

</td><td>

Flag that indicates whether the policy check is active.Valid values:

-   true: Policy check is active.
-   false: Policy check is inactive.

Data type: Boolean

</td></tr><tr><td>

policies.checks.auto\_generate

</td><td>

Flag that indicates whether to automatically generate the command with the **command\_prefix** value.Valid values:

-   true: Automatically populate the **command** property with active parameter values.
-   false: Command isn't automatically generated.

Data type: Boolean

</td></tr><tr><td>

policies.checks.check\_type

</td><td>

Check type specifying the monitoring option.Possible values:

-   Discovery: Check that locates CIs related to the agent.
-   Events: The check's result is transformed into an Event Management event.
-   Metrics: The values from the check result are transformed to metrics.

Data type: String

</td></tr><tr><td>

policies.checks.command

</td><td>

Command that the Agent Client Collector executes. Parameter taken from a template or monitored CI.**Note:** If **auto\_generate** is true, this property is automatically populated with the prefix and flags of the active parameters listed in the **parameters** object.

Data type: String

</td></tr><tr><td>

policies.checks.command\_prefix

</td><td>

If the **auto\_generate** property is true, this command is used for automatic generation. The prefix consists of any portion of the command which is static \(does not change\), such as the script name.Data type: String

</td></tr><tr><td>

policies.checks.event\_status\_change\_threshold

</td><td>

Number of consecutive times that a check's response status must happen before a new event is sent. Returns null if not set.For example, if this value is 3, a check whose response status changes from OK to Error generates a new event with an Error status after the third consecutive occurrence of the status change.

Data type: Number

</td></tr><tr><td>

policies.checks.event\_status\_repair\_threshold

</td><td>

Number of consecutive times that a check's response status must improve to close the previous event. Returns null if not set. For example, if this value is 3, a check whose response status changes from Error to OK closes the previous event and generates a new event with an OK status after the third consecutive occurrence of the status change.

Data type: Number

</td></tr><tr><td>

policies.checks.interval

</td><td>

Amount of time in seconds to wait between check executions. For example, a value of 60 means that the check runs every 60 seconds.Data type: Number

</td></tr><tr><td>

policies.checks.name

</td><td>

Name of the check.Data type: String

</td></tr><tr><td>

policies.checks.sys\_id

</td><td>

Sys\_id of the check.Data type: String

Table: Check Instances \[sn\_agent\_check\]

</td></tr><tr><td>

policies.checks.timeout

</td><td>

Amount of time, in seconds, after which the check execution stops when no output is returned. For example, a value of 60 means that when the check execution doesn't return a value for 60 seconds, the execution stops.Data type: String

</td></tr><tr><td>

policies.cred\_alias

</td><td>

Credential name.Data type: String

Table: Credentials \[discovery\_credentials\]

</td></tr><tr><td>

policies.credential\_alias

</td><td>

Sys\_id of the credential alias.Data type: String

Table: Connection &amp; Credential Aliases \[sys\_alias\]

</td></tr><tr><td>

policies.filter

</td><td>

Filter restricting the policy's checks to monitor only the specified criteria. Data type: String

</td></tr><tr><td>

policies.interval

</td><td>

Amount of time in seconds to wait between policy checks. For example, a value of 60 means that the check runs every 60 seconds.**Note:** The value of the **checks.interval** property overrides the value configured in this field.

Data type: Number

</td></tr><tr><td>

policies.monitored\_ci\_group

</td><td>

Name of the [CMDB groups](https://www.servicenow.com/docs/access?context=cmdb-groups&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) associated with the policy.This field is only applied if the value of the **monitored\_ci\_type\_group** property is true.

Data type: String

Table: CMDB Groups \[cmdb\_group\]

</td></tr><tr><td>

policies.monitored\_ci\_script

</td><td>

Script for monitoring CIs.This field is only applied if the value of the **policies.monitored\_ci\_type\_script** property is true.

Data type: String

</td></tr><tr><td>

policies.monitored\_ci\_type\_filter

</td><td>

Flag that indicates whether filtering by CI type is enabled. The CI type is listed in the **table** property.Valid values:

-   true: Filtering by checks group is enabled.
-   false: Filtering by checks group is disabled.

Data type: Boolean

</td></tr><tr><td>

policies.monitored\_ci\_type\_group

</td><td>

Flag that indicates whether monitoring by CMDB group type is enabled.Valid values:

-   true: CMDB group type is enabled.
-   false: CMDB group type is disabled.

Data type: Boolean

</td></tr><tr><td>

policies.monitored\_ci\_type\_script

</td><td>

Flag that indicates whether the script for monitoring CIs is enabled.Valid values:

-   true: Script for monitoring CIs is enabled.
-   false: Script for monitoring CIs is disabled.

Data type: Boolean

</td></tr><tr><td>

policies.name

</td><td>

Name of the policy.Data type: String

</td></tr><tr><td>

policies.publish\_status

</td><td>

Indicates whether the policy is published. Possible values:

-   Draft: Policy has not been published and is editable using the update endpoints.
-   Published: Policy is published. The draft \(sandbox copy\) and published copy are identical.
-   Published\*: Policy is published, but the draft copy \(sandbox view\) has changes not found in the published copy.

Data type: String

</td></tr><tr><td>

policies.sys\_id

</td><td>

Sys\_id of the policy.Data type: String

Table: Policies \[sn\_agent\_policy\]

</td></tr><tr><td>

policies.sys\_updated\_on

</td><td>

Date and time that the policy was last updated.Data type: String

</td></tr><tr><td>

policies.table

</td><td>

Monitored CI-type field on the policy. This field is only applied if **monitored\_ci\_type\_filter** is true.Data type: String

</td></tr><tr><td>

policies.params

</td><td>

List of objects containing information of check parameters. These results only display if the **X-Include-Check-Params** header parameter is set to true.Data type: Array of Objects

```
"params": [
  {
    "active": Boolean,
    "flag": "String",
    "mandatory: Boolean,
    "name": "String",
    "sys_id": "String",
    "value": "String",
    "value_required": Boolean
  }
]
```

Table: Check Parameters \[sn\_agent\_check\_param\]

</td></tr><tr><td>

policies.params.active

</td><td>

Flag that indicates whether the check parameter is active.Valid values:

-   true: Check parameter is active.
-   false: Check parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

policies.params.flag

</td><td>

Parameter flag to use during check invocation.Data type: String

</td></tr><tr><td>

policies.params.mandatory

</td><td>

Flag that indicates whether this check is mandatory.Valid values:

-   true: This check is mandatory.
-   false: This check is optional.

Data type: Boolean

</td></tr><tr><td>

policies.params.name

</td><td>

Name of the parameter.Data type: String

</td></tr><tr><td>

policies.params.sys\_id

</td><td>

Sys\_id of the parameter.Data type: String

Table: Check Parameters \[sn\_agent\_check\_param\]

</td></tr><tr><td>

policies.params.value

</td><td>

Value of the parameter.Data type: String

</td></tr><tr><td>

policies.params.value\_required

</td><td>

Flag that indicates whether the information provided by the value property is required.Valid values:

-   true: The value property is required.
-   false: The value property is null or not required.

Data type: Boolean

</td></tr><tr><td>

policies.secure\_params

</td><td>

List of objects containing information of check secure parameters. For more information, see [Create a secure parameter for a check](https://www.servicenow.com/docs/access?context=acc-create-secure-params&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US). These results only display if the **X-Include-Check-Params** header parameter is set to true.Data type: Array of Objects

```
"secure_params": [
   {
     "active": Boolean,
     "name": "String",
     "order": Number,
     "sys_id": "String"
   }
]
```

Table: Check Secure Parameters \[sn\_agent\_check\_secure\_param\]

</td></tr><tr><td>

policies.secure\_params.active

</td><td>

Flag that indicates whether the check secure parameter is active.Valid values:

-   true: The check secure parameter is active.
-   false: The check secure parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

policies.secure\_params.name

</td><td>

Name of the secure parameter.Data type: String

</td></tr><tr><td>

policies.secure\_params.order

</td><td>

Order in which the parameter is sent to the check command/script.Data type: Number

</td></tr><tr><td>

policies.secure\_params.sys\_id

</td><td>

Sys\_id of the record.Data type: String

Table: Check Secure Parameter \[sn\_agent\_check\_secure\_param\]

</td></tr></tbody>
</table>### cURL request

The following example shows how to restrict results by query and number. The query returns all active policies and the ID of the associated agent.

```
curl "https://instance.service-now.com/api/sn_agent/agents/policies/list" \
--request GET \
--header "Accept:application/json" \
--header 'X-Enc-Query: active=true ' \
--header 'X-Include-Checks-And-Agents: true' \
--user 'username' : 'password'
```

Output:

```
{
  "policies": [
    {
      "name": "Basic Discovery",
      "sys_id": "68bfd27c536113006dfeddeeff7b12be",
      "active": "true",
      "interval": "43200",
      "sys_updated_on": "2020-07-21 10:14:12",
      "monitored_ci_type_filter": "true",
      "filter": "discovery_source=AgentClientCollector^ORlast_discoveredRELATIVELT@dayofweek@ago@14",
      "table": "cmdb_ci_server",
      "monitored_ci_type_script": "false",
      "monitored_ci_script": "/*\n      Provide a script to get monitored CI type. ...",
      "monitored_ci_type_group": "false",
      "monitored_ci_group": "null// group name as seen in cmdb_group table",
      "cred_alias": "null// credential name as seen in discovery_credentials table",
      "credential_alias": "null// credential alias sys id as seen in sys_alias table",
      "publish_status": "Published",
      "checks": [
        {
          "name": "check-discovery-basic",
          "sys_id": "5b10c644c7e10010b9a4362c14c260aa",
          "active": "true",
          "command": "check_discover.rb",
          "command_prefix": "check_discover.rb",
          "auto_generate": "true",
          "timeout": "60",
          "interval": "43200",
          "event_status_change_threshold": null,
          "event_status_repair_threshold": null,
          "check_type": "Discovery"
        }
      ],
      "agent_ids": "b1faba21b066256f,a088b75b1b25b0a0"
    }
  ]
}
```

## Agent Client Collector - GET /agents/policy/activate/\{policy\_id\}

Activates a published policy.

For a list of published policies, use [GET /agents/policies/list](agnt_clnt_cll-api.md#). This endpoint only supports sys\_ids in which the value of the policy's **publish\_status** property is `Published` or `Published*`.

### URL format

`/api/sn_agent/agents/policy/activate/{policy_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policy\_id

</td><td id="agntCC-entry-parm-policyID-pub">

Sys\_id of the published policy.Data type: String

Table: Policies \[sn\_agent\_policy\]

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_h5l_bgs_2pb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to activate a policy.

```
curl "https://instance.service-now.com/api/sn_agent/agents/policy/activate/<sys_id>" \
--request GET \
--header "Accept:application/json" \
--user 'username' : 'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

## Agent Client Collector - GET /agents/policy/deactivate/\{policy\_id\}

Deactivates a published policy.

For a list of published policies, use [GET /agents/policies/list](agnt_clnt_cll-api.md#). This endpoint only supports sys\_ids in which the value of the policy's **publish\_status** property is `Published` or `Published*`.

### URL format

`/api/sn_agent/agents/policy/activate/{policy_id}`

### Supported request parameters

<table id="table_f4v_qfs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policy\_id

</td><td id="agntCC-entry-parm-policyID-pub">

Sys\_id of the published policy.Data type: String

Table: Policies \[sn\_agent\_policy\]

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_h5l_bgs_2pb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to deactivate a policy.

```
curl "https://instance.service-now.com/api/sn_agent/agents/policy/deactivate/<sys_id>" \
--request GET \
--header "Accept:application/json" \
--user 'username' : 'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

## Agent Client Collector - GET /agents/policy/publish/\{policy\_id\}

Publishes a draft policy.

Use any of the following endpoints to modify a draft or sandbox copy prior to publishing:

-   [POST /agents/update/policy/\{policy\_id\}](agnt_clnt_cll-api.md#)
-   [POST /agents/update/check/\{check\_id\}](agnt_clnt_cll-api.md#)
-   [POST /agents/update/check\_param/\{param\_id\}](agnt_clnt_cll-api.md#)
-   [POST /agents/update/check\_secure\_param/\{param\_id\}](agnt_clnt_cll-api.md#)

### URL format

`/api/sn_agent/agents/policy/publish/{policy_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policy\_id

</td><td>

Sys\_id of a policy in the Policies \[sn\_agent\_policy\] table that is in Draft state or a sandbox copy.-   For a list of policies and details including publish state, use [GET /agents/policies/list](agnt_clnt_cll-api.md#).
-   To retrieve sandbox copy of a policy, use [GET /agents/policy/sandbox\_from\_published/\{policy\_id\}](agnt_clnt_cll-api.md#).

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_h5l_bgs_2pb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to publish a policy.

```
curl "https://instance.service-now.com/api/sn_agent/agents/policy/publish/<sys_id>" \
--request GET \
--header "Accept:application/json" \
--user 'username' : 'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

## Agent Client Collector - GET /agents/policy/sandbox\_from\_published/\{policy\_id\}

Gets the sandbox copy of a published policy and provides policy details.

Use the sandbox copy to make updates to a policy and publish. You can use the sys\_ids in the response body to work with the following endpoints:

-   [POST /agents/update/policy/\{policy\_id\}](agnt_clnt_cll-api.md#)
-   [POST /agents/update/check/\{check\_id\}](agnt_clnt_cll-api.md#)
-   [POST /agents/update/check\_param/\{param\_id\}](agnt_clnt_cll-api.md#)
-   [POST /agents/update/check\_secure\_param/\{param\_id\}](agnt_clnt_cll-api.md#)

For a list of published policies, use [GET /agents/policies/list](agnt_clnt_cll-api.md#). This endpoint only supports sys\_ids in which the value of the policy's **publish\_status** property is `Published` or `Published*`.

### URL format

`/api/sn_agent/agents/policy/sandbox_from_published/{policy_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policy\_id

</td><td id="agntCC-entry-parm-policyID-pub">

Sys\_id of the published policy.Data type: String

Table: Policies \[sn\_agent\_policy\]

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;

</td><td>

Extended details of the sandbox copy associated with the policy. For information on policies, see [default checks and policies](https://www.servicenow.com/docs/access?context=agent-policies-checks&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).```
{
  "active": Boolean"
  "agent_ids": "String",
  "checks": [Array],
  "cred_alias": "String",
  "credential_alias": "String",
  "filter": "String",
  "interval": "Number",
  "monitored_ci_group": "String",
  "monitored_ci_script": "String",
  "monitored_ci_type_filter": Boolean,
  "monitored_ci_type_group": Boolean,
  "monitored_ci_type_script": "String",
  "name": "String",
  "params": [Array],
  "publish_status": "String",
  "secure_params": [Array],
  "sys_id": "String",
  "sys_updated_on": "String",
  "table": "String"
}
```

</td></tr><tr><td>

active

</td><td>

Flag that indicates whether the policy is active.Valid values:

-   true: Policy is active.
-   false: Policy isn't active.

Data type: Boolean

</td></tr><tr><td>

agent\_ids

</td><td>

Unique ID of an agent. These results only display if the **X-Include-Checks-And-Agents** header parameter is set to true.For extended information of an agent, run the ID in the [GET /agents/\{agent\_id\}](agnt_clnt_cll-api.md#) endpoint.

Data type: String

Table: In the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.

</td></tr><tr><td>

checks

</td><td>

List of objects defining checks listed in the Check Instances \[sn\_agent\_check\] table. ```
"checks": [
   {
     "active": Boolean,
     "auto_generate": Boolean,
     "check_type": "String"
     "command_prefix": "String",
     "command": "String",
     "event_status_change_threshold": Number,
     "event_status_repair_threshold": Number,
     "interval": Number,
     "name": "String",
     "sys_id": "String",
     "timeout": "String"
   }
]
```

 Data type: Array

</td></tr><tr><td>

checks.active

</td><td>

Flag that indicates whether the policy check is active.Valid values:

-   true: Policy check is active.
-   false: Policy check is inactive.

Data type: Boolean

</td></tr><tr><td>

checks.auto\_generate

</td><td>

Flag that indicates whether to automatically generate the command with the **command\_prefix** value.Valid values:

-   true: Automatically populate the **command** property with active parameter values.
-   false: Command isn't automatically generated.

Data type: Boolean

</td></tr><tr><td>

checks.check\_type

</td><td>

Check type specifying the monitoring option.Possible values:

-   Discovery: Check that locates CIs related to the agent.
-   Events: The check's result is transformed into an Event Management event.
-   Metrics: The values from the check result are transformed to metrics.

Data type: String

</td></tr><tr><td>

checks.command

</td><td>

Command that the Agent Client Collector executes. Parameter taken from a template or monitored CI.**Note:** If **auto\_generate** is true, this property is automatically populated with the prefix and flags of the active parameters listed in the **parameters** object.

Data type: String

</td></tr><tr><td>

checks.command\_prefix

</td><td>

If the **auto\_generate** property is true, this command is used for automatic generation. The prefix consists of any portion of the command which is static \(does not change\), such as the script name.Data type: String

</td></tr><tr><td>

checks.event\_status\_change\_threshold

</td><td>

Number of consecutive times that a check's response status must happen before a new event is sent. Returns null if not set.For example, if this value is 3, a check whose response status changes from OK to Error generates a new event with an Error status after the third consecutive occurrence of the status change.

Data type: Number

</td></tr><tr><td>

checks.event\_status\_repair\_threshold

</td><td>

Number of consecutive times that a check's response status must improve to close the previous event. Returns null if not set. For example, if this value is 3, a check whose response status changes from Error to OK closes the previous event and generates a new event with an OK status after the third consecutive occurrence of the status change.

Data type: Number

</td></tr><tr><td>

checks.interval

</td><td>

Amount of time in seconds to wait between check executions. For example, a value of 60 means that the check runs every 60 seconds.Data type: Number

</td></tr><tr><td>

checks.name

</td><td>

Name of the check.Data type: String

</td></tr><tr><td>

checks.sys\_id

</td><td>

Sys\_id of the check. The [POST /agents/update/check/\{check\_id\}](agnt_clnt_cll-api.md#) endpoint takes this value to update the sandbox copy.Data type: String

Table: Check Instances \[sn\_agent\_check\]

</td></tr><tr><td>

checks.timeout

</td><td>

Amount of time, in seconds, after which the check execution stops when no output is returned. For example, a value of 60 means that when the check execution doesn't return a value for 60 seconds, the execution stops.Data type: String

</td></tr><tr><td>

cred\_alias

</td><td>

Credential name.Data type: String

Table: Credentials \[discovery\_credentials\]

</td></tr><tr><td>

credential\_alias

</td><td>

Sys\_id of the credential alias.Data type: String

Table: Connection &amp; Credential Aliases \[sys\_alias\]

</td></tr><tr><td>

filter

</td><td>

Filter restricting the policy's checks to monitor only the specified criteria. Data type: String

</td></tr><tr><td>

interval

</td><td>

Amount of time in seconds to wait between policy checks. For example, a value of 60 means that the check runs every 60 seconds.**Note:** The value of the **checks.interval** property overrides the value configured in this field.

Data type: Number

</td></tr><tr><td>

monitored\_ci\_group

</td><td>

Name of the [CMDB groups](https://www.servicenow.com/docs/access?context=cmdb-groups&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) associated with the policy.This field is only applied if the value of the **monitored\_ci\_type\_group** property is true.

Data type: String

Table: CMDB Groups \[cmdb\_group\]

</td></tr><tr><td>

monitored\_ci\_script

</td><td>

Script for monitoring CIs.This field is only applied if the value of the **policies.monitored\_ci\_type\_script** property is true.

Data type: String

</td></tr><tr><td>

monitored\_ci\_type\_filter

</td><td>

Flag that indicates whether filtering by CI type is enabled. The CI type is listed in the **table** property.Valid values:

-   true: Filtering by checks group is enabled.
-   false: Filtering by checks group is disabled.

Data type: Boolean

</td></tr><tr><td>

monitored\_ci\_type\_group

</td><td>

Flag that indicates whether monitoring by CMDB group type is enabled.Valid values:

-   true: CMDB group type is enabled.
-   false: CMDB group type is disabled.

Data type: Boolean

</td></tr><tr><td>

monitored\_ci\_type\_script

</td><td>

Flag that indicates whether the script for monitoring CIs is enabled.Valid values:

-   true: Script for monitoring CIs is enabled.
-   false: Script for monitoring CIs is disabled.

Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Name of the policy.Data type: String

</td></tr><tr><td>

publish\_status

</td><td>

Indicates whether the policy is published. Possible values:

-   Draft: Policy has not been published and is editable using the update endpoints.
-   Published: Policy is published. The draft \(sandbox copy\) and published copy are identical.
-   Published\*: Policy is published, but the draft copy \(sandbox view\) has changes not found in the published copy.

Data type: String

</td></tr><tr><td>

params

</td><td>

List of objects containing information of check parameters. These results only display if the **X-Include-Check-Params** header parameter is set to true.Data type: Array of Objects

```
"params": [
  {
    "active": Boolean,
    "flag": "String",
    "mandatory: Boolean,
    "name": "String",
    "sys_id": "String",
    "value": "String",
    "value_required": Boolean
  }
]
```

Table: Check Parameters \[sn\_agent\_check\_param\]

</td></tr><tr><td>

params.active

</td><td>

Flag that indicates whether the check parameter is active.Valid values:

-   true: Check parameter is active.
-   false: Check parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

params.flag

</td><td>

Parameter flag to use during check invocation.Data type: String

</td></tr><tr><td>

params.mandatory

</td><td>

Flag that indicates whether this check is mandatory.Valid values:

-   true: This check is mandatory.
-   false: This check is optional.

Data type: Boolean

</td></tr><tr><td>

params.name

</td><td>

Name of the parameter.Data type: String

</td></tr><tr><td>

params.sys\_id

</td><td>

Sys\_id of the parameter listed in the Check Parameters \[sn\_agent\_check\_param\] table. The [POST /agents/update/check\_param/\{param\_id\}](agnt_clnt_cll-api.md#) endpoint takes this value to update the sandbox copy.Data type: String

</td></tr><tr><td>

params.value

</td><td>

Value of the parameter.Data type: String

</td></tr><tr><td>

params.value\_required

</td><td>

Flag that indicates whether the information provided by the value property is required.Valid values:

-   true: The value property is required.
-   false: The value property is null or not required.

Data type: Boolean

</td></tr><tr><td>

secure\_params

</td><td>

List of objects containing information of check secure parameters. For more information, see [Create a secure parameter for a check](https://www.servicenow.com/docs/access?context=acc-create-secure-params&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US). These results only display if the **X-Include-Check-Params** header parameter is set to true.Data type: Array of Objects

```
"secure_params": [
   {
     "active": Boolean,
     "name": "String",
     "order": Number,
     "sys_id": "String"
   }
]
```

Table: Check Secure Parameters \[sn\_agent\_check\_secure\_param\]

</td></tr><tr><td>

secure\_params.active

</td><td>

Flag that indicates whether the check secure parameter is active.Valid values:

-   true: The check secure parameter is active.
-   false: The check secure parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

secure\_params.name

</td><td>

Name of the secure parameter.Data type: String

</td></tr><tr><td>

secure\_params.order

</td><td>

Order in which the parameter is sent to the check command/script.Data type: Number

</td></tr><tr><td>

secure\_params.sys\_id

</td><td>

Sys\_id of the record. The [POST /agents/update/check\_secure\_param/\{param\_id\}](agnt_clnt_cll-api.md#) endpoint takes this value to update the sandbox copy.Data type: String

Table: Check Secure Parameter \[sn\_agent\_check\_secure\_param\]

</td></tr><tr><td>

sys\_id

</td><td>

Sys\_id of the policy. The [POST /agents/update/policy/\{policy\_id\}](agnt_clnt_cll-api.md#) endpoint takes this value to update the sandbox copy.Data type: String

Table: Policies \[sn\_agent\_policy\]

</td></tr><tr><td>

sys\_updated\_on

</td><td>

Date and time that the policy was last updated.Data type: String

</td></tr><tr><td>

table

</td><td>

Monitored CI-type field on the policy. This field is only applied if **monitored\_ci\_type\_filter** is true.Data type: String

</td></tr></tbody>
</table>### cURL request

The following shows how to get information of the Docker Container Metrics policy.

```
curl "https://instance.service-now.com/api/sn_agent/agents/policy/sandbox_from_published/<sys_id>" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'
```

Output:

```
{
  "name": "Docker Container Metrics",
  "sys_id": "b01e609a1b9fe4943e7f0b05464bcb91",
  "active": "false",
  "interval": "60",
  "sys_updated_on": "2021-04-05 19:52:28",
  "monitored_ci_type_filter": "true",
  "filter": "operational_status=1",
  "table": "cmdb_ci_docker_container",
  "monitored_ci_type_script": "false",
  "monitored_ci_script": "/*\n Provide a script to get monitored CI type.",
  "monitored_ci_type_group": "false",
  "monitored_ci_group": "null// group name as seen in cmdb_group table",
  "cred_alias": "null// credential name as seen in discovery_credentials table",
  "credential_alias": "null// credential alias sys id as seen in sys_alias table",
  "publish_status": "Published",
  "checks": [
    {
      "name": "container.docker.metrics-docker",
      "sys_id": "701e609a1b9fe4943e7f0b05464bcb94",
      "active": "true",
      "command": "metrics-docker-stats.rb -N {{.labels.params_ci_container_id}} -P -n -i",
      "command_prefix": "metrics-docker-stats.rb -N {{.labels.params_ci_container_id}}",
      "auto_generate": "true",
      "timeout": "60",
      "interval": "60",
      "event_status_change_threshold": null,
      "event_status_repair_threshold": null,
      "check_type": "Metrics",
      "params": [
        {
          "name": "scheme",
          "sys_id": "c11e609a1b9fe4943e7f0b05464bcb97",
          "value": null,
          "active": "false",
          "mandatory": "false",
          "value_required": "true",
          "flag": "-s"
        },
        ...
        {
          "name": "docker_host",
          "sys_id": "cd1e609a1b9fe4943e7f0b05464bcb97",
          "value": null,
          "active": "false",
          "mandatory": "false",
          "value_required": "true",
          "flag": "-H"
        }
      ],
      "secure_params": []
    }
  ]
}
```

## Agent Client Collector - GET /agents/\{agent\_id\}/restart

Restarts a specified agent with alive/up status.

If Agent Client Collector performance issues occur, you can restart the agent. Manual restart is supported in the following environments:

-   Linux-based agents using `systemd`
-   Windows agents

### URL format

`/api/sn_agent/agents/{agent_id}/restart`

### Supported request parameters

<table id="table_oyt_cd3_dpb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agent\_id

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table. For a list of agent IDs and other details, run the GET /agents/list endpoint.

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id or this agent does not support restart.|

### Response body parameters \(JSON\)

<table id="table_owl_zyc_z4b"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to restart an agent.

```
curl "https://instance.service-now.com/api/sn_agent/agents/<agent_id>/restart" \
--request GET \
--header "Accept:application/json" \
--user 'username':'password'

```

Output:

```
{
  "message": "Restarting Agent With ID: <agent_id>"
}
```

## Agent Client Collector - POST /agents/check\_defs/\{check\_def\_id\}/run

Runs a check against the given configuration item.

To stop a background check, use the request ID provided in the GET /agents/exec/background/stop/\{request\_id\} API.

### URL format

`/api/sn_agent/agents/check_defs/{check_def_id}/run`

### Supported request parameters

|Name|Description|
|----|-----------|
|check\_def\_id|Sys\_id of a check definition in the Check Definitions \[sn\_agent\_check\_def\] table.|

|Name|Description|
|----|-----------|
|None| |

<table id="table_cvh_5gq_wqb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

params

</td><td>

Map of parameter names and values. These settings can be used to override the parameter records of the check definition and its specified values. ```
"params": {
  "<parameter name>": "String"
}
```

 Data type: Object

</td></tr><tr><td>

priority

</td><td>

Priority of the request to be set on the ECC queue. Possible values:

-   0: interactive
-   1: expedited
-   2: standard

 Data type: Number

</td></tr><tr><td>

query

</td><td>

Encoded query for retrieving the GlideRecord from the table specified in the **table** property.Data type: String

</td></tr><tr><td>

table

</td><td>

Name of the cmdb\_ci table for this background check.Data type: String

</td></tr><tr><td>

timeout

</td><td>

Value of the timeout for the request in seconds. Data type: Number

</td></tr></tbody>
</table>### Headers

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
|400|The is an error in the arguments provided in the request body.|
|404|The check definition with the ID provided is not found.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|requestId|Sys\_id of the generated background check request.|

### cURL request

The following example shows how to run a background check and get its request ID.

```
curl "https://instance.service-now.com/api/sn_agent/agents/check_defs/a90d3c361be1301060d2773ad54bcb6f/run" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"table\":\"sn_agent_check_def\"}" \
--user 'username':'password'
```

Output:

```
{
  "request_id": "278c0170db2a30108a0751f4f3961926"
}
```

## Agent Client Collector - POST /agents/check\_defs/\{check\_def\_id\}/test

Enables building test check requests on check definitions.

Use this API for the following tasks:

-   Set the check definition to test
-   Set the configuration item to run the test against

You can also specify one of the following identifiers to use during the test:

-   Credential sys\_id
-   Credential alias id
-   Credential name

### URL format

`/api/sn_agent/agents/check_defs/{check_def_id}/test`

### Supported request parameters

|Name|Description|
|----|-----------|
|check\_def\_id|Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table.|

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|ci\_id|Sys\_id of a CMDB Configuration Item.|
|credentials\_id|Sys\_id of a credentials record.|
|credentials\_name|Name of the credentials record.|
|credentials\_alias\_id|Sys\_id of a credentials alias record.|
|credentials\_alias\_name|Name of a credentials alias.|

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
|500|Error building the test request.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|result\_id|Sys\_id of the test result record.|

## Agent Client Collector - POST /agents/check\_instances/\{check\_instance\_id\}/test

Enables building test check requests on check instances.

Use this API for the following tasks:

-   Set the check instance to test
-   Set the configuration item to run the test against

You can also specify one of the following identifiers to use during the test:

-   Credential sys\_id
-   Credential alias id
-   Credential name

### URL format

`/api/sn_agent/agents/check_instances/{check_instance_id}/test`

### Supported request parameters

|Name|Description|
|----|-----------|
|check\_instance\_id|Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table.|

|Name|Description|
|----|-----------|
|None| |

|Name|Description|
|----|-----------|
|ci\_id|Sys\_id of a CMDB Configuration Item.|
|credentials\_id|Sys\_id of a credentials record.|
|credentials\_name|Name of the credentials record.|
|credentials\_alias\_id|Sys\_id of a credentials alias record.|
|credentials\_alias\_name|Name of a credentials alias.|
|proxy\_agent\_id|Unique ID of an agent proxy to run this check. This value is listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.|

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
|500|Error building the test request.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|result\_id|Sys\_id of the test result record.|

## Agent Client Collector - POST /agents/update/check/\{check\_id\}

Updates a selected policy check.

To retrieve the properties of a policy sandbox copy, use [GET /agents/policy/sandbox\_from\_published/\{policy\_id\}](agnt_clnt_cll-api.md#).

### URL format

`/api/sn_agent/agents/update/check/{check_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check\_id

</td><td>

Sys\_id of a policy check sandbox copy in the Check Instances \[sn\_agent\_check\] table.Data type: String

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_xvx_g2z_2pb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the policy check is active.Valid values:

-   true: Policy check is active.
-   false: Policy check is inactive.

Data type: Boolean

</td></tr><tr><td>

auto\_generate

</td><td>

Flag that indicates whether to automatically generate the command with the **command\_prefix** value.Valid values:

-   true: Automatically populate the **command** property with active parameter values.
-   false: Command isn't automatically generated.

Data type: Boolean

</td></tr><tr><td>

check\_type

</td><td>

Check type specifying the monitoring option.Possible values:

-   Discovery: Check that locates CIs related to the agent.
-   Events: The check's result is transformed into an Event Management event.
-   Metrics: The values from the check result are transformed to metrics.

Data type: String

</td></tr><tr><td>

command

</td><td>

Command that the Agent Client Collector executes. Parameter taken from a template or monitored CI.**Note:** If **auto\_generate** is true, this property is automatically populated with the prefix and flags of the active parameters listed in the **parameters** object.

Data type: String

</td></tr><tr><td>

command\_prefix

</td><td>

If the **auto\_generate** property is true, this command is used for automatic generation. The prefix consists of any portion of the command which is static \(does not change\), such as the script name.Data type: String

</td></tr><tr><td>

event\_status\_change\_threshold

</td><td>

Number of consecutive times that a check's response status must happen before a new event is sent. Returns null if not set.For example, if this value is 3, a check whose response status changes from OK to Error generates a new event with an Error status after the third consecutive occurrence of the status change.

Data type: Number

</td></tr><tr><td>

event\_status\_repair\_threshold

</td><td>

Number of consecutive times that a check's response status must improve to close the previous event. Returns null if not set. For example, if this value is 3, a check whose response status changes from Error to OK closes the previous event and generates a new event with an OK status after the third consecutive occurrence of the status change.

Data type: Number

</td></tr><tr><td>

interval

</td><td>

Amount of time in seconds to wait between check executions. For example, a value of 60 means that the check runs every 60 seconds.Data type: Number

</td></tr><tr><td>

name

</td><td>

Name of the check.Data type: String

</td></tr><tr><td>

timeout

</td><td>

Amount of time, in seconds, after which the check execution stops when no output is returned. For example, a value of 60 means that when the check execution doesn't return a value for 60 seconds, the execution stops.Data type: String

</td></tr></tbody>
</table>### Headers

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_ewx_g2z_2pb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to update the event change and repair properties of a policy check.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/check/<check_sys_id>" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
    \"event_status_change_threshold\" : \"2\",
    \"event_status_repair_threshold\" : \"1\"
}" \
--user 'username':'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

## Agent Client Collector - POST /agents/update/check\_def\_params/\{check\_def\_param\_id\}

Enables changing one or more field values of a specified check parameter.

### URL format

`/api/sn_agent/agents/update/check_def_params/{check_def_param_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check\_def\_param\_id

</td><td>

Sys\_id of the check parameter.Data type: String

Table: Check Parameter Definitions \[sn\_agent\_check\_param\_def\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_fhm_klr_wqb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the check parameter is active.Valid values:

-   true: The check parameter is active.
-   false: The check parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

default\_value

</td><td>

Specifies the default value for this check parameter.Data type: String

</td></tr><tr><td>

mandatory

</td><td>

Flag that indicates whether the check parameter is required.

 Valid values:

-   true: The check parameter is required.
-   false: The check parameter is optional.

 Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Name of the check parameter.Data type: String

</td></tr></tbody>
</table>**Note:** Refer to the data dictionary for a comprehensive list of Check Definition fields and types.

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
|404|The check parameter was not found with sys\_id provided.|
|500|Error updating the check parameter.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|None|Success or error message.|

### cURL request

The following example shows how to activate a check parameter.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/check_def_params/02d89bb01b307490f271ea42b24bcb63" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"active\":\"true\"}" \
--user 'username':'password'
```

Output:

```
"message": "Check Definition Parameter Updated Successfully"
```

## Agent Client Collector - POST /agents/update/check\_def\_secure\_params/\{check\_def\_secure\_param\_id\}

Enables changing one or more field values of a specified check secure parameter.

### URL format

`/api/sn_agent/agents/update/check_def_secure_params/{check_def_secure_param_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check\_def\_secure\_param\_id

</td><td>

Sys\_id of the secure parameter.Data type: String

Table: Check Secure Parameter Definitions \[sn\_agent\_check\_secure\_param\_def\]

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

Flag that indicates whether the secure parameter is active.Valid values:

-   true: The secure parameter is active.
-   false: The secure parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Name of the secure parameter.Data type: String

</td></tr><tr><td>

order

</td><td>

Order in which the parameter is sent to the check command/script.Data type: String

</td></tr></tbody>
</table>### Headers

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
|404|The check secure parameter was not found with sys\_id provided.|
|500|Error updating the check secure parameter.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|None|Success or error message.|

### cURL request

The following example shows how to activate a check secure parameter.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/check_def_secure_params/2d30a066dba530106f4810284b9619c1" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"active\":\"true\"}" \
--user 'username':'password'
```

Output:

```
"message": "Check Definition Secure Parameter Updated Successfully"
```

## Agent Client Collector - POST /agents/update/check\_defs/\{check\_def\_id\}

Enables changing one or more field values of a specified check definition.

### URL format

`/api/sn_agent/agents/update/check_defs/{check_def_id}`

### Supported request parameters

<table class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

check\_def\_id

</td><td>

Sys\_id of the check definition listed in the Check Definitions \[sn\_agent\_check\_def\] table. Data type: String

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

Indicates whether this check definition is active.Valid values:

-   0: This check definition is inactive.
-   1: This check definition is active.

 Data type: Number

</td></tr><tr><td>

background

</td><td>

Flag that indicates whether this check definition is a background check. A background check is a check which the agent starts execution of and doesn’t wait for it to finish running.Valid values:

-   true: This check definition is a background check.
-   false: This check definition is not a background check.

 Data type: Boolean

</td></tr><tr><td>

check\_group

</td><td>

Group specified for this check definition.

</td></tr><tr><td>

check\_type

</td><td>

Type of check.Possible values:

-   Events – Check results are transformed into an Event Management event.
-   Metrics – Values from the check result are transformed to metrics.

 Data type: String

</td></tr><tr><td>

command

</td><td>

Command that the Agent Client Collector executes.Data type: String

</td></tr><tr><td>

name

</td><td>

Name of the check.Data type: String

</td></tr><tr><td>

params

</td><td>

Map of parameter names and values. These settings can be used to override the parameter records of the check definition and its specified values. ```
"params": {
  "<parameter name>": "String"
}
```

 Data type: Object

</td></tr><tr><td>

plugins

</td><td>

List of [Agent Client Collector plugins](https://www.servicenow.com/docs/access?context=acc-assets&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US) associated with this check.Data type: Array

</td></tr><tr><td>

proxy\_valid

</td><td>

Flag that indicates whether the check definition policy is set to work as a proxy.

 Valid values:

-   true: This check definition policy is set to work as a proxy.
-   false: This check definition policy is not set to work as a proxy.

 Data type: Boolean

</td></tr><tr><td>

query

</td><td>

Encoded query for retrieving the GlideRecord from the table specified in the **table** property.Data type: String

</td></tr><tr><td>

table

</td><td>

Name of the cmdb\_ci table for this check.Data type: String

</td></tr><tr><td>

timeout

</td><td>

Timeout in seconds.Data type: Number

</td></tr></tbody>
</table>**Note:** Refer to the data dictionary for a comprehensive list of Check Definition fields and types.

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
|404|The check definition was not found with sys\_id provided.|
|500|Error updating the check definition.|

### Response body parameters \(JSON\)

|Name|Description|
|----|-----------|
|None|Success or error message.|

### cURL request

The following example shows how to deactivate a check definition.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/check_defs/99e12466dba530106f4810284b961976" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{\"active\":\"false\"}" \
--user 'username':'password'
```

Output:

```
"message": "Check Definition Updated Successfully"
```

## Agent Client Collector - POST /agents/update/check\_param/\{param\_id\}

Updates a selected policy check parameter.

To retrieve the properties of a policy sandbox copy, use [GET /agents/policy/sandbox\_from\_published/\{policy\_id\}](agnt_clnt_cll-api.md#).

### URL format

`/api/sn_agent/agents/update/check_param/{param_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

param\_id

</td><td>

Sys\_id of policy check parameter sandbox copy.Data type: String

Table: Check Parameters \[sn\_agent\_check\_param\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_fvh_g2z_2pb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the check parameter is active.Valid values:

-   true: Check parameter is active.
-   false: Check parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

flag

</td><td>

 

</td></tr><tr><td>

mandatory

</td><td>

Flag that indicates whether this check is mandatory.Valid values:

-   true: This check is mandatory.
-   false: This check is optional.

Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Name of the parameter.Data type: String

</td></tr><tr><td>

value

</td><td>

Value of the parameter.Data type: String

</td></tr><tr><td>

value\_required

</td><td>

Flag that indicates whether the information provided by the value property is required.Valid values:

-   true: The value property is required.
-   false: The value property is null or not required.

Data type: Boolean

</td></tr></tbody>
</table>### Headers

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_mvh_g2z_2pb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to update several properties of a policy check parameter.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/check_param/<param_sys_id>" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"flag\" : \"-d\",
   \"mandatory\" : \"true\",
   \"name\" : \"scheme2\",
   \"value\" : \"120\",
   \"value_required\" : \"false\"
}" \
--user 'username':'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

## Agent Client Collector - POST /agents/update/check\_secure\_param/\{param\_id\}

Updates a selected policy check secure parameter.

To retrieve the properties of a policy sandbox copy, use [GET /agents/policy/sandbox\_from\_published/\{policy\_id\}](agnt_clnt_cll-api.md#).

### URL format

`/api/sn_agent/agents/update/check_secure_param/{param_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

param\_id

</td><td>

Sys\_id of the policy check secure parameter sandbox copy.Data type: String

Table: Check Secure Parameter \[sn\_agent\_check\_secure\_param\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table id="table_fzx_f2z_2pb" class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

active

</td><td>

Flag that indicates whether the check secure parameter is active.Valid values:

-   true: The check secure parameter is active.
-   false: The check secure parameter is inactive.

Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Name of the secure parameter.Data type: String

</td></tr><tr><td>

order

</td><td>

Order in which the parameter is sent to the check command/script.Data type: Number

</td></tr></tbody>
</table>### Headers

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table id="table_mzx_f2z_2pb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to update the properties of a policy check secure parameter.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/check_secure_param/<param_sys_id>" \
--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
   \"name\" : \"new name\",
   \"order\" : \"2\"
}" \
--user 'username':'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

## Agent Client Collector - POST /agents/update/policy/\{policy\_id\}

Updates a sandbox copy of a policy.

To retrieve the properties of a policy sandbox copy, use [GET /agents/policy/sandbox\_from\_published/\{policy\_id\}](agnt_clnt_cll-api.md#).

### URL format

`/api/sn_agent/agents/update/policy/{policy_id}`

### Supported request parameters

<table id="table_n3g_1fs_2pb" class="rest_api_path_parameters"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

policy\_id

</td><td>

Sys\_id of a policy sandbox copy.Data type: String

Table: Policies \[sn\_agent\_policy\]

</td></tr></tbody>
</table>|Name|Description|
|----|-----------|
|None| |

<table class="rest_api_request_body"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

cred\_alias

</td><td>

Credential name.Data type: String

Table: Credentials \[discovery\_credentials\]

</td></tr><tr><td>

credential\_alias

</td><td>

Sys\_id of the credential alias.Data type: String

Table: Connection &amp; Credential Aliases \[sys\_alias\]

</td></tr><tr><td>

filter

</td><td>

Filter restricting the policy's checks to monitor only the specified criteria. Data type: String

</td></tr><tr><td>

interval

</td><td>

Amount of time in seconds to wait between policy checks. For example, a value of 60 means that the check runs every 60 seconds.**Note:** The value of the **checks.interval** property overrides the value configured in this field.

Data type: Number

</td></tr><tr><td>

monitored\_ci\_group

</td><td>

Name of the [CMDB groups](https://www.servicenow.com/docs/access?context=cmdb-groups&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) associated with the policy.This field is only applied if the value of the **monitored\_ci\_type\_group** property is true.

Data type: String

Table: CMDB Groups \[cmdb\_group\]

</td></tr><tr><td>

monitored\_ci\_script

</td><td>

Script for monitoring CIs.This field is only applied if the value of the **policies.monitored\_ci\_type\_script** property is true.

Data type: String

</td></tr><tr><td>

monitored\_ci\_type\_filter

</td><td>

Flag that indicates whether filtering by CI type is enabled. The CI type is listed in the **table** property.Valid values:

-   true: Filtering by checks group is enabled.
-   false: Filtering by checks group is disabled.

Data type: Boolean

</td></tr><tr><td>

monitored\_ci\_type\_group

</td><td>

Flag that indicates whether monitoring by CMDB group type is enabled.Valid values:

-   true: CMDB group type is enabled.
-   false: CMDB group type is disabled.

Data type: Boolean

</td></tr><tr><td>

monitored\_ci\_type\_script

</td><td>

Flag that indicates whether the script for monitoring CIs is enabled.Valid values:

-   true: Script for monitoring CIs is enabled.
-   false: Script for monitoring CIs is disabled.

Data type: Boolean

</td></tr><tr><td>

name

</td><td>

Name of the policy.Data type: String

</td></tr><tr><td>

table

</td><td>

Monitored CI-type field on the policy. This field is only applied if **monitored\_ci\_type\_filter** is true.Data type: String

</td></tr></tbody>
</table>### Headers

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
|403|The user does not have the agent\_client\_collector\_admin role.|
|404|No record found with the provided sys\_id.|
|500|Internal server error. An unexpected error occurred while processing the request. The response contains additional information about the error.|

### Response body parameters \(JSON\)

<table><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Message containing operation success or failure results.Data type: String

</td></tr></tbody>
</table>### cURL request

The following example shows how to update the name and filter properties/fields of a policy.

```
curl "https://instance.service-now.com/api/sn_agent/agents/update/policy/<policy_sys_id>" \--request POST \
--header "Accept:application/json" \
--header "Content-Type:application/json" \
--data "{
  \"name\" : \"new policy name\",
  \"filter\" : \"operational_status=1\"
}" \
--user 'username':'password'
```

Output:

```
{
  "message": "Operation was successful"
}
```

