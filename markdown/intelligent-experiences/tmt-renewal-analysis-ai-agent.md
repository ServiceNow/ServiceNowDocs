---
title: Renewal analysis AI agent
description: The agent analyzes a renewal for a contract or engagement. It combines insight scores and value realization data into a renewal report and offers to create a renewal success play.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-renewal-analysis-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Customer Success Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Renewal analysis AI agent

The agent analyzes a renewal for a contract or engagement. It combines insight scores and value realization data into a renewal report and offers to create a renewal success play.

## Workflow

The agent helps the user analyze a renewal and start a follow-up play.

1.  Validate the renewal analysis configuration. Stop and tell the user if the configuration is not valid.
2.  Ask the user for a contract number or engagement number if the agent was not started from a record, and validate the number.
3.  Run the Success insights AI agent to populate score and trend data.
4.  Run the Value realization assessor AI agent to retrieve value realization data.
5.  Fetch the renewal analysis from both results and generate the renewal report.
6.  Display the follow-up options: do nothing, create a renewal success play, or start a Get to Green play.
7.  Start the play that the user selects and add the assessment to it.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Script**

Add Assessment to internal play

Fetch renewal analysis

Get the sysIDs

Populate the variables

Validate the configuration for renewal analysis

Validate the given Number

-   **Subflow**

Get to green play

Simple renewal play

-   **Topic**

Generate renewal report

Internal Sub-Flow Options


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_acct\_lc.customer\_success\_agent

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Support renewals and expansion agentic workflow

</td></tr></tbody>
</table>Learn more about Customer Success Management at [Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md).

**Parent Topic:**[Customer Success Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/customer-success-ai-agents-overview.md)

