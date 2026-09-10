---
title: Service Mapping MCP tools
description: The Service Mapping tools expose live application service data and enable AI clients to query service topology, identify mapping gaps, and create application services in natural language.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-mapping/service-mapping-mcp-server.html
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 8
keywords: [MCP Server, Service Mapping, Claude, Model Context Protocol, AI assistant, application service topology, MCP Server Console, CMDB MCP Server]
breadcrumb: [AI in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping MCP tools

The Service Mapping tools expose live application service data and enable AI clients to query service topology, identify mapping gaps, and create application services in natural language.

The Service Mapping MCP tools provide query and create processes for investigating, visualizing, and building service topology, by implementing the Model Context Protocol \(MCP\) on the ServiceNow AI Platform. The MCP gives AI clients structured, secured, tool-based access to your data in the ServiceNow® instance.

Once a license is obtained, the admin can set up the CMDB MCP Server. Then users can connect Claude Desktop, and use it to query in natural language and create services. Claude selects the appropriate tool and retrieves live data or creates records directly from the ServiceNow® instance over OAuth 2.0 and JWT authentication. The results are presented in several visualizations or confirmations.

## Benefits

-   **Reduced time to insight**

    Getting a complete picture of an application service through a natural-language query in Claude.

-   **AI access to live Service Mapping data**

    Without the MCP tools, Claude has no programmatic access to live Service Mapping state. They must rely on static snapshots or user-provided context, leading to stale or inaccurate outputs. The MCP tools give Claude access to current data directly from the instance at query time.

-   **Visibility into traffic connections outside the CMDB**

    CIs connected only by observed TCP traffic, with no matching Configuration Management Database \(CMDB\) relationship, are invisible to operators until something breaks. The get\_unmapped\_topology tool surfaces these CIs so admins can prioritize mapping work proactively.

-   **Service creation at scale**

    The create\_top\_down\_service tool enables bulk onboarding of applications without manual efforts. An admin can prompt "create services using these entry points" and the tool creates application service records, detects entry point types \(HTTP vs TCP\), and triggers discovery. For detailed information on prompts and outputs, see [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md).

-   **Secure, role-controlled access**

    The MCP tools enforce the same ACLs and role permissions that govern standard ServiceNow REST API calls. Each request is executed under the authenticated user's session using caller-scoped data access \(GlideRecordSecure\). OAuth 2.0 with JWT tokens is used to authenticate the AI client connection.

    Read-only tools require the sm\_mcp\_user role. The create\_top\_down\_service write tool requires the sm\_mcp\_admin role.

-   **No additional scripting required**

    The six Service Mapping tools ship as part of the CMDB MCP Server scoped application. Once the server is activated and the AI client is connected, the tools are available immediately. All tools return structured, consistent responses and degrade gracefully when CMDB data is incomplete, returning partial results with a warning flag rather than a hard failure.


## How the Service Mapping MCP tools work

The Service Mapping MCP tools are built on the following technical stack:

-   **Six scripted REST API tools**

    Five tools map to read-only scripted REST API endpoints under /api/sn\_sm\_gen\_ai/ on the ServiceNow instance. One tool, create\_top\_down\_service, maps to a write-enabled endpoint that creates cmdb\_ci\_service\_discovered records and triggers asynchronous Service Mapping discovery. All tools are registered as REST API type tools in the MCP Server Console.

-   **MCP Framework integration**

    The server uses MCP Framework version 1.4.2 \(sn\_mcp v1.4.2\). The MCP Discovery Layer at `/sncapps/mcp-server/mcp/...` receives tool invocation requests from external clients and routes them to the scripted REST API.

-   **OAuth 2.0 and JWT authentication**

    External clients authenticate using OAuth 2.0 Authorization Code grant with JWT token format. ACL filtering and role-based scope enforcement are applied at the scripted REST API layer. The OAuth inbound integration must use the service\_mapping\_mcp\_auth\_scope authorization scope, limited to the MCP Tools API and CMDB Mcp Api. Using a different scope results in a successful OAuth connection but no tools visible in the AI client.

-   **Caller-scoped data access**

    Business logic is executed by the Service Mapping MCP tools, ensuring data is returned only for CIs and services the authenticated user is permitted to access.

    Write operations \(service creation\) are performed under the authenticated user's permissions. The create\_top\_down\_service tool is restricted to users with the sm\_mcp\_admin role.

    The data sources are CMDB Services tables, CMDB relationships, TCP Traffic, and service record creation tables.

-   **Asynchronous discovery on write**

    When create\_top\_down\_service creates a new service record, Service Mapping discovery job is initiated from the provided entry point. Discovery runs asynchronously in the background and does not block the tool response. The tool returns immediately to the AI client with the new service system ID. Claude can continue with topology queries or other operations without waiting for discovery to complete.


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

The CMDB MCP Server provides six tools: five read-only query tools and one write tool for service creation. All tools are consumable by Claude via the MCP protocol without additional transformation.

Access to each tool is controlled by the same ACLs that apply to the corresponding ServiceNow REST API. If the authenticated user does not have the required role, the tool returns an authorization error. For detailed role requirements, see [Configure roles for the Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.md).

For detailed input and output specifications and example queries, see [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md).

-   **get\_all\_application\_service\_names**

    Returns a catalog of all application service names. Use this tool to browse the service catalog or locate a specific service before querying its topology.

    The following example shows get\_all\_application\_service\_names returning a categorized portfolio view of all mapped services in an instance, broken down by service type.

    \[Omitted image "sm-mcp-catalog-portfolio.png"\] Alt text: The output showing 103 named services grouped into categories: Financial, Enterprise platforms, Customer-facing, and Discovered.

-   **get\_all\_application\_service\_for\_server**

    Returns all application services that include a specified server as a member CI. Use this tool to assess which services are at risk when a server is degraded or undergoing maintenance.

    The following example shows get\_all\_application\_service\_for\_server identifying every named service at risk from a single Windows server.

    \[Omitted image "sm-mcp-server-triage-radial.png"\] Alt text: The output showing a server connected to four impacted application services via a radial diagram, with the label 4 services impacted if this fails.

-   **get\_application\_service\_topology**

    Returns the full topology of a specified application service, including all member CIs and the CMDB relationships \(edges\) connecting them, with CI class, relationship type, and direction. Reflects the current state of the service map, not a cached version.

    \[Omitted image "sm-mcp-topology.png"\] Alt text: Topology graph with 14 members, 21 edges, and 4 CI classes across SERVICE, APP, DB, and HOSTS layers, with Depends on and Runs on edges.

-   **get\_server\_impact\_graph**

    Given a server CI, returns the observed connections using TCP traffic edges and CMDB relationships. Use this tool to walk the graph outward from a host and view how far the cascade goes.

    \[Omitted image "sm-mcp-blast-radius.png"\] Alt text: The output showing concentric hop rings with 3 hops, 25 or more CIs reached, 35 edges walked, and a capped traversal depth indicator.

-   **get\_unmapped\_topology**

    Starting from a single server or application CI, returns the CIs reachable from it by observed TCP traffic only, without traversing CMDB relationships. Use this tool alongside get\_server\_impact\_graph to see what a CMDB-only map is missing.

    The following example shows get\_server\_impact\_graph and get\_unmapped\_topology side by side for the same server, illustrating the difference between CMDB-modeled edges \(left\) and traffic-only connections not already captured in the CMDB \(right\).

    \[Omitted image "sm-mcp-impact-vs-unmapped.png"\] Alt text: Side-by-side comparison: on the left, get\_server\_impact\_graph showing 35 CMDB-modeled edges and 25 CIs; on the right, get\_unmapped\_topology showing 0 traffic-only edges for the same server, confirming full CMDB coverage.

-   **create\_top\_down\_service**

    Creates a new application service from one or more entry points \(HTTP URLs or TCP host-and-port pairs\). Automatically detects each entry point's type and validates inputs. Use this tool to onboard applications, stand up services on demand, or automate service creation workflows.

    This tool requires the sm\_mcp\_admin role. For detailed information, see [Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md)


## Setting up the Service Mapping MCP tools

Setting up the Service Mapping MCP tools involves sequential tasks performed by a system administrator, followed by a connection step performed by each Service Mapping user.

\[Omitted image "mcp-server-flow-sep26.png"\] Alt text: Four-stage setup flow: install the MCP plugin and assign roles, activate the MCP server, configure OAuth, then connect Claude Desktop and call the Service Mapping MCP tools.

-   **[Configure roles for the Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-config-role-hierarchy.md)**  
Assign the required roles to users so they can connect to the CMDB MCP Server and call the Service Mapping MCP tools.
-   **[Activate the CMDB MCP Server for Service Mapping tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/activate-sm-mcp-server.md)**  
Activate the CMDB MCP Server and configure the OAuth inbound integration so that external AI clients can connect to your ServiceNow® instance and query application service data.
-   **[Connect Claude Desktop to the Service Mapping MCP Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/connect-claude-desktop-sm-mcp.md)**  
Add the Service Mapping MCP Server as a custom connector in Claude Desktop so you can query application service data from your ServiceNow® instance in natural language.
-   **[Service Mapping MCP tools reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/sm-mcp-tools.md)**  
Details on the six Service Mapping MCP tools, including their inputs, outputs, and example natural-language queries for use with Claude, and service creation workflows.

**Parent Topic:**[AI in Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-mapping/ai-workflows-service-mapping.md)

