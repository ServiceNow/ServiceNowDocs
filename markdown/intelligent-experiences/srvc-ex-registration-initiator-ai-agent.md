---
title: Registration initiator AI agent
description: This AI agent initiates the registration process and manages its early stages, including creating the registration record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/srvc-ex-registration-initiator-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Service Exchange AI agents, Service Exchange, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Registration initiator AI agent

This AI agent initiates the registration process and manages its early stages, including creating the registration record.

## Workflow

The agent helps initiate a new Service Exchange provider registration and manages its early stages.

1.  Verify the provider count and check for any outstanding health issues before proceeding.
2.  Collect and verify the provider's company, contact, and URL details.
3.  Create the provider and registration records once the details are verified.
4.  Run the Service Exchange Pre-Onboarding suite against the new registration.
5.  Check the registration state and report the result, including a link to any related issues, to the user.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Scripts**

Create issue link

Create provider

Create registration

Execute Service Exchange Pre-Onboarding suite

Get provider name company

Retrieve issues

Show resolve health dashboard message

Verify company contact url

Verify provider company

Verify provider count

Verify registration

Verify the Registration state


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_sb.admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_sb.admin

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Service Exchange Onboarding

</td></tr></tbody>
</table>**Parent Topic:**[Service Exchange AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/srvc-ex-ai-agents-overview.md)

