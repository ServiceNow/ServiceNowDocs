---
title: AI Search XCC AI agent
description: This agent assists with AI Search External Content Connector \(XCC\) setup for private data sources \(SharePoint, Confluence, Google Drive, Box, OneDrive\) and public providers \(Zoom, Apple Support, Okta\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/xcc-ai-search-xcc-agent-ai-agent.html
release: australia
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 3
breadcrumb: [External Content Connector AI agents, External Content Connectors, Available AI agents on the ServiceNow AI Platform, AI assets, Enable AI experiences]
---

# AI Search XCC AI agent

This agent assists with AI Search External Content Connector \(XCC\) setup for private data sources \(SharePoint, Confluence, Google Drive, Box, OneDrive\) and public providers \(Zoom, Apple Support, Okta\).

## Workflow

The agent helps users complete tasks related to AI search XCC agent. The agent guides connector selection, authentication, content scope, crawl scheduling, and search profile mapping. It also interprets user intent for new setup, updates, or troubleshooting with secure credential handling and parameter validation.

1.  Parse the user's request to determine intent \(create vs. update\) and match it to an available connector \(SharePoint, Confluence, Google Drive, etc.\), or offer to set up a custom web crawler if nothing matches.
2.  If configurations already exist for that connector, let the user choose one to update; otherwise start a new instance.
3.  Collect and validate credentials for private connectors via a secure form; public connectors skip this step entirely.
4.  For connectors that support it, map source-system users to ServiceNow users for permission-based search.
5.  Choose which sites/pages to include or exclude, and \(for private connectors\) which file types to index.
6.  Choose a one-time or recurring crawl, along with frequency, day, time, and timezone \(public connectors are limited to one-time crawls\).
7.  Present a full configuration summary and require explicit confirmation before proceeding.
8.  Save the configuration and kick off the crawl job, then display the results and links to the created records.
9.  Show which AI Search profiles the data source is already linked to, and let the user add it to another profile or remove it from one.

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

Connectors permission and credentials

-   **Generative AI skills**

Identify Search Profile

-   **Scripts**

Fetch AI Search Configurations

Fetch connector info along with all the step details

Fetch Available Connectors

Initiate Crawl

Perform AI Search Config Operation


</td></tr><tr><td>

Agent roles \(ACLs\)

</td><td>

sn\_ext\_conn.xcc\_admin

</td></tr><tr><td>

Data access roles

</td><td>

agent\_admin, agent\_security\_admin, ais\_admin, api\_analytics\_read, connection\_admin, cors\_rule\_admin, credential\_admin, decision\_table\_reader, df\_data\_steward, export\_rest\_api, external\_app\_install\_admin, fd\_read, fd\_read\_actions, fd\_read\_flows, fd\_read\_operations, fd\_read\_operations\_all, flow\_designer, flow\_operator, flow\_write\_enabled, graphql\_schema\_admin, metadata\_scope\_viewer, now.assist.creator, now.assist.creator.analytics, oauth\_admin, openapi\_admin, pa\_viewer, rest\_api\_builder, rest\_api\_explorer, search\_application\_admin, search\_relevancy\_model\_admin, sn\_ace.ace\_user, sn\_conv\_fa.conv\_fa\_designer, sn\_diagram\_builder.db\_read, sn\_ext\_conn.xcc\_admin, sn\_ext\_conn.xcc\_reader, sn\_kmf.cryptographic\_manager, sn\_mcp\_client.viewer, sn\_query\_gen.user, sn\_udc.basic\_read, sn\_workflow\_studio.workflow\_studio\_read, trigger\_designer, trigger\_designer\_read, view\_changer, wdf\_consumer, wdf\_operator, web\_service\_admin, workflow\_ai\_author

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
</table>Learn more about [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ext-cont-connectors-landing-page.md) at .

**Parent Topic:**[External Content Connector AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/xcc-ai-agents-overview.md)

