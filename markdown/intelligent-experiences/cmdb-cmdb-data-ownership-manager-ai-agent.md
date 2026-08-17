---
title: CMDB data ownership manager AI agent
description: Performs actions related to the data ownership of configuration item \(CI\) classes
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/cmdb-cmdb-data-ownership-manager-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [CMDB AI agents, CMDB, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# CMDB data ownership manager AI agent

Performs actions related to the data ownership of configuration item \(CI\) classes

## Workflow

The agent helps users complete tasks related to CMDB data ownership manager.

1.  If you have done it before, skip to step 2.
2.  Ask the user what CI class they would like to check the data ownership for.
3.  Determine the ownership field of the specified CI class.
4.  Ask the user whether the determined ownership field is correct.
5.  Evaluate the quality of the data ownership of the specified CI class.
6.  Ask the user if they want to check the data ownership of another CI class.
7.  Inform the user that they have completed the step of going through the data ownership of CIs.

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

Determine the ownership of a CI class

Evaluate the ownership quality of a CI class

Get similar CI Classes


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_cmdb\_admin, snc\_internal

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

