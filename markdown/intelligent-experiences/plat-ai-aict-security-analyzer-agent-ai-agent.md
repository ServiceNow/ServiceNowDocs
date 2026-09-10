---
title: AICT security analyzer AI agent
description: This AI agent generates context for a detected AI security event by aggregating asset, prompt, cross-threat, and correlation data. It then computes a confidence score from detection strength, event risk, and authorization signals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/plat-ai-aict-security-analyzer-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow AI Platform AI agents, ServiceNow AI Platform, AI agents library, AI assets, Enable AI experiences]
---

# AICT security analyzer AI agent

This AI agent generates context for a detected AI security event by aggregating asset, prompt, cross-threat, and correlation data. It then computes a confidence score from detection strength, event risk, and authorization signals.

## Workflow

For all threats, the agent deterministically executes outcomes in a single finalization step: creating a security incident for critical severity findings with no open duplicate, saving a triage record capturing the full verdict and rationale, and triggering an AI insight for platform-wide visibility after the triage record is committed.

1.  Retrieve the detected AI security event record and gather its full context, including the related asset, prompt, cross-threat indicators, and recent threat correlation.
2.  If the event context indicates an error, finalize the analysis immediately with the error details and stop.
3.  Calculate a confidence score using detection strength, event type risk, prompt authorization signals, and any cross-threat or correlation overrides.
4.  Finalize the analysis by determining severity and creating a security incident with no open duplicate. Save a triage record with the full rationale, and trigger an AI insight for platform-wide visibility.
5.  If finalization fails, present the error and its details to the user.

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

Assess Threat

Finalize Analysis


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

sn\_ai\_governance.ai\_steward

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

sn\_ai\_governance.ai\_steward

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[ServiceNow AI Platform AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-ai-agents-overview.md)

