---
title: AI voice agent reference
description: Reference information for AI voice agents.
locale: en-US
release: australia
topic_type: reference
last_updated: "2025-08-14"
reading_time_minutes: 3
breadcrumb: [Deploy AI voice agents, Now Assist AI agents, Enable AI experiences]
---

# AI voice agent reference

Reference information for AI voice agents.

## AI voice agent roles

The following table lists the roles installed with the Voice for Now Assist plugin.

|Roles|Description|
|-----|-----------|
|sn\_voice\_aia.admin|Provides access to agents configuration flow|
|sn\_voice\_aia.guest|Enables employees to use AI voice agents without authentication|
|sn\_voice\_aia.integration|Enables access to integrations such as Oracle|

## AI voice agent attributes

The AI voice agent attributes enable you to configure the authentication functionality for AI voice agents. Navigate to **All** &gt; **System Definition** &gt; **Tables** and search for Now Assist Deployment Config Attributes table to view the attributes.

The following table lists the attributes related to AI voice agent configuration.

|Attribute|Description|
|---------|-----------|
|voice\_max\_retries|The maximum number of retries allowed for successful authentication before the user account is locked. The default value is 3.|
|voice\_minutes\_account\_is\_locked|The number of minutes the user account is locked for, following maximum retries. The default value is 1440 minutes.|

## AI voice agent system properties

The following table consists of system properties to set up AI voice agents.

|Property|Description|
|--------|-----------|
|sn\_aia.enable\_voice\_agent\_setup|The system property to enable AI voice agents. Set the value of the property to true to enable AI voice agents on the instance.|

## Configuration for custom AI voice agent provider

The following table captures the required configurations on your instance to support AI voice agents. These configurations are required only if you’re creating a new messaging channel, provider channel, and provider channel identity for AI voice agents.

|Field|Value|
|-----|-----|
|Messaging channel|
|Type|Phone|
|Synchronous|True|
|Provider Channel|
|Provider attributes action|sn\_va\_as\_service.virtual\_agent\_\_bot\_to\_bot\_provider\_attributes|
|Sender subflow|sn\_va\_as\_service.virtual\_agent\_\_bot\_to\_bot\_contextual\_action|
|Contextual action|sn\_va\_as\_service.virtual\_agent\_\_bot\_to\_bot\_contextual\_action|
|Allow account linking|True|
|Account linking type|Verification question|
|Automatic link action|sn\_va\_as\_service.virtual\_agent\_\_bot\_to\_bot\_auto\_link\_account|
|Rich control mappings|
|Control type|DefaultAction|
|Outbound transformer action|sn\_va\_as\_service.virtual\_agent\_\_bot\_to\_bot\_action\_outbound\_transformer|
|Provider Channel Identity|
|Message auth|Name of the message authentication that you created as part of|
|Provider Identity properties|
|allow\_storing\_history\_in\_ongoing\_conversation|True|

## AI voice agent analytics indicators details

The following table maps the visualizations to the indicator sources and the calculation behind the metrics shown in the dashboard.

|Visualization|Indicator type|Calculation|Available breakdowns|Frequency|Unit|Precision|
|-------------|--------------|-----------|--------------------|---------|----|---------|
|Total voice conversations|Automated|Count of all voice calls|None|Daily|\#|0|
|Calls completed without a live agent|Automated|Count of voice calls where Agent chat=false|None|Daily|\#|0|
|Conversations transferred to a live agent|Automated|Count of voice calls where Agent chat=true|None|Daily|\#|0|
|Number of tickets created|Automated|Count of Interaction Related Records where Agent chat = false and Interaction Virtual agent = true and Interaction Type = Phone and Interaction AI Voice = true|None|Daily|\#|0|
|Conversations disconnected|Automated|Count of voice calls where State=Closed Abandoned|None|Daily|\#|0|
|Inferred customer satisfaction \(CSAT\): average score \(out of 5\)|sn\_na\_analytics\_insights table|Average of session CSAT|None|Daily|\#|1|
|Average voice conversation duration|Formula|\[\[AI Agent- Summed duration of calls\]\] / \[\[AI Agents- Total Calls\]\]|None|Daily|Minutes|0|
|Number of deflected conversations per AI agent|sn\_na\_analytics\_insights table|Count of voice calls where Resolved is Yes|None|Daily|\#|0|

## AI voice agent transcript and logs tables

The following tables contain details of the voice calls, from initiation and conversation details to agent actions and tool executions.

<table id="table_vxc_b2f_nhc"><thead><tr><th>

Table

</th><th>

Details

</th></tr></thead><tbody><tr><td>

sn\_aia\_execution\_plan

</td><td>

The sn\_aia\_execution\_plan table stores execution plans associated with voice calls. Each record in this table represents a single execution plan and contains detailed information about the interactions and actions that occurred during the call.

</td></tr><tr><td>

sn\_aia\_tools\_execution

</td><td>

The sn\_aia\_tools\_execution table logs information related to tool executions during a voice call. Each record represents a single tool execution and captures details about the agent, the tool used, and the outcome of that execution.

</td></tr><tr><td>

sys\_cs\_conversation

</td><td>

The sys\_cs\_conversation table stores the conversation record created at the start of a voice call. Its creation timestamp marks the beginning of the call. This table contains metadata and transcripts associated with the conversation, like state, device type, and transcripts from the call.**Note:** Personally Identifiable Information \(PII\) data is redacted from transcripts before it is stored.

</td></tr><tr><td>

Interactions

</td><td>

The Interactions table is similar to sys\_cs\_conversation and is created at the same time as the conversation record. It contains much of the same information related to the voice call.

</td></tr><tr><td>

sys\_generative\_ai\_log

</td><td>

The sys\_generative\_ai\_log table stores general-purpose logs for generative AI interactions during a voice call. If an agent uses an LLM \(Large Language Model\) during the call, this table records the relevant details such as prompt, response, and errors.

</td></tr></tbody>
</table>