---
title: Service Mapping MCP tools
description: The Service Mapping tools, delivered as part of the Now Assist CMDB MCP Server, expose live application service data and enable AI clients such as Claude to query service topology and mapping gaps in natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 6
keywords: [MCP Server, Service Mapping, Claude, Model Context Protocol, AI assistant, application service topology, MCP Server Console, CMDB MCP Server]
breadcrumb: [AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping MCP tools

The Service Mapping tools, delivered as part of the Now Assist CMDB MCP Server, expose live application service data and enable AI clients such as Claude to query service topology and mapping gaps in natural language.

The Service Mapping MCP tools provide query-based processes for investigating and visualizing service topology, by implementing the Model Context Protocol \(MCP\) on the ServiceNow AI Platform. The MCP gives AI clients structured, secured, tool-based access to your data in the ServiceNow® instance.

The admin sets up the Now Assist CMDB MCP Server in the MCP admin console, then users can connect Claude Desktop, and use it to query in natural language. Claude selects the appropriate tool, retrieves live data directly from the ServiceNow® instance over OAuth 2.0 and JWT authentication, and presents the results in several visualizations.

## Benefits

-   **Reduced time to insight**

    Getting a complete picture of an application service through a natural-language query in Claude.

-   **AI access to live Service Mapping data**

    Without the MCP tools, AI models have no programmatic access to live Service Mapping state and must rely on static snapshots or user-provided context, leading to stale or inaccurate outputs. The MCP tools give Claude access to current data directly from the instance at query time.

-   **Visibility into unmapped topology**

    CIs that have Configuration Management Database \(CMDB\) relationships or TCP traffic signals but have not yet been pulled into a service map are invisible to operators until something breaks. The MCP tools surface these CIs so admins can prioritize mapping work proactively.

-   **Secure, role-controlled access**

    The MCP tools enforce the same ACLs and role permissions that govern standard ServiceNow REST API calls. Each request is executed under the authenticated user's session using caller-scoped data access \(GlideRecordSecure\). OAuth 2.0 with JWT tokens is used to authenticate the AI client connection.

-   **No additional scripting required**

    The five Service Mapping tools ship as part of the CMDB MCP Server scoped application. Once the server is activated and the AI client is connected, the tools are available immediately. All tools return structured, consistent responses and degrade gracefully when CMDB data is incomplete, returning partial results with a warning flag rather than a hard failure.


## How the Service Mapping MCP tools work

The Service Mapping MCP tools are built on the following technical stack:

-   **Five scripted REST API tools**

    Each tool maps to a scripted REST API endpoint under `/api/sn_sm_gen_ai/` on the ServiceNow instance. The tools are registered as REST API type tools in the MCP Server Console.

-   **MCP Framework integration**

    The server uses MCP Framework version 1.4.2 \(sn\_mcp v1.4.2\). The MCP Discovery Layer at `/sncapps/mcp-server/mcp/...` receives tool invocation requests from external clients and routes them to the scripted REST API.

-   **OAuth 2.0 and JWT authentication**

    External clients authenticate using OAuth 2.0 Authorization Code grant with JWT token format. ACL filtering and role-based scope enforcement are applied at the scripted REST API layer. The OAuth inbound integration must use the service\_mapping\_mcp\_auth\_scope authorization scope, limited to the MCP Tools API and CMDB Mcp Api. Using a different scope results in a successful OAuth connection but no tools visible in the AI client.

-   **Caller-scoped data access**

    Business logic is executed by the Service Mapping MCP tools, ensuring data is returned only for CIs and services the authenticated user is permitted to access. The data sources are CMDB Services tables, CMDB relationships, and TCP Traffic.


## Scale limits

The Service Mapping MCP tools enforce the following scale limits to maintain performance.

-   **Edge maximum**

    2,000 edges per topology response.

-   **Traversal depth maximum**

    4 levels of relationship depth per query.

-   **Response time target**

    Under 5 seconds per tool call.


For application services that approach these limits, request summary data rather than full topology to stay within the bounds. For example, ask for member count and edge count only, rather than the full topology.

## Available tools

The Now Assist CMDB MCP Server provides five read-only tools. All tools are read-only and do not create, update, or delete records.

The AI client selects the appropriate tool based on the user's natural-language input and passes the required parameters. All five tools are consumable by Claude via the MCP protocol without additional transformation. The tool schemas include input and output field descriptions suitable for AI tool-calling.

Access to each tool is controlled by the same ACLs that apply to the corresponding ServiceNow REST API. If the authenticated user does not have the required role, the tool returns an authorization error.

For detailed input and output specifications and example queries, see [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md).

-   **get\_all\_application\_service\_names**

    Returns a catalog of all application service names. Use this tool to browse the service catalog or locate a specific service before querying its topology.

    The following example shows get\_all\_application\_service\_names returning a categorized portfolio view of all mapped services in an instance, broken down by service type.

    \[Omitted image "sm-mcp-catalog-portfolio.png"\] Alt text: The output showing 103 named services grouped into categories: Financial, Enterprise platforms, Customer-facing, and Discovered.

-   **get\_all\_application\_services\_for\_a\_server**

    Returns all application services that include a specified server as a member CI. Use this tool to assess which services are at risk when a server is degraded or undergoing maintenance.

    The following example shows get\_all\_application\_services\_for\_a\_server identifying every named service at risk from a single Windows server.

    \[Omitted image "sm-mcp-server-triage-radial.png"\] Alt text: The output showing a server connected to four impacted application services via a radial diagram, with the label 4 services impacted if this fails.

-   **get\_application\_service\_topology**

    Returns the full topology of a specified application service, including all member CIs and the CMDB relationships \(edges\) connecting them, with CI class, relationship type, and direction. Reflects the current state of the service map, not a cached version.

    \[Omitted image "sm-mcp-topology.png"\] Alt text: Topology graph with 14 members, 21 edges, and 4 CI classes across SERVICE, APP, DB, and HOSTS layers, with Depends on and Runs on edges.

-   **get\_server\_impact\_graph**

    Given a server CI, returns the observed connections using TCP traffic edges and CMDB relationships. Use this tool to walk the graph outward from a host and view how far the cascade goes.

    \[Omitted image "sm-mcp-blast-radius.png"\] Alt text: The output showing concentric hop rings with 3 hops, 25 or more CIs reached, 35 edges walked, and a capped traversal depth indicator.

-   **get\_unmapped\_topology**

    Returns CIs that have CMDB relationships or TCP traffic signals but are not currently members of any application service, filterable by CI class. Use this tool to identify mapping gaps and prioritize further Service Mapping work.

    The following example shows get\_server\_impact\_graph and get\_unmapped\_topology side by side, illustrating the difference between CMDB-modeled edges \(left\) and traffic-only unmapped connections \(right\).

    \[Omitted image "sm-mcp-impact-vs-unmapped.png"\] Alt text: Side-by-side comparison: on the left, get\_server\_impact\_graph showing 35 CMDB-modeled edges and 25 CIs; on the right, get\_unmapped\_topology showing 0 traffic-only edges for the same server, confirming full CMDB coverage.


## Setting up the Service Mapping MCP tools

Setting up the Service Mapping MCP tools involves sequential tasks performed by a system administrator, followed by a connection step performed by each Service Mapping user.

\[Omitted image "mcp-server-flow.png"\] Alt text: Setup flow diagram: the admin installs the plugin, configures the role hierarchy, activates the Now Assist CMDB MCP Server. The user connects Claude Desktop and call the MCP tools.

-   **[Configure roles for the Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.md)**  
Configure the role containment chain and assign the required roles to users so they can connect to the Now Assist CMDB MCP Server and call the Service Mapping MCP tools.
-   **[Activate the Now Assist CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/activate-sm-mcp-server.md)**  
Activate the Now Assist CMDB MCP Server and configure the OAuth inbound integration so that external AI clients can connect to your ServiceNow® instance and query application service data.
-   **[Connect Claude Desktop to the Service Mapping MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/connect-claude-desktop-sm-mcp.md)**  
Add the Service Mapping MCP Server as a custom connector in Claude Desktop so you can query application service data from your ServiceNow® instance in natural language.
-   **[Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md)**  
Reference information for the five Service Mapping MCP tools provided by the Now Assist CMDB MCP Server, including their inputs, outputs, and example natural-language queries for use with Claude.

**Parent Topic:**[AI capabilities in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/ai-workflows-service-mapping.md)

