---
title: Procurement product recommendation AI agent
description: This Sourcing and Procurement Operations agent can browse the catalog and create orders. The agent matches user requirements against available items, then routes to submission forms based on vendor status and dollar thresholds. Accepts and processes uploaded quote documents or SOW \(Statement of Work\) files to extract line items and pricing.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/spo-procurement-product-recommendation-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [Sourcing and Procurement Operations AI agents, Sourcing and Procurement Operations, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Procurement product recommendation AI agent

This Sourcing and Procurement Operations agent can browse the catalog and create orders. The agent matches user requirements against available items, then routes to submission forms based on vendor status and dollar thresholds. Accepts and processes uploaded quote documents or SOW \(Statement of Work\) files to extract line items and pricing.

## Workflow

1.  Create a purchase request from the quote or statement of work was uploaded by the user.
2.  Run recommendations for all requested products, then present them one product at a time as selectable options. Collect a selection or skip for each product before moving on.
3.  Assemble the selected products with any available details and run the channel decision tool, which determines whether the request routes to purchasing or sourcing. Render an HTML plan for the user.
4.  If the plan flags missing fields, ask the user to provide them, re-run the plan tool, and repeat until nothing is missing.
5.  Present the plan and ask the user to submit or edit. Edits are applied by re-running the plan tool with the updates, then re-presenting the plan.
6.  Ask about attachments, then submit via either the purchasing or sourcing tool based on whether the selected products have product IDs.

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

-   **Conversational topics**

Add or update attachment

Quote or sow attachment

-   **Script**

Channel decision and plan creation

Create a document task

Create purchasing record

Create sourcing record

Created record from document

Document type extractor

Recommendation

Show more results


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_spend\_gen\_ai.now\_assist\_requester

</td></tr><tr><td>

Data access roles

</td><td>

sn\_spend\_gen\_ai.now\_assist\_requester, sn\_shop.shopper

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

Help fulfill procurement requests

</td></tr></tbody>
</table>Learn more about Sourcing and Procurement Operations at [Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/psm-overview.md).

**Parent Topic:**[Sourcing and Procurement Operations AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/spo-ai-agents-overview.md)

