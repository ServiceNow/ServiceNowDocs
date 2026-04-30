---
title: AccAgentsAPI - Scoped
description: The AccAgentsAPI script include enables you to perform management actions on available agents.Creates an AccAgentsAPI instance.Checks the status of a grab log request.Gets the information of a specified agent.Gets a list of agents with related information.Restarts a specified agent with alive/up status.Runs a discovery check to locate CIs related to an agent. The specified agent must be in alive/up status.Set the given data collection status \(true/false if enabled or not\) for a specified agent.Requests the log of a specified agent with alive/up status.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# AccAgentsAPI- Scoped

The AccAgentsAPI script include enables you to perform management actions on available agents.

This script include requires the Agent Client Collector Framework \(sn\_agent\) store application and is provided within the `sn_agent` namespace. For more information, refer to [Agent Client Collector](https://www.servicenow.com/docs/access?context=acc-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

For the REST API solution, refer to [Agent Client Collector API](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#).

This script include provides methods that enable the following:

-   Getting extensive information of one or more agents.
-   Submitting a request to grab an agent log and retrieving information about the request progress.
-   Starting or stopping data collection.
-   Restarting an agent.
-   Running discovery on an agent.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## AccAgentsAPI - AccAgentsAPI\(\)

Creates an AccAgentsAPI instance.

|Name|Type|Description|
|----|----|-----------|
|None| | |

The following example shows how to initialize AccAgentsAPI.

```
var agentsApi = new sn_agent.AccAgentsAPI();
```

## AccAgentsAPI - checkGrabLogRequestProgress\(String requestId\)

Checks the status of a grab log request.

Run the [submitGrabLogRequest\(\)](AccAgentsAPIAPIScoped.md#) method to get a request ID.

|Name|Type|Description|
|----|----|-----------|
|requestId|String|Sys\_id of a request in the Agent Client Collector Requests \[sn\_agent\_request\] table.|

<table id="table_al2_2g2_z4b" class="returns"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;

</td><td>

JSON object containing the grab log request status.```
{
  "status": Number,
  "output": "String"
}
```

</td></tr><tr><td>

status

</td><td>

Number indicating status of the grab log request.Possible values:

-   0: Grab log request is complete.
-   1: Grab log request in progress.
-   2: Grab log request timed out.
-   3: Grab log request has an error.
-   4: Grab log request was not found.

</td></tr><tr><td>

output

</td><td>

Information describing the status.

</td></tr></tbody>
</table>The following example shows how to use a request ID to get the status of a grab log request.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var logRequestStatus = agentsApi.checkGrabLogRequestProgress("<request_ID>");

gs.info(JSON.stringify(logRequestStatus, null, 2));
```

Output:

```
{
  "status": 2,
  "output": "Grab Log Request Timed Out"
}
```

## AccAgentsAPI - getAgent\(String agentID\)

Gets the information of a specified agent.

To get a list of agent IDs:

-   Run the getAgentsList\(\) method.
-   Check the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.
-   Run the [Agent Client Collector GET list](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#) REST API.

|Name|Type|Description|
|----|----|-----------|
|agentID|String|Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.|

<table id="table_al2_2g2_z4b" class="returns"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;

</td><td>

Object containing extended agent information.```
{
  "error": String,
  "agent": Object
}
```

</td></tr><tr><td>

error

</td><td id="accAgents-rtrns-error">

Error message. Null if there is no error.Data type: String

</td></tr><tr><td>

agent

</td><td>

```
"agent": {
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

agent.agent\_id

</td><td>

ID of the agent as submitted.Data type: String

</td></tr><tr><td>

agent.data\_collection

</td><td>

Data collection indicates whether scheduled checks are to be run. These checks are a part of the policies scheduled for this agent to run.Possible values:

-   0: On – Checks run as scheduled.
-   1: Off \(manual\) – Checks have been disabled manually.
-   2: Off \(auto\) – Checks have been disabled automatically due to high CPU consumption by the

 Data type: Number

</td></tr><tr><td>

agent.ip\_address

</td><td>

Agent IP address.Data type: String

</td></tr><tr><td>

agent.is\_duplicate

</td><td>

Flag that indicates whether this agent is a duplicate of another. There should be only a single agent on a given host.

 Possible values:

-   true: The agent has the same host as an Alive/Up agent with a different agent ID. Turn off or uninstall the duplicate
-   false: This agent has no duplicates in the Alive/Up state.

 Data type: Boolean

</td></tr><tr><td>

agent.is\_restart\_enabled

</td><td>

Flag that indicates whether restart is enabled. Agent restart is not configurable. It depends on the OS and the version of the OS the agent is running on.

 Possible values:

-   true: Restart is enabled for this agent.
-   false: Restart is disabled for this agent.

 Data type: Boolean

</td></tr><tr><td>

agent.name

</td><td>

Name of the agent.Data type: String

</td></tr><tr><td>

agent.number\_of\_running\_checks

</td><td>

The number of checks the agent is scheduled to run. These checks are a part of the policies scheduled for this agent to run.Data type: Number

</td></tr><tr><td>

agent.status

</td><td>

Status of the agent.Possible values:

-   0: Alive/Up – The agent is active.
-   1: Warning – The agent has not received a keep-alive message in the past few minutes.
-   2: Down – The agent has not received a keep-alive message in a long time.
-   3: Restarting – The agent is restarting.

 Data type: Number

</td></tr><tr><td>

agent.up\_since

</td><td>

UTC time since the agent's status became alive/up. The value is in [GlideDateTime](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) format.Data type: String

</td></tr><tr><td>

agent.version

</td><td>

Version of Agent Client Collector the agent is running.Data type: String

</td></tr></tbody>
</table>The following example shows how to display an agent's status.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var agentInfo = agentsAPI.getAgent("<agent_ID>");

if (!gs.nil(agentInfo.error))
	gs.error(agentInfo.error);
else
	gs.info("agent status: " + agentInfo.agent.status);

```

Output:

```
agent status: 2
```

The following example shows how to get all agent details.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var agentInfo = agentsAPI.getAgent("<agent_ID>");

gs.info(JSON.stringify(agentInfo, null, 2));
```

Output:

```
{
  "error": null,
  "agent": {
    "name": "win2016-dc-64bit",
    "status": 0,
    "agent_id": "<agent_ID>",
    "ip_address": "10.222.333.42",
    "number_of_running_checks": 1,
    "data_collection": 0,
    "is_restart_enabled": true,
    "is_duplicate": false,
    "up_since": "2021-03-24 11:04:38",
    "version": "2.4.0"
  }
}
```

## AccAgentsAPI – getAgentsList\(String encodedQuery, Number limit\)

Gets a list of agents with related information.

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

encodedQuery

</td><td>

String

</td><td>

Encoded query string in standard Glide format. See [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

limit

</td><td>

Number

</td><td>

Optional. Restricts results to a maximum number of agents. Use null or undefined for both if they are not required.Default/Max: 20,000

</td></tr></tbody>
</table><table id="table_al2_2g2_z4b" class="returns"><thead><tr><th>

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

UTC time since the agent's status became alive/up. The value is in [GlideDateTime](../../glideDateTimeScoped/concept/c_GlideDateTimeScoped.md#) format.Data type: String

</td></tr><tr><td>

version

</td><td id="accAgents-parm-agent-obj-version-entry">

Version of Agent Client Collector the agent is running.Data type: String

</td></tr></tbody>
</table>The following example shows how to restrict results by query and number. The query returns all agents that are not in the down state with a maximum of two results.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var agentList = agentsApi.getAgentsList("agent_extended_info.status!=2", 2);

gs.info(JSON.stringify(agentList, null, 2));
```

Output:

```
[
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
```

The following example shows how to list every agent in the system. This example uses no query and no maximum number of results.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var agentList = agentsApi.getAgentsList(null, 0);

gs.info(JSON.stringify(agentList, null, 2));
```

The following example shows how to iterate over the results provided and displays each agent ID.

```
var agentsApi = new sn_agent.AccAgentsAPI();

var agentsList = agentsApi.getAgentsList(null, 0);
for (var i = 0; i < agentsList.length; i++)
   gs.info("agent with id: " + agentsList[i].agent_id);
```

Output:

```
sn_agent: agent with id: 000a00e0aa1aa3a4
sn_agent: agent with id: 000a00e1aa1aa3a4
sn_agent: agent with id: 000a00e2aa1aa3a4
```

## AccAgentsAPI - restartAgent\(String agentID\)

Restarts a specified agent with alive/up status.

If Agent Client Collector performance issues occur, you can restart the agent. Manual restart is supported in the following environments:

-   Linux-based agents using `systemd`
-   Windows agents

To get a list of agent IDs:

-   Run the getAgentsList\(\) method.
-   Check the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.
-   Run the [Agent Client Collector GET list](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#) REST API.

|Name|Type|Description|
|----|----|-----------|
|agentID|String|Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.|

|Type|Description|
|----|-----------|
|String|Error message if applicable, null otherwise.|

The following example shows how to restart an agent.

```
var agentsApi = new sn_agent.AccAgentsAPI();

var err = agentsApi.restartAgent("<agent_ID>");
if (!gs.nil(err))
	gs.error(err);
```

## AccAgentsAPI - runDiscovery\(String agentID\)

Runs a discovery check to locate CIs related to an agent. The specified agent must be in alive/up status.

To get a list of agent IDs:

-   Run the getAgentsList\(\) method.
-   Check the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.
-   Run the [Agent Client Collector GET list](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#) REST API.

|Name|Type|Description|
|----|----|-----------|
|agentID|String|Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.|

|Type|Description|
|----|-----------|
|String|Error message if applicable, null otherwise. For example, `Agent With ID: <agentID> Is Not Up: no thrown error`.|

The following example shows how to run discovery on an agent with alive/up status.

```
var agentsApi = new sn_agent.AccAgentsAPI();

var err = agentsApi.runDiscovery("<agent_ID>");

if (!gs.nil(err))
	gs.error(err);
```

## AccAgentsAPI - setDataCollectionStatus\(String agentID, Boolean status\)

Set the given data collection status \(true/false if enabled or not\) for a specified agent.

To get a list of agent IDs:

-   Run the getAgentsList\(\) method.
-   Check the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.
-   Run the [Agent Client Collector GET list](../../../../../integrate/inbound-rest/concept/agnt_clnt_cll-api.md#) REST API.

<table id="table_zk2_2g2_z4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

agentID

</td><td>

String

</td><td>

Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.

</td></tr><tr><td>

status

</td><td>

Boolean

</td><td>

Flag that indicates whether data collection is enabled for the agent.

 Valid values:

-   true: Enables data collection for this agent.
-   false: Disables data collection for this agent.

 Default: true

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Error message if applicable, null otherwise. For example, `Agent With ID: <agentID> Is Not Up: no thrown error`.|

The following example shows how to turn on agent data collection.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var err = agentsApi.setDataCollectionStatus("<agentID>", true);
if (!gs.nil(err))
   gs.error(err);
```

The following example shows how to turn off agent data collection.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var err = agentsApi.setDataCollectionStatus("<agentID>", false);
if (!gs.nil(err))
   gs.error(err);
```

## AccAgentsAPI - submitGrabLogRequest\(String agentId\)

Requests the log of a specified agent with alive/up status.

**Note:** To retrieve the log and check its progress, pass the request ID returned to the checkGrabLogRequestProgress\(\) method.

|Name|Type|Description|
|----|----|-----------|
|agentID|String|Unique ID of an agent listed in the Agent ID column of the Agent Client Collectors \[sn\_agent\_cmdb\_ci\_agent\] table.|

<table id="table_al2_2g2_z4b" class="returns"><thead><tr><th>

Properties

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;Object&gt;

</td><td>

JSON object containing the request ID and any error information.```
{
  "error": "String",
  "request_id": "String"
}
```

</td></tr><tr><td>

error

</td><td>

Error message. Null if there is no error.Data type: String

</td></tr><tr><td>

request\_id

</td><td>

Sys\_id of a request in the Agent Client Collector Requests \[sn\_agent\_request\] table. You can use this ID to get the status of the request using GET /agents/\{request\_id\}/.

 Data type: String

</td></tr></tbody>
</table>The following example shows how to get a log request ID.

```
var agentsApi = new sn_agent.AccAgentsAPI();
var submittedRequest = agentsApi.submitGrabLogRequest("<agentID>");

if (!gs.nil(submittedRequest.error))
   gs.error(submittedRequest.error);
else
   gs.info("Request ID: " + submittedRequest.request_id);
```

Output:

```
Request ID: <sys_id>
```

