---
title: Playbook processing AI agent
description: This ServiceNow Otto for Creator agent is a general-purpose processing engine. The agent can receive diverse input types, determine the appropriate processing logic, and return structured, meaningful, and actionable outputs. The agent supports tasks such as summarization, transformation, classification, translation, data extraction, natural language understanding, and more.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/wfs-ply-playbook-processing-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Otto for Creator AI agents, ServiceNow Otto for Creator, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Playbook processing AI agent

This ServiceNow Otto for Creator agent is a general-purpose processing engine. The agent can receive diverse input types, determine the appropriate processing logic, and return structured, meaningful, and actionable outputs. The agent supports tasks such as summarization, transformation, classification, translation, data extraction, natural language understanding, and more.

## Workflow

1.  Determine what kind of data was provided \(plain text, JSON, code, tabular, etc.\) and infer the domain \(legal, medical, software, business, etc.\).
2.  If not explicitly stated, determine what the user wants done based on context.
3.  Choose and perform a single operation \(validation, summarization, classification, translation, extraction, transformation, computation, or reasoning/explanation\) rather than combining multiple unless explicitly instructed.
4.  Present the output concisely in Markdown or JSON with clear labels \(Input Type, Inferred Task, Result\). Provide detailed explanation only if requested.

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

Not defined.

</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

playbook.agent\_user

</td></tr><tr><td>

Data access roles

</td><td>

playbook.agent\_user

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
</table>Learn more about ServiceNow Otto for Creator at [ServiceNow Otto for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/now-assist-for-creator-landing.md).

**Parent Topic:**[ServiceNow Otto for Creator AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-creator-ai-agents-overview.md)

