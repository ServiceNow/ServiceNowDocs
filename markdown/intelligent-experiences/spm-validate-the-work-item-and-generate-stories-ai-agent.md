---
title: Validate the work item and generate stories AI agent
description: This Strategic Portfolio Management agent transforms Enterprise Agile Planning work items \(epics and features\) into a set of well-formed, actionable user stories. It evaluates work items to verify that it contains sufficient information, and guides users through a structured validation process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spm-validate-the-work-item-and-generate-stories-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Strategic Portfolio Management AI agents, Strategic Portfolio Management, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Validate the work item and generate stories AI agent

This Strategic Portfolio Management agent transforms Enterprise Agile Planning work items \(epics and features\) into a set of well-formed, actionable user stories. It evaluates work items to verify that it contains sufficient information, and guides users through a structured validation process.

## Workflow

1.  Collect the work item number, description, and any additional context as needed \(based on flags from the system\), confirming with the user before saving each piece of information.
2.  Produce user stories based on the validated work item and collected context.
3.  Display the generated stories and offer refinement options: discard stories, combine or split them, adjust personas or metrics, or add new ones.
4.  If the user chooses to refine, apply their changes, re-display the updated stories, and offer the same refine-or-save choice again. This loop continues until the user chooses to save.
5.  Save the finalized stories to the system and give the user a navigation link to view them.

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

-   **Scripts**

Refine Stories

Save stories

Validate and Generate Stories


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_apw\_advanced.eap\_user

</td></tr><tr><td>

Data access roles

</td><td>

sn\_apw\_advanced.eap\_user

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

Create stories

</td></tr></tbody>
</table>Learn more about Strategic Portfolio Management at [Strategic Portfolio Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/r_ITBusinessManagement.md).

**Parent Topic:**[Strategic Portfolio Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/spm-ai-agents-overview.md)

