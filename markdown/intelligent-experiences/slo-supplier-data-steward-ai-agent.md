---
title: Supplier data steward AI agent
description: This Supplier Lifecycle Operations agent manages supplier onboarding by verifying supplier details, handling duplicate detection, allowing corrections to supplier name or email, and creating the supplier record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/slo-supplier-data-steward-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Supplier Lifecycle Operations AI agents, Supplier Lifecycle Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Supplier data steward AI agent

This Supplier Lifecycle Operations agent manages supplier onboarding by verifying supplier details, handling duplicate detection, allowing corrections to supplier name or email, and creating the supplier record.

## Workflow

1.  Based on the case state, prompt the user for a case number \(if details are needed\), proceed directly to record creation, or handle duplicates.
2.  Present the duplicate records to the user and ask whether to continue. If yes, offer the option to correct the supplier's legal name, email, or both before proceeding. If the correction resolves the duplicate, continue to onboarding. If the correction triggers a rejection, stop. If the user declines to continue, proceed with rejection.
3.  Run the verification and record creation tool using the supplier details and the user's continuation decision.
4.  Display one of four results: successful registration, halted by user decision, rejected due to validation failure, or rejected for other reasons.

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

Update supplier case details

-   **Subflow**

Verify and create records


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_slm.owner, sn\_supplier\_gen\_ai.now\_assist\_fulfiller

</td></tr><tr><td>

Data access roles

</td><td>

sn\_slm.owner, sn\_supplier\_gen\_ai.now\_assist\_fulfiller

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
</table>Learn more about Supplier Lifecycle Operations at [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supp-mgmt-landing-page.md).

**Parent Topic:**[Supplier Lifecycle Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/slo-ai-agents-overview.md)

