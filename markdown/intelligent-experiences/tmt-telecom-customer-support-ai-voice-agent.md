---
title: Telecom customer support AI voice agent
description: The AI voice agent helps a consumer troubleshoot a broadband service issue over the phone. It validates the caller, finds their active services, and walks them through the troubleshooting steps from a knowledge article one step at a time. It can also check the contract termination status.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-telecom-customer-support-ai-voice-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-22"
reading_time_minutes: 2
breadcrumb: [Customer Service Problem Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Telecom customer support AI voice agent

The AI voice agent helps a consumer troubleshoot a broadband service issue over the phone. It validates the caller, finds their active services, and walks them through the troubleshooting steps from a knowledge article one step at a time. It can also check the contract termination status.

## Workflow

The agent helps the caller troubleshoot a broadband service issue and, if they ask, moves them on to cancellation or to a live agent.

1.  Greet the caller and confirm that they want to troubleshoot their broadband service.
2.  Capture the product offering name and the service location when the caller mentions them.
3.  Validate the caller as a consumer in the system, and ask them to contact support when the validation fails.
4.  Retrieve the active services at the caller's location, and offer to check a different location when none are found.
5.  Confirm to the caller that no known outages affect their service.
6.  Ask the caller what the issue is and find a knowledge article with matching troubleshooting steps.
7.  Present one troubleshooting step at a time and ask the caller to confirm whether it resolved the issue before moving to the next step.
8.  Check the contract termination status or transfer the call to a live agent, only when the caller asks to cancel the service or to speak to an agent.

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

CheckContractTermination

Get relevant knowledge articles for troubleshooting

Validate Consumer

fetchProductInventory


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

Not defined.

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_customerservice.consumer

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure a voice assistant using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>Learn more about Customer Service Problem Management at [Customer Service Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/cspm-landing-page.md).

**Parent Topic:**[Customer Service Problem Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cspm-ai-agents-overview.md)

