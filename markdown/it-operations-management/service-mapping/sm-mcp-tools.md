---
title: Service Mapping MCP tools reference
description: Reference information for the five Service Mapping MCP tools provided by the Now Assist CMDB MCP Server, including their inputs, outputs, and example natural-language queries for use with Claude.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-mcp-tools.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 3
keywords: [MCP tools, Service Mapping, get\_all\_application\_service\_names, get\_all\_application\_services\_for\_a\_server, get\_application\_service\_topology, get\_server\_impact\_graph, get\_unmapped\_topology, reference, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping MCP tools reference

Reference information for the five Service Mapping MCP tools provided by the Now Assist CMDB MCP Server, including their inputs, outputs, and example natural-language queries for use with Claude.

The Now Assist CMDB MCP Server exposes five tools that an MCP-compatible AI client can invoke to retrieve application service data from a ServiceNow instance. All tools are read-only and do not create, update, or delete records.

## get\_all\_application\_service\_names

Returns a list of all application service names in the instance.

-   **Input**

    An optional filter parameter to limit results by mapping type: pattern-based, tag-based, or calculated. If no filter is provided, all service types are returned.

-   **Output**

    A paginated list of entries. Each entry includes:

    -   Service name
    -   System ID
    -   Service type
    The response is paginated or bounded to prevent oversized payloads.

-   **Example queries**
    -   "Use the ServiceNow Service Mapping tool, get\_all\_application\_service\_names, to list all application services."
    -   "List all tag-based application services in ServiceNow."

## get\_all\_application\_services\_for\_a\_server

Returns all application services that include a specified server as a member CI.

-   **Input**

    Server CI name or System ID.

-   **Output**

    A list of application services. Each entry includes:

    -   Service name
    -   System ID
    -   Service type
    -   Mapping status
    If no services are found for the specified server, an empty list is returned. This is not treated as an error.

-   **Example queries**
    -   "Use the ServiceNow Service Mapping tool, get\_all\_application\_services\_for\_a\_server, to find which services contain server emse-10152008.servicenow.com"
    -   "Which application services include server haproxy-s?"

## get\_application\_service\_topology

Returns the full topology of a specified application service, including all member CIs and the CMDB relationships \(edges\) connecting them.

-   **Input**

    Application service name or System ID.

-   **Output**

    The complete topology of the service. Each CI entry includes:

    -   CI name
    -   CI class
    -   Relationship type
    -   Direction: upstream or downstream
    The topology reflects the current state of the service map, not a cached version.

-   **Example queries**
    -   "Use the ServiceNow Service Mapping tool, get\_application\_service\_topology, to get the topology for the Inclusion service. Just show me the member count and edge count, don't visualize."
    -   "Show me the topology of the Payroll service."
-   **Usage note**

    Application services with a large number of member CIs and edges \(more than 50 members\) return a significant volume of data. When querying topology for large services, ask Claude for a summary or specific counts rather than a full visualization to avoid reaching message-length limits on the Claude free tier.


## get\_server\_impact\_graph

Given a server CI, returns all CIs related to it via CMDB relationships and all CIs with observed TCP traffic connections to or from that server.

-   **Input**

    Server CI name or System ID.

-   **Output**

    A set of related CIs. The response distinguishes between:

    -   CIs related via CMDB relationships. Uses \[cmdb\_rel\_ci\] or equivalent.
    -   CIs with observed TCP traffic connections to or from the specified server
    This distinction enables AI-assisted identification of candidates for service map inclusion.

-   **Example queries**
    -   "Use the ServiceNow Service Mapping tool, get\_server\_impact\_graph, to get impact analysis for server haproxy-s."
    -   "What CIs are related to server db-cluster-02 via CMDB or traffic?"

## get\_unmapped\_topology

Returns CIs that have CMDB relationships, TCP traffic signals or both, but are not currently members of any application service. Use this tool to identify mapping gaps and prioritize further Service Mapping work.

-   **Input**

    An optional CI class filter, for example to return only Linux servers or only application servers.

-   **Output**

    A list of unmapped CIs. Each entry includes:

    -   CI name
    -   CI class
    -   Number of CMDB relationship edges
    -   Number of TCP traffic connections
-   **Example queries**
    -   "Use the ServiceNow Service Mapping tool, get\_unmapped\_topology, to show me which CIs have relationships or traffic signals but are not in any application service."
    -   "Use the ServiceNow Service Mapping tool, get\_unmapped\_topology, to show me unmapped Linux servers in ServiceNow."

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md)

