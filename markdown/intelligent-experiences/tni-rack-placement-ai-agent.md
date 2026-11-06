---
title: Rack placement AI agent
description: This AI agent finds a data center rack allocation that fits the capacity requirements of a change request. It validates the request, applies the placement policies for the data center, and records the outcome on the change request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/tni-rack-placement-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-10-27"
reading_time_minutes: 2
breadcrumb: [Telecommunications Network Inventory AI agents, Telecommunications, Media and Technology AI agents, Telecom, Media and Tech AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# Rack placement AI agent

This AI agent finds a data center rack allocation that fits the capacity requirements of a change request. It validates the request, applies the placement policies for the data center, and records the outcome on the change request.

## Workflow

The agent helps the user find racks that can accommodate the capacity requirements of a change request. It runs on its own, and the only question it asks is the one about existing affected CIs.

1.  Retrieve the change request. If it already has affected CIs, ask the user whether to continue with rack placement or finish without changes.
2.  Validate the capacity requirements in the change request.
3.  Retrieve the placement policies for the data center and its racks. This step always runs before the racks are found. If no policy exists for the data center, the agent continues with default values and does not ask the user for a policy.
4.  Find the racks that can accommodate the requirements.
5.  Show the user the structured request, the policy, the placement, any issues writing the results back, and a decision summary that explains why racks were chosen or excluded.
6.  Add a work note to the change request that says whether the allocation succeeded or failed and summarizes the outcome, and move the change request to Design Complete. This final step runs on every exit, including early exits.
7.  If any step fails, tell the user, and then record the failure in the final step. A placement that has issues writing the results back also counts as a failure.

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

finalize\_allocation

find\_rack\_placement

retrieve\_change\_request

retrieve\_policy

validate\_change\_request


</td></tr><tr><td>

Allowed user roles The specific user roles that can access this AI agent.

</td><td>

-   sn\_ni\_core.dc\_ops\_agent
-   sn\_ni\_core.inventory\_agent

</td></tr><tr><td>

Data access roles The specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   sn\_ni\_core.dc\_ops\_agent
-   sn\_ni\_core.inventory\_agent

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

[Racks Allocation Workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/servicenow-otto-agentic-workflows.md)

</td></tr></tbody>
</table>Learn more about Telecommunications Network Inventory at [Telecommunications Network Inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-network-inventory/telecom-network-inventory.md).

**Parent Topic:**[Telecommunications Network Inventory AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/tni-ai-agents-overview.md)

