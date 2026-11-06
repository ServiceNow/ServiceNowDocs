---
title: Properties, tables, and roles installed with Build Agent
description: System properties installed with Build Agent control operational settings and resource limits. Tables store conversation, message, checkpoint, and telemetry data. Roles define access control for properties and features.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/ba-properties-installed-with.html
release: australia
topic_type: reference
last_updated: "2026-11-02"
reading_time_minutes: 4
keywords: [system properties, tables, roles, access control, ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Configure, Build Agent, Build, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Properties, tables, and roles installed with Build Agent

System properties installed with Build Agent control operational settings and resource limits. Tables store conversation, message, checkpoint, and telemetry data. Roles define access control for properties and features.

## System properties

To access these properties, enter `sys_properties.list` in the navigation filter to open the System Properties \[sys\_properties\] table. All properties are in the Build Agent \(Trial\) scope.

|Property|Type|Default|Read role|Write role|Description|
|--------|----|-------|---------|----------|-----------|
|**sn\_build\_agent.tool.execution.timeouts**|String \(JSON\)|`{"run_query": 120000, "get_knowledge_source": 120000, "create_new_servicenow_app": 300000, "default": 240000}`|sn\_glider.admin|sn\_glider.admin|Sets the maximum execution time \(in milliseconds\) for each tool.|

These properties can be read by admin but not written.

|Property|Type|Default|Read role|Write role|Description|
|--------|----|-------|---------|----------|-----------|
|**sn\_build\_agent.prompt\_limit\_period\_days**|Integer|30|admin|None|Rolling window period \(in days\) used in prompt-limit calculations.|
|**sn\_build\_agent.user\_prompt\_limit**|Integer|100|admin|None|Maximum prompts per user per rolling window in production environments.|
|**sn\_build\_agent.user\_prompt\_limit\_pdi**|Integer|25|admin|None|Maximum prompts per user per rolling window in non-production instances.|
|**sn\_build\_agent.tier\_override**|String|None|admin|None|Overrides the Build Agent tier. Valid options: `free` or `paid`. Setting `paid` requires the `sn_build_agent_pro` scope to be installed. No entitlement check is performed through `sn_now_creator`.|

|Property|Type|Default|Read role|Write role|Description|
|--------|----|-------|---------|----------|-----------|
|**sn\_build\_agent.keyword\_search.default\_limit**|Integer|10|sn\_glider.admin|sn\_glider.admin|Default number of results returned by keyword search when the client omits the limit parameter.|
|**sn\_build\_agent.keyword\_search.max\_field\_length**|Integer|2000|sn\_glider.admin|sn\_glider.admin|Default maximum characters per content field when **contentMode** is `truncate`. Clients can override this with the **maxFieldLength** request parameter.|

|Property|Type|Default|Read role|Write role|Description|
|--------|----|-------|---------|----------|-----------|
|**sn\_build\_agent.instruction.dispatch\_enabled**|Boolean|true|sn\_glider.admin|sn\_glider.admin|When false, dispatched \(non-interactive\) work item runs skip loading instance and user skills and rules.|
|**sn\_build\_agent.instruction.rule.active\_limit**|Integer|5|sn\_glider.admin|sn\_glider.admin|Maximum number of active rule instructions per applies-to bucket.|
|**sn\_build\_agent.instruction.skill.active\_limit**|Integer|50|sn\_glider.admin|sn\_glider.admin|Maximum number of active skill instructions per applies-to bucket.|

|Property|Type|Default|Read role|Write role|Description|
|--------|----|-------|---------|----------|-----------|
|**sn\_build\_agent.script\_execution\_enabled**|Boolean|true|sn\_glider.admin|sn\_glider.admin|Per-instance switch for the `run_script` tool. Set to false to withdraw the script\_execution capability on this instance, which stops the tool being offered to the agent. Withdraw-only: a production instance does not expose the capability, regardless of this setting.|

|Property|Type|Default|Read role|Write role|Description|
|--------|----|-------|---------|----------|-----------|
|**sn\_build\_agent.implementation\_job\_monitor.enabled**|Boolean|true|sn\_glider.admin|sn\_glider.admin|Main kill switch for the Implementation Jobs Monitor scheduled job. Set to false to stop all monitor activity without disabling the scheduled trigger.|
|**sn\_build\_agent.implementation\_job\_monitor.max\_per\_run**|Integer|50|sn\_glider.admin|sn\_glider.admin|Maximum number of in-progress work items the watchdog scans and interrupts in a single run. Caps script execution time. Remaining candidates are caught on the next run.|
|**sn\_build\_agent.implementation\_job\_monitor.stall\_threshold\_sec**|Integer|900|sn\_glider.admin|sn\_glider.admin|Seconds a work item's newest run conversation can go without a new message before the watchdog interrupts it \(moves it to `needs_attention`\). A conversation that never received a message is measured from when its run was dispatched.|

## Main tables

The following table lists tables in the `sn_build_agent` scope. The access shown is for sn\_glider.admin. Descriptions are inferred from table and field names. Conversation, message, and checkpoint tables are controlled by scripts and are not listed here.

|Table|What it stores|Access for sn\_glider.admin|
|-----|--------------|---------------------------|
|Build Agent Activity \[sn\_build\_agent\_activity\]|Units of work the agent performs in a conversation, with outcome and retry state|Read, update, create, delete|
|Build Agent Plan \[sn\_build\_agent\_plan\]|Plans the agent drafts for a request, with state and order|Read, update, create, delete|
|Build Agent Work Item Dependency \[sn\_build\_agent\_work\_item\_dependency\]|Links between work items that set the order of work|Read, update, create, delete|
|Build Agent ATF Test \[sn\_build\_agent\_atf\_test\]|Automated Test Framework results for an activity|Read, update, create, delete|
|Build Agent Conversation Change Log \[sn\_build\_agent\_conversation\_change\_log\]|Files and records the agent changed in a conversation|Read, update, create, delete|
|Build Agent IDE File Mount \[sn\_build\_agent\_ide\_file\_mount\]|Mapping of conversations to IDE file locations|Read, create, delete|
|Build Agent Script Request \[sn\_build\_agent\_script\_request\]|Requests for the agent to run a script, with execution history|Read, update, create, delete|
|Build Agent Instruction \[sn\_build\_agent\_instruction\]|Admin-defined instructions the agent follows|Read, update, create, delete|
|Build Agent Skill \[sn\_build\_agent\_skill\]|Skills the agent can use|Read, update, create, delete|
|Build Agent Skill Resource \[sn\_build\_agent\_skill\_resource\]|Supporting files attached to skills|Read, update, create, delete|
|Build Agent User Instruction \[sn\_build\_agent\_user\_instruction\]|Personal instructions users give the agent|Read, update, create, delete|
|Event telemetry \[sn\_build\_agent\_event\_telemetry\]|Usage metrics for individual agent events|Read, update, delete|
|Task telemetry \[sn\_build\_agent\_task\_telemetry\]|Usage metrics per agent task|Read, update, delete|

## Access control \(ACLs\)

Build Agent \(Trial\) requires the sn\_glider.admin role for every feature, and there is no separate customer role. Some records are also limited to the user who created them.

|Access level|Meaning|Applies to|
|------------|-------|----------|
|Role only|Any user with sn\_glider.admin|Plans, work items, skills, instructions, script requests, file mounts, ATF test results, change logs, activity, task telemetry|
|Role and ownership|Role required, and the user must own the record|Conversations, messages, checkpoints|
|Hidden|Not visible to customers|Records marked internal, such as Build Agent background runs|

Points to know:

-   Users with the same role can't see each other's conversations or messages. This is intended.
-   Admin doesn't bypass ownership on conversations and messages. Even base admin must own the conversation to change it.
-   Most properties are read and write for the sn\_glider.admin role. The prompt-limit properties and **tier\_override** are read-only for admin, so customers can view them but not change them.

**Parent Topic:**[Build Agent configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/configure-build-agent.md)

