---
title: Product adoption roadmap AI agent
description: The agent creates a product adoption roadmap for a customer. It analyzes the engagement and similar engagements, creates the roadmap, and arranges lanes and items to match the customer's goals.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tmt-product-adoption-roadmap-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Customer Success Management AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Product adoption roadmap AI agent

The agent creates a product adoption roadmap for a customer. It analyzes the engagement and similar engagements, creates the roadmap, and arranges lanes and items to match the customer's goals.

## Workflow

The agent creates a product adoption roadmap for an engagement without asking the user for inputs.

1.  Collect the engagement details, including the sold products and other customer success information, and analyze them.
2.  Identify similar engagements. If none exist, skip to creating the roadmap.
3.  Collect data for the similar engagements and select the one that best matches the provided engagement.
4.  Look up the roadmaps of the selected engagement and select the one that best matches the requested roadmap name and description.
5.  Create the product adoption roadmap, using the similar roadmap as a reference when one is found.
6.  Rearrange the lanes and items so that they reflect the customer's goals, timeline, and product usage, and update the roadmap.
7.  Display a link to the roadmap and a short summary of the rearrangements.
8.  Ask whether the user has questions about the arrangement, then end the session.

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

-   **Capability**

Identify similar engagements

-   **Script**

Collect contextual data for provided engagement

Collect contextual data for similar engagements

Create product adoption roadmap entities

Look up product adoption roadmap details

Perform scripted update on roadmap entities

Retrieve created product adoption roadmap link


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

Product adoption roadmap agentic workflow

</td></tr></tbody>
</table>Learn more about Customer Success Management at [Customer Success Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-events-landing.md).

**Parent Topic:**[Customer Success Management AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/customer-success-ai-agents-overview.md)

