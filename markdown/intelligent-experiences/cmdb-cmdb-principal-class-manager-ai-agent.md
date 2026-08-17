---
title: CMDB principal class manager AI agent
description: Performs actions related to principal configuration item \(CI\) classes
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cmdb-cmdb-principal-class-manager-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [CMDB AI agents, CMDB, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# CMDB principal class manager AI agent

Performs actions related to principal configuration item \(CI\) classes

## Workflow

The agent helps users complete tasks related to CMDB principal class manager.

1.  Check the CMDB governance access level for the current user.
2.  If you have done it before, skip to step 3.
3.  List all existing and potential principal CI classes.
4.  If the user does not have permission to mark principal classes, skip to step 7.
5.  Ask the user whether they want to mark a suggested CI class or unmark a current CI class from the list as principal.
6.  If the user specifies a class, mark or unmark the selected CI class as principal.
7.  Ask the user if they are done reviewing, or if they want to see details about a specific CI class.
8.  If the user has write access, inform the user that they have completed the step of managing principal CI classes.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Allow third party to access this AI agent

</td><td>

When enabled, third-party AI agents can use this agent. This value is off \(false\) by default. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the External discoverable field.

</td></tr><tr><td>

Allow AI specialists to access this AI agent

</td><td>

When enabled, AI specialists can use this agent. This value is off \(false\) by default. When set to true, more configuration options for tools become available so that an AI specialist can map inputs and response templates to tool outputs. This setting is defined in the AI Agent configs \[sn\_aia\_agent\_config\] table on the Specialist enabled field.

</td></tr><tr><td>

Manage long-term memory

</td><td>

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Get CMDB governance access level

Get similar CI Classes

Identify principal classes

Mark CI class as principal

Unmark CI class as principal


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

snc\_internal, sn\_cmdb\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_cmdb\_admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

CMDB Data Governance

</td></tr></tbody>
</table>Learn more about Configuration Management Database \(CMDB\) at [Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c_ITILConfigurationManagement.md).

**Parent Topic:**[CMDB AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/cmdb-ai-agents-overview.md)

