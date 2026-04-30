---
title: Now Assist AI agents reference
description: Find more information about user roles, tables, and the different properties that are installed in Now Assist AI agents.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-27"
reading_time_minutes: 8
breadcrumb: [Now Assist AI agents, Enable AI experiences]
---

# Now Assist AI agents reference

Find more information about user roles, tables, and the different properties that are installed in Now Assist AI agents.

## Now Assist AI agents roles

The following roles are installed with Now Assist AI agents with a compatible Now Assist application.

|Role|Description|
|----|-----------|
|AI Agent Admin \[sn\_aia.admin\]|Administrator of the application. A user with the sn\_aia\_admin role can create, read, update, and delete records.|
|AI Agent Viewer \[sn\_aia.viewer\]|Read-only access to the application. A user with the sn\_aia\_viewer role has read and report access on all tables.|
|agent\_role\_config\_admin|With this role, user can access and modify Agent role configurations with AI Agent Admin \[sn\_aia\_admin\] being the parent role.|
|agent\_role\_config\_viewer|Can view the Agent role configurations with AI Agent Viewer \[sn\_aia\_viewer\] being the parent role.|

## Now Assist AI agents system properties

The following are system properties that define default values and behavior.

<table id="table_byl_5rr_k2c"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aia.agent\_llm\_provider

</td><td>

Defines the \(large language model\) LLM service provider for AI agents.Default value: **azure\_openai**.

</td></tr><tr><td>

sn\_aia.agent\_tool\_supported\_data\_types

</td><td>

Defines a comma-separated list of supported data types for tools that are used by agents for IntegrationHub spoke. Each value corresponds to the name field of records in the Field classes table \[sys\_glide\_object\].

</td></tr><tr><td>

sn\_aia.analytics\_dashboard\_sysid

</td><td>

Provides the sys\_id for the AI Agents Analytics dashboard.read\_roles: sn\_aia.admin and sn\_aia.viewer

</td></tr><tr><td>

sn\_aia.continuous\_communicator\_output\_limit

</td><td>

Defines the maximum number of continuous outputs that the AI Agent Orchestrator can trigger to show to users. Default value: **3**

</td></tr><tr><td>

sn\_aia.continuous\_tool\_execution\_limit

</td><td>

Defines the maximum consecutive number of uses for the same tool. Default value: **7**

</td></tr><tr><td>

sn\_aia.enable\_usecase\_tool\_execution\_mode\_override

</td><td>

Enables running agentic workflows fully autonomously, overriding any non-automated tools in the agentic workflow. Default value: **false**

</td></tr><tr><td>

sn\_aia.ltm.category.auto\_create

</td><td>

Enables AI-generated categories if no matching categories exist. Default value: **false**

</td></tr><tr><td>

sn\_aia.ltm.enable\_long\_term\_memory

</td><td>

Enables long-term memory for AI agents. All previous user interactions are used as context for the LLM. Default value: **false**

</td></tr><tr><td>

sn\_aia.maximum\_agent\_tools

</td><td>

Defines the maximum number of tools that can be assigned to an AI agent. Default value: **20**

</td></tr><tr><td>

sn\_aia.max\_scheduled\_trigger\_query

</td><td>

Defines how many records are processed when a scheduled trigger is detected. Default value: **10**

 Write\_role: admin

</td></tr><tr><td>

sn\_aia.mid\_skill\_switch\_enabled

</td><td>

Enables mid-skill switching. Default value: **false**

</td></tr><tr><td>

sn\_aia.react\_failure\_retry\_max\_limit

</td><td>

Defines the maximum number of retries in case of an execution failure. Default value: **3**

</td></tr><tr><td>

sn\_nowassist\_va.router\_redirect\_va\_agentic

</td><td>

Determines AI agent discovery in Virtual Agent. If set to **NEVER**, Virtual Agent continues Q&amp;A without any agentic AI.Default: **ROUTER\_DECISION**

</td></tr><tr><td>

com.glide.cs.dynamic.capability.timeout

</td><td>

Defines the Timeout for AIA Proficiency Descriptor. Default value: **180**.

Write\_role: admin.

</td></tr><tr><td>

sn\_aia.enable\_follow\_up

</td><td>

Enables users to continue the conversation with follow-ups after the agentic workflow execution is complete.Default value: **true**.

</td></tr><tr><td>

sn\_aia.follow\_up\_message

</td><td>

Defines a follow-up message sent after execution is completed.Default Value: **How else can I help you?**

</td></tr><tr><td>

sn\_aia.allow\_context\_sharing

</td><td>

Enables the sharing of short-term memory, allowing context to persist across execution within the same conversation.Default Value: **true**

</td></tr><tr><td>

sn\_aia.agent\_strategy\_choice\_enabled

</td><td>

Enables to show the LLM reasoning strategy in the agent setup screen.Default Value: **false**

</td></tr><tr><td>

sn\_aia.context\_sharing\_strategy

</td><td>

This property defines the strategy to use for storing short-term memory for an execution.Default Value: **summarise**

</td></tr><tr><td>

sn\_aia.enable\_agent\_tool\_input\_value\_overrides

</td><td>

Enables you to override the agent tool input value.Default Value: **true**.

</td></tr><tr><td>

sn\_aia.follow\_up\_qna\_failure\_limit

</td><td>

Defines the limit to exit execution if the number of consecutive questions and answers aren’t available in the follow-up.Default value: **1**.

</td></tr><tr><td>

sn\_aia.ltm.use\_memory\_for\_ai\_agent

</td><td>

Enables long-term memory for AI agent interactions. When enabled, stored user memories are utilized in AI agent interactions.Default value: **true.**

</td></tr><tr><td>

sn\_aia.quick\_mode\_failure\_retry\_max\_limit

</td><td>

Defines maximum limit for retries in case of a failure in Quick Mode execution.Default value: **3**.

</td></tr><tr><td>

sn\_aia.user\_context\_data

</td><td>

Defines a comma-separated list of user context data to be used with AI Agents. The list is used to pick the data available from knowledge graph API: getUserContext.

List of available user information:

-   profile
-   manager
-   reportees
-   assets

The user information can also be customized by overriding the method getUserContext via UserContextUtil.

If customized, the property must define the comma separated list of keys generated by the customized getUserContext method.

Default value: **profile**.

</td></tr><tr><td>

sn\_aia.external\_agents.enabled

</td><td>

Set to `true` to enable external agent features

</td></tr><tr><td>

sn\_aia.external\_agents.parallel\_conversations.enabled

</td><td>

Enables or disables multiple simultaneous conversations per user

</td></tr><tr><td>

sn\_mcp\_client.cursor.max\_iterations

</td><td>

Specifies the maximum number of cursor-based pagination iterations to perform when fetching MCP tools. Helps prevent excessive looping or API calls during data retrieval.

**Note:** Set this value to 0 to disable pagination iteration limits.

</td></tr><tr><td>

mcp\_guardian\_check

</td><td>

Enables guardian check for MCP Client when the value is set to **true**.The default value is **false**.

**Note:** To enable guardian check for MCP Client, ensure that you enable Now Assist guardian on **AI Agent Studio** &gt; **Settings** page.

</td></tr><tr><td>

com.glide.agentic\_processes\_view.enabled

</td><td>

Enables the in-product experience for agentic workflows in the AI Workflows panel. Ensure that this is set to `true` if you plan on using UI actions to run agentic workflows.

</td></tr></tbody>
</table><table id="table_zsw_hkd_m3c"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_aia.enable\_episodic\_memory

</td><td>

Enables episodic memory. When enabled, episodic memories from past interactions are collected and stored in sn\_aia\_memory and utilized in future interactions to enhance the overall experienceDefault value: **true**.

.

</td></tr><tr><td>

sn\_aia.enable\_memory\_limit

</td><td>

Maximum number of episodic memories to inject into prompt when an agent is invoked. **Note:** The maximum number of values allowed is less than or equal to 5.

</td></tr><tr><td>

sn\_aia.use\_episodic\_memory\_for\_ai\_agent

</td><td>

Enables episodic memory injection for AI agent interactions. When enabled, stored user memories are utilized in AI agent interactions.Default value: **true**.

</td></tr></tbody>
</table>## Properties on the Agent Properties table

The following properties are on the Agent Properties \[sn\_aia\_property\] table. These properties affect different AI agent behaviors.

<table><thead><tr><th>

Name

</th><th>

Description

</th><th>

Default value

</th></tr></thead><tbody><tr><td>

alert.assist\_spike\_hours\_to\_check

</td><td>

Time interval, in hours, between running the scheduled job that checks for spikes in assist usage

</td><td>

3

</td></tr><tr><td>

alert.assist\_spike\_usage\_percentage\_threshold

</td><td>

Percentage increase required from previous job results to trigger the spike in assist usage notification

</td><td>

0.5 \(50%\)

</td></tr><tr><td>

alert.assist\_spike\_usage\_threshold

</td><td>

Minimum number of assists to trigger the spike in assist usage notification

</td><td>

5000

</td></tr><tr><td>

alert.consecutive\_error\_count

</td><td>

Consecutive number of latency errors to trigger the latency notification

</td><td>

3

</td></tr><tr><td>

alert.llm\_latency\_threshold

</td><td>

Time taken, in seconds, for the LLM to respond before sending a latency error

</td><td>

10

</td></tr><tr><td>

alert.tool\_latency\_threshold

</td><td>

Time taken, in seconds, for a tool to finish executing before sending a latency error

</td><td>

300

</td></tr><tr><td>

enable\_agent\_tool\_input\_value\_overrides

</td><td>

Determines whether tool input values can be overriden by the AI agent or other tools for use by another tool

</td><td>

false

</td></tr><tr><td>

execution\_task.latency\_thresholds

</td><td>

Determines thresholds on LLM and tool execution times and response tokens/character counts for tool calling

</td><td>

```
{
  "llm": {
    "timeBoundaries": [
      5000,
      10000
    ],
    "tokenLimit": 500
  },
  "tool": {
    "timeBoundaries": [
      200000,
      300000
    ],
    "outputCharLimit": 10000
  }
}
```

</td></tr><tr><td>

follow\_up\_behaviour

</td><td>

Actions to take by the agentic workflow after it has finished executing. Each record applies to only one agentic workflow.

</td><td>

no\_followup\_close\_conversation

</td></tr><tr><td>

mcp\_guardian\_check

</td><td>

Determines whether Now Assist Guardian runs on MCP tool executions

</td><td>

false

</td></tr><tr><td>

show\_citations

</td><td>

Determines whether agentic AI-generated responses in Now Assist panel or Now Assist in Virtual Agent add citations for their output

</td><td>

false

</td></tr></tbody>
</table>The following properties are used to detect and avoid infinite recursion or execution loops. If you reach the max executions that match the query within the time window, any new executions matching the query will abort. You can adjust these values if you want to lower the threshold for detecting recursion.

<table><tbody><tr><td>

recursive\_check.create\_max\_executions

</td><td>

Maximum number of matching executions creating records

</td><td>

50

</td></tr><tr><td>

recursive\_check.create\_time\_window

</td><td>

Time window, in minutes, for checking for matching executions creating records

</td><td>

15

</td></tr><tr><td>

recursive\_check.query\_for\_create\_record

</td><td>

Query for the fields of execution plans to create records to check if executions are repeating

</td><td>

objective=\{objective\}^agent=\{agent\}^ORusecase=\{usecase\}

</td></tr><tr><td>

recursive\_check.query\_for\_update\_record

</td><td>

Query for the fields of execution plans to update records to check if executions are repeating

</td><td>

related\_task\_record=\{related\_task\_record\}^objective=\{objective\}^agent=\{agent\}^ORusecase=\{usecase\}

</td></tr><tr><td>

recursive\_check.update\_max\_executions

</td><td>

Maximum number of matching executions updating a record

</td><td>

5

</td></tr><tr><td>

recursive\_check.update\_time\_window

</td><td>

Time window, in minutes, for checking for matching execution updates

</td><td>

15

</td></tr></tbody>
</table>## Now Assist AI agents tables installed

The following tables are installed so Now Assist AI agents works as expected:

<table id="table_trq_gvx_k2c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Agentic workflows \[sn\_aia\_usecase\]

</td><td>

List of configured agentic workflows.

</td></tr><tr><td>

AI Agents \[sn\_aia\_agent\]

</td><td>

List of configured AI agents.

</td></tr><tr><td>

Tools \[sn\_aia\_tool\]

</td><td>

List of tools used by an AI agent.

</td></tr><tr><td>

Strategies \[sn\_aia\_strategy\]

</td><td>

List of strategies used by an AI agent.

</td></tr><tr><td>

Teams \[sn\_aia\_team\]

</td><td>

Team that is a group of listed agents.

</td></tr><tr><td>

Team members \[sn\_aia\_team\_member\]

</td><td>

List of teams mapped to an agent.

</td></tr><tr><td>

AIA Trigger Configurations \[sn\_aia\_trigger\_configuration\]

</td><td>

List of triggers created for an agentic workflow.

</td></tr><tr><td>

Execution Tasks \[sn\_aia\_execution\_task\]

</td><td>

List of tasks by execution plan ID.

</td></tr><tr><td>

Messages \[/sn\_aia\_message\]

</td><td>

List of messages recorded in AI agent conversations to and from the human users.

</td></tr><tr><td>

Tools Executions \[sn\_aia\_tools\_execution\]

</td><td>

List of tools executed by the plan ID.**Note:** The records in the Tools Executions table expire and become unavailable after a period of 13 months.

</td></tr><tr><td>

Execution Plans \[sn\_aia\_execution\_plan\]

</td><td>

List of plan executions by conversation ID.

</td></tr><tr><td>

Agent Tools \[sn\_aia\_agent\_tool\_m2m\]

</td><td>

List of tools and maximum automatic executions.

</td></tr><tr><td>

AI Agent configs \[sn\_aia\_agent\_config\]

</td><td>

List of active AI agents configured for the proficiency that they’ll be used in.

</td></tr><tr><td>

Agent properties \[sn\_aia\_property\]

</td><td>

Various properties that affect AI agent behavior.

</td></tr><tr><td>

Gen AI Metadata M2M \[sn\_aia\_gen\_ai\_m2m\]

</td><td>

List of Gen AI metadata and the maximum automatic executions.Maintains the mapping between sn\_aia\_execution\_task and Gen AI log metadata. If two large language model \(LLM\) calls are made to the sn\_aia\_execution\_task, then the sn\_aia\_gen\_ai\_m2m table has two records.

</td></tr><tr><td>

Report metrics \[sn\_aia\_report\_metric\]

</td><td>

List of the report metrics.

</td></tr><tr><td>

Agent Access Role Configurations \[sys\_agent\_access\_role\_configuration\]

</td><td>

List of agent access roles. You can also create agent access roles from this table.

</td></tr><tr><td>

AI Agent Memory \[sn\_aia\_memory\]

</td><td>

Stores individual facts tied to users and memory categories.

</td></tr><tr><td>

AI Agent Memory Categories \[sn\_aia\_ltm\_category\]

</td><td>

Defines what types of information can be remembered.

</td></tr><tr><td>

AI Agent Category Mappings \[sn\_aia\_ltm\_category\_mapping\]

</td><td>

Controls which agents have access to specific memories.

</td></tr></tbody>
</table>|Table|Description|
|-----|-----------|
|GAF record group \[sn\_gaf\_record\_group\]|Stores the output of the grouping skill. Each record represents a cluster of related records. You can open each record group record to discover which records were included within the cluster.|
|GAF record group detail \[sn\_gaf\_record\_group\_detail\]|Contains the individual records that belong to each group GAF record group. You can also find if a record is marked to act as a representative of the cluster on these records.|
|GAF action strategy result \[sn\_gaf\_action\_strategy\_result\]|Holds the results of the Action Strategy skill, which selects representative records from each group for downstream processing.|
|GAF action mapper results \[sn\_gaf\_action\_mapper\_result\]|Stores the output of the Mapper skill, which maps new records to existing clusters.|
|GAF action reducer results \[sn\_gaf\_action\_reducer\_result\]|Stores the result of the Action Reducer skill. The results include insights for entire clusters. For example, how to resolve incidents similar to those gathered in a cluster.|

