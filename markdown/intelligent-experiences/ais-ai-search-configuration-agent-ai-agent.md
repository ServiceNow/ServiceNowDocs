---
title: AI Search Configuration AI agent
description: Responsible for managing the end-to-end process of formally configuring AI Search for ServiceNow internal tables. This agent is invoked whenever a user mentions ServiceNow internal tables in the context of AI Search.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ais-ai-search-configuration-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 2
breadcrumb: [AI Search AI agents, AI Search, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# AI Search Configuration AI agent

Responsible for managing the end-to-end process of formally configuring AI Search for ServiceNow internal tables. This agent is invoked whenever a user mentions ServiceNow internal tables in the context of AI Search.

## Workflow

The agent helps users complete tasks related to configuring AI Search.

1.  Greet user and help them set up filter conditions for their search.
2.  Gather information from user and validate.
3.  Create new search source.
4.  End flow.

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

Fetch internal sources configuration

Perform Create/update/delete operation on internal sources

Text to encoded query generation

-   **Generative AI skill**

Identify Search Profile based on user persona/experience

-   **Topic Block**

Table Details Analyzer


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

search\_application\_admin

</td></tr><tr><td>

Data access roles

</td><td>

agent\_role\_config\_admin, ais\_admin, approver\_user, catalog, localization\_requestor, one\_extend\_viewer, pa\_viewer, personalize\_dictionary, public, role\_viewer, search\_application\_admin, search\_relevancy\_model\_admin, sn\_ace.ace\_user, sn\_cd.content\_approver, sn\_cd.content\_manager, sn\_cd.content\_template\_owner, sn\_ce.analytics\_reader, sn\_esign.config\_manager, sn\_na\_analytics.admin, sn\_na\_analytics.viewer, sn\_nowassist\_admin.nsa\_admin, sn\_query\_gen.admin, sn\_query\_gen.user, taxonomy\_admin, ui\_action\_admin, user\_criteria\_admin, user\_criteria\_read

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
</table>Learn more about AI Search at [AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/overview-ais.md).

**Parent Topic:**[AI Search AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-search-ai-agents-overview.md)

