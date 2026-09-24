---
title: AI Search XCC AI agent
description: This agent assists you with setting up the ServiceNow AI Platform External Content Connectors \(XCC\) application to make content from external repositories searchable in AI Search applications. It helps you set up external content connectors for private source systems like Google Drive or Microsoft SharePoint Online, and public web content sources like Apple Support, Okta, or Zoom.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/xcc-ai-search-xcc-agent-ai-agent.html
release: brazil
topic_type: reference
last_updated: "2026-09-21"
reading_time_minutes: 3
breadcrumb: [External Content Connector AI agents, External Content Connectors, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# AI Search XCC AI agent

This agent assists you with setting up the ServiceNow AI Platform® External Content Connectors \(XCC\) application to make content from external repositories searchable in AI Search applications. It helps you set up external content connectors for private source systems like Google Drive or Microsoft SharePoint Online, and public web content sources like Apple Support, Okta, or Zoom.

## Workflow

The agent helps you complete tasks related to the External Content Connectors application. It guides you through connector selection, authentication, user mapping, content scope, crawl scheduling, and search profile linking. The agent also interprets your intent for new setup, updates, or troubleshooting, and it handles credentials securely and validates parameters.

The agent can perform the following tasks:

1.  Parse your request to determine your intent \(create a new external content connector or update an existing one\). Match your request to an available external content connector type \(Atlassian Confluence Cloud, Box, Google Drive, Microsoft OneDrive, and Microsoft SharePoint Online\). If no available connector type matches, offer to set up a custom Webcrawler connector.
2.  If configured instances of the specified external content connector type already exist, prompt you to choose one to update. If no instances of that external content connector type exist, create a new external content connector of that type.
3.  Collect and validate credentials for the external content connector through a secure form. \(For external content connectors that crawl public content, the agent skips this step.\)
4.  For external content connectors that support permission-based search, preserve permissions for source system users by mapping them to ServiceNow AI Platform users.
5.  Prompt you to choose which locations \(sites, pages, and so on\) to include or exclude when crawling content from the source system. If applicable, also prompt you to choose which retrieved file or attachment types to index for search.
6.  Prompt you to choose a one-time or recurring content crawl, along with crawl frequency, day, time, and time zone. \(External content connectors that crawl public content are limited to one-time crawls.\)
7.  Present a full configuration summary and require explicit confirmation before proceeding.
8.  Save the external content connector configuration and start the content crawl job, then display the results and links to the created records.
9.  Show which search profiles the external content connector's data source is already linked to. Enable you to link the data source to another search profile or unlink it from one.

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

When enabled, all previous user interactions are used as context for the LLM. This value is off \(false\) by default. This setting is defined by the **sn\_aia.ltm.enable\_long\_term\_memory** system property. For more information, see [ServiceNow Otto AI agents reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/na-aia-reference.md).

</td></tr><tr><td>

Tools

</td><td>

-   **Conversational topics**

Connectors permission and credentials

-   **Generative AI skills**

Identify Search Profile

-   **Scripts**
    -   Fetch AI Search Configurations
    -   Fetch connector info along with all the step details
    -   Fetch Available Connectors
    -   Initiate Crawl
    -   Perform AI Search Config Operation

</td></tr><tr><td>

Allowed user rolesThe specific user roles that can access this AI agent.

</td><td>

sn\_ext\_conn.xcc\_admin

</td></tr><tr><td>

Data access rolesThe specific user identity roles that determine which data the AI agent can access and what actions it can take.

</td><td>

-   agent\_admin
-   agent\_security\_admin
-   ais\_admin
-   api\_analytics\_read
-   connection\_admin
-   cors\_rule\_admin
-   credential\_admin
-   decision\_table\_reader
-   df\_data\_steward
-   export\_rest\_api
-   external\_app\_install\_admin
-   fd\_read
-   fd\_read\_actions
-   fd\_read\_flows
-   fd\_read\_operations
-   fd\_read\_operations\_all
-   flow\_designer
-   flow\_operator
-   flow\_write\_enabled
-   graphql\_schema\_admin
-   metadata\_scope\_viewer
-   now.assist.creator
-   now.assist.creator.analytics
-   oauth\_admin
-   openapi\_admin
-   pa\_viewer
-   rest\_api\_builder
-   rest\_api\_explorer
-   search\_application\_admin
-   search\_relevancy\_model\_admin
-   sn\_ace.ace\_user
-   sn\_conv\_fa.conv\_fa\_designer
-   sn\_diagram\_builder.db\_read
-   sn\_ext\_conn.xcc\_admin
-   sn\_ext\_conn.xcc\_reader
-   sn\_kmf.cryptographic\_manager
-   sn\_mcp\_client.viewer
-   sn\_query\_gen.user
-   sn\_udc.basic\_read
-   sn\_workflow\_studio.workflow\_studio\_read
-   trigger\_designer
-   trigger\_designer\_read
-   view\_changer
-   wdf\_consumer
-   wdf\_operator
-   web\_service\_admin
-   workflow\_ai\_author

</td></tr><tr><td>

Triggers

</td><td>

Optional. None defined by default. An admin can specify triggers if desired. For more information, see [Add a trigger to an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/add-trigger-aia.md).

</td></tr><tr><td>

Channels

</td><td>

Configure an assistant for Virtual Agent or ServiceNow Otto panel using [Assistant Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-now-assist-va.md).

</td></tr><tr><td>

Used in agentic workflows

</td><td>

Not applicable.

</td></tr></tbody>
</table>To learn more about the External Content Connectors application, see [External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ext-cont-connectors-landing-page.md).

**Parent Topic:**[External Content Connector AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/xcc-ai-agents-overview.md)

