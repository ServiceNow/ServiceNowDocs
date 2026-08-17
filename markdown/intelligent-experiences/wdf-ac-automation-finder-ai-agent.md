---
title: Automation finder AI agent
description: This Workflow Data Fabric agent fetches automation records from tables on your instance. The agent discovers relevant automations for a specified asset, estimates cost and time savings, saves the discovered automations, and presents a value insights summary to the user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wdf-ac-automation-finder-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric AI agents, Workflow Data Fabric AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Automation finder AI agent

This Workflow Data Fabric agent fetches automation records from tables on your instance. The agent discovers relevant automations for a specified asset, estimates cost and time savings, saves the discovered automations, and presents a value insights summary to the user.

## Workflow

1.  Pass the input JSON received from the data-collection agent to the automation discovery tool to find relevant automations.
2.  For the first few discovered automations, run the saving estimator tool to calculate time and cost savings per run, then append those estimates to each automation's record.
3.  Execute the discovered automations tool to persist the results and generate a summary.
4.  Display the output under the title **Value Insights**, without listing individual automations or inventing additional content.

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

Automation Discovery

-   **Topic**

Discovered Automations

-   **Generative AI skill**

Saving Estimator


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles

</td><td>

sn\_ac.automation\_technical\_user

</td></tr><tr><td>

Triggers

</td><td>

sn\_ac.automation\_technical\_user

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Automation Explorer

</td></tr></tbody>
</table>Learn more about Workflow Data Fabric at [Build an automation with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/build-automation-now-assist.md).

**Parent Topic:**[Workflow Data Fabric AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/wdf-ai-agents-overview.md)

