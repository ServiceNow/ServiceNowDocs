---
title: Available Enterprise MCP Registries
description: Pre-configured connection information for a set of high‑value MCP Servers are available as part of the Enterprise MCP Registry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/mcp-reg-enterprise.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: reference
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [ServiceNow MCP Registry, Connect, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Available Enterprise MCP Registries

Pre-configured connection information for a set of high‑value MCP Servers are available as part of the Enterprise MCP Registry.

The available MCP Servers are:

<table id="table_xvp_l4d_mjc"><thead><tr><th>

Server

</th><th>

URL/Endpoint

</th><th>

Services

</th><th>

Authentication

</th><th>

Notes

</th></tr></thead><tbody><tr><td>

Zoom

</td><td>

`https://mcp.zoom.us/mcp/zoom/streamable`

</td><td>

-   Meetings
-   Team Chat
-   Zoom Docs \(search and retrieval\)
-   AI summaries
-   Recordings and transcripts

</td><td>

-   OAuth 2.0 registered via Zoom App Marketplace.
-   Server-to-Server OAuth supported for headless use.

</td><td>

Enables natural-language retrieval of meeting assets including AI summaries, docs, recordings, and whiteboards.

</td></tr><tr><td>

Zoom Revenue Accelerator

</td><td>

`https://mcp.zoom.us/mcp/revenue_accelerator/streamable`

</td><td>

-   Conversation intelligence
-   Deal insights
-   Sales activity
-   CRM data
-   Coaching signals

</td><td>

OAuth 2.0 registered via Zoom App Marketplace.

</td><td>

-   Focused MCP surface for sales insights and deal intelligence.
-   Supports reviewing customer interactions and preparing follow-up notes.
-   Requires a Zoom Revenue Accelerator license.

</td></tr><tr><td>

Zoom Whiteboard

</td><td>

`https://mcp.zoom.us/mcp/whiteboard/streamable`

</td><td>

-   Whiteboard creation and management
-   Diagram generation

</td><td>

OAuth 2.0 registered via Zoom App Marketplace.

</td><td>

-   Provides MCP tools for creating editable whiteboards and diagrams from prompts and locating existing boards.
-   Intended for workshop planning, visual collaboration, and diagram-generation use cases.
-   Exposes only boards the authenticated user can access.

</td></tr><tr><td>

Zoom Docs

</td><td>

`https://mcp.zoom.us/mcp/docs/streamable`

</td><td>

-   Document creation
-   Document retrieval
-   Notes in Markdown

</td><td>

OAuth 2.0 registered via Zoom App Marketplace.

</td><td>

-   Supports creating new Zoom Docs from Markdown content and retrieving existing Zoom Docs or notes.
-   Designed for structured document generation and read-back flows.
-   Does not expose update or delete operations.

</td></tr><tr><td>

Zoom Chat

</td><td>

`https://mcp.zoom.us/mcp/team_chat/streamable`

</td><td>

-   Team chat channels
-   Messages
-   Contacts
-   Collaboration context

</td><td>

OAuth 2.0 registered via Zoom App Marketplace.

</td><td>

-   Focused MCP surface for chat channels, messages, contacts, and collaboration context.
-   Supports locating chat history, preparing summaries, and generating follow-ups.
-   Separate from the Zoom Workspace server; exposes write and update tools for messages and channels.

</td></tr><tr><td>

Atlassian Rovo

</td><td>

`https://mcp.atlassian.com/v1/mcp` Legacy SSE endpoint \(`/v1/sse`\) deprecated after June 30, 2026.

</td><td>

-   Jira
-   Confluence
-   Compass

</td><td>

-   OAuth 2.1.
-   API token supported for headless or machine-to-machine use if enabled by org admin.

</td><td>

-   Cloud-based bridge between an Atlassian Cloud site and compatible external tools.
-   All actions respect existing user permissions. Exposes 46+ tools across product areas.

</td></tr><tr><td>

DocuSign

</td><td>

`https://mcp.docusign.com/mcp`

</td><td>

-   e-Signature
-   Envelope management
-   Agreement workflows
-   Maestro
-   Navigator

</td><td>

OAuth 2.0 access token is required per interaction.

</td><td>

-   Enables natural-language interaction with DocuSign APIs, including authentication, API testing, and envelope creation.
-   Production connectors support seven API groups; additional endpoints accessible in developer mode.

</td></tr><tr><td>

Miro

</td><td>

`https://mcp.miro.com/`

</td><td>

-   Whiteboard and board content
-   Sticky notes, shapes, frames
-   Diagram generation
-   Comments

</td><td>

OAuth 2.1 with dynamic client registration

</td><td>

-   Supports content summarization, board creation, diagram generation, and comment resolution.
-   Users must supply a board URL in prompts; agents cannot discover or access boards not explicitly referenced.

</td></tr><tr><td>

Figma

</td><td>

-   Remote: `https://mcp.figma.com/mcp`
-   Desktop/local: `http://127.0.0.1:3845/sse`

</td><td>

-   Design files and nodes
-   Components and variables
-   Styles
-   Code Connect
-   FigJam
-   Code-to-canvas capture

</td><td>

OAuth 2.0 \(browser-based; `mcp:connect` scope required; access limited to clients in the Figma MCP Catalog\)

</td><td>

Enables design context extraction, native Figma content creation, and live UI capture as design layers.

</td></tr><tr><td>

Linear

</td><td>

-   Streamable HTTP \(recommended\): `https://mcp.linear.app/mcp`
-   SSE \(deprecated\): `https://mcp.linear.app/sse`

</td><td>

-   Issues
-   Projects
-   Cycles
-   Comments
-   Teams and labels

</td><td>

OAuth 2.1 with dynamic client registration \(no API key required; browser OAuth flow\)

</td><td>

Provides 25+ tools covering the full project management workflow.

</td></tr><tr><td>

Prisma

</td><td>

-   Remote: `https://mcp.prisma.io/mcp`
-   Local: `npx prisma mcp` \(CLI\)

</td><td>

-   Prisma Postgres database provisioning
-   Schema migrations
-   Backups
-   Connection strings
-   SQL query execution
-   Database recovery

</td><td>

OAuth \(browser-based authentication via Prisma Console on first use\)

</td><td>

Dual-mode architecture: local server handles development workflows \(migrations, schema, queries\); remote server manages Prisma Postgres infrastructure.

</td></tr></tbody>
</table>**Note:** Some connectors may require additional configurations. See [Additional connector configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/additional-configs-mcr.md) for the list of supported connectors that require additional configurations. If your connector is listed, perform the required configurations before registering the client manually.

