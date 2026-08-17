---
title: Billing plan recommender AI agent
description: This Telecommunications, Media, and Technology \(TMT\) agent generates recommended service plans and updates the billing inquiry case work notes with the results. The agent helps to ensure a seamless recommendation process without requiring additional user input beyond initial confirmation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/tmt-billing-plan-recommender-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Billing plan recommender AI agent

This Telecommunications, Media, and Technology \(TMT\) agent generates recommended service plans and updates the billing inquiry case work notes with the results. The agent helps to ensure a seamless recommendation process without requiring additional user input beyond initial confirmation.

## Workflow

1.  Retrieve plan recommendations based on the high usage line item code \(not the case sold product code\).
2.  If no recommended plans are available, inform the user and stop.
3.  Write the recommended plan and summary to the billing inquiry case record as a numbered, line-by-line work note entry.

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

-   **Flow Action**

Generate Recommended Service Plans

-   **Script**

Update work notes of Billing Inquiry Case with the Recommended Plans


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_tmt\_agentic\_ai.telco\_billing\_inquiry\_case\_agent

</td></tr><tr><td>

Data access roles

</td><td>

sn\_tmt\_agentic\_ai.telco\_billing\_inquiry\_case\_agent

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

Help remediate bill issues

</td></tr></tbody>
</table>Learn more about Supplier Lifecycle Operations at [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supp-mgmt-landing-page.md).

**Parent Topic:**[Telecommunications, Media and Technology AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/tmt-ai-agents-overview.md)

