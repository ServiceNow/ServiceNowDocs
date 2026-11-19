---
title: Banking CSR customer insights AI agent
description: The AI agent answers a customer service representative's questions about a banking customer, presenting account, transaction, and case information in a clear, structured format so the representative can quickly explore relevant customer data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/fso-banking-csr-customer-insights-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-09-28"
reading_time_minutes: 2
breadcrumb: [Financial Services Operations AI Agents, Financial Services Operations, AI agents library, AI assets, Enable AI experiences]
---

# Banking CSR customer insights AI agent

The AI agent answers a customer service representative's questions about a banking customer, presenting account, transaction, and case information in a clear, structured format so the representative can quickly explore relevant customer data.

## Workflow

The AI agent helps the CSR explore a banking customer's account, transaction, and case information through natural-language questions.

1.  Load the default configuration for the customer insights session.
2.  Ask the CSR what they'd like to know about the customer, offering quick-prompt options alongside free-text entry.
3.  Look up the answer to each query using the customer's context and the banking domain.
4.  Present the results in a clear, per-topic summary using only the most relevant fields, and let the CSR know when nothing matches.
5.  Return to asking for the next question, continuing until the CSR ends the session.

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

-   **Scripts**

Fetch default configurations

-   **Subflows**

CSR query analyser


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_fso\_csr.business\_agent
-   sn\_fso\_csr.personal\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_fso\_csr.business\_agent
-   sn\_fso\_csr.personal\_agent

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

Not applicable.

</td></tr></tbody>
</table>**Parent Topic:**[Financial Services Operations AI Agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/fso-ai-agents-overview.md)

