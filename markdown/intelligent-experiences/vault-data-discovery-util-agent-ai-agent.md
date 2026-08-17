---
title: Data Discovery util AI agent
description: This ServiceNow Vault agent assists data stewards in scheduling and managing data discovery jobs by verifying required roles, entitlements, and subscriptions. The agent categorizes discovered data patterns into compliance groups to support regulatory and security requirements. It also help user to add tags to data patterns on demand.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-data-discovery-util-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [ServiceNow Vault AI agents, ServiceNow Vault AI agents, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# Data Discovery util AI agent

This ServiceNow Vault agent assists data stewards in scheduling and managing data discovery jobs by verifying required roles, entitlements, and subscriptions. The agent categorizes discovered data patterns into compliance groups to support regulatory and security requirements. It also help user to add tags to data patterns on demand.

## Workflow

1.  Check the user's permissions. Stop if role or entitlement is missing, and note the subscription status either way.
2.  Verify no active discovery job conflicts with the requested one. Stop if conflicts exist.
3.  Fetch all available data patterns and check which ones already have tags assigned, displaying them grouped by tag.
4.  For patterns without tags, use the discovery grouping skill to recommend classifications across sensitive data categories.
5.  Show tagged patterns first, then untagged patterns with their recommended categories.
6.  Prompt the user to add patterns to existing categories, create custom categories, and assign patterns across multiple categories.
7.  Offer to tag patterns so they're easier to find and assign in future discovery policies. Create tags as needed and associate patterns to them one by one.

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

Check if tag is available

Create data pattern record tag

Create label entry for data patterns

Data Discovery AI services validation script

Data Discovery conflicting job validation script

Data Discovery entitlement validation script

Data Discovery role validation script

Get available data pattern tags

Get available data patterns

-   **Generative AI skills**

Discovery data pattern grouping skill


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_data\_discovery.data\_discovery\_admin

</td></tr><tr><td>

Data access roles

</td><td>

sn\_data\_discovery.data\_discovery\_admin

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

Data discovery job scheduler workflow

</td></tr></tbody>
</table>Learn more about ServiceNow Vault at [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md).

**Parent Topic:**[ServiceNow Vault AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/vault-ai-agents-overview.md)

