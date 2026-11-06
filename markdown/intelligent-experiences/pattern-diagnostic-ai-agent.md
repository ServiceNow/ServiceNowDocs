---
title: Pattern Diagnostic AI agent
description: The Pattern Diagnostic Agent AI agent analyzes CMDB configuration item \(CI\) data quality by using Discovery pattern metadata. The agent identifies CIs with missing attribute values, parses discovery logs to diagnose the failures, and prepares the error data for remediation through the Error Framework.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/pattern-diagnostic-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-06"
reading_time_minutes: 2
breadcrumb: [IT Operations Management AI agents, IT Operations Management, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Pattern Diagnostic AI agent

The Pattern Diagnostic Agent AI agent analyzes CMDB configuration item \(CI\) data quality by using Discovery pattern metadata. The agent identifies CIs with missing attribute values, parses discovery logs to diagnose the failures, and prepares the error data for remediation through the Error Framework.

## Workflow

The agent helps the user find out why Discovery didn't populate an attribute on recently discovered CIs of a specific CI class.

1.  Identify the CI class and the attribute to investigate, suggesting matching CI classes and the attributes that Discovery patterns populate if the user doesn't specify them.
2.  Check the Discovery pattern metadata to confirm that Discovery is responsible for populating the attribute, and inform the user if the attribute requires manual entry or an external integration instead.
3.  Find the CIs discovered by ServiceNow in the last 30 days that are missing a value for the attribute, and report whether any affected CIs exist.
4.  Resolve the managed IP addresses for the affected CIs and search the discovery logs for errors, warnings, and diagnostic messages that explain the missing data.
5.  Classify the primary error from the discovery logs and log it to the Error Framework when a matching error code is found.
6.  Present an investigation summary that covers the Discovery pattern responsible for the attribute, the affected CIs, and the likely root cause, with links to the CI records and discovery logs.
7.  Ask the user whether they want to investigate a different attribute or CI class.

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

DQA Discovery Log Parser

DQA Error Classifier

DQA ManagedIP Resolver

DQA Missing Data Detector

DQA Pattern Lookup

Resolve CI Class


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

discovery\_admin

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

discovery\_admin

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

Pattern Diagnostic Workflow

</td></tr></tbody>
</table>**Parent Topic:**[IT Operations Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/itom-ai-agents-overview.md)

