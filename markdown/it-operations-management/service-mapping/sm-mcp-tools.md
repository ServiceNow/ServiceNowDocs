---
title: Service Mapping MCP tools reference
description: Reference information for the six Service Mapping MCP tools provided by the CMDB MCP Server, including their inputs, outputs, and example natural-language queries for use with Claude, and service creation workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-mcp-tools.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 6
keywords: [MCP tools, Service Mapping, get\_all\_application\_service\_names, get\_all\_application\_services\_for\_a\_server, get\_application\_service\_topology, get\_server\_impact\_graph, get\_unmapped\_topology, reference, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI capabilities in Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping MCP tools reference

Reference information for the six Service Mapping MCP tools provided by the CMDB MCP Server, including their inputs, outputs, and example natural-language queries for use with Claude, and service creation workflows.

The CMDB MCP Server exposes six tools that an MCP-compatible AI client can invoke to retrieve application service data from a ServiceNow instance and create application services. Five tools are read-only and do not create, update, or delete records. One tool, Create Top Down Service, creates application service records and initiates Service Mapping discovery.

The following five tools retrieve application service data without modifying records:

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

## createTopDownService

Creates an application service record from an entry point \(HTTP URL or TCP host and port\) and initiates Service Mapping discovery. The user provides a unique service name for the service and the new entry point that is not used in another service. The user can also provide optional metadata details. The entry point type is automatically detected from the input format.

-   **Input**

    Required:

    -   service\_name \(string\) — A unique name for the application service.
    -   entry\_point \(string or object\) — A unique entry point for the service. Can be either: \(1\) a URL string \(e.g., "https://payments.acme.com"\), or \(2\) an object with host, port, and optional protocol for TCP endpoints \(e.g., \{host: "10.10.5.20", port: 6379, protocol: "TCP"\}\). Required.
    Optional:

    -   short\_description \(string\) — A brief description of the service purpose.
    -   business\_criticality \(string or integer\) — Service criticality level. Accepts "High" / 1, "Medium" / 2, "Low" / 3. Used to set the business\_criticality field on the service record.
    -   service\_classification \(string\) — Service classification category \(e.g., "Business Service", "Application Service"\). Maps to the service\_classification field.
    -   owned\_by \(string\) — Owner user name or system ID.
    -   support\_group \(string\) — Support group name or system ID for operational support assignment.
    -   operational\_status \(string\) — Operational status \(e.g., "Operational", "Pilot", "Planned"\).
    -   used\_for \(string\) — Free-text description of the service's purpose.
-   **Output**

    On success:

    -   success \(boolean\) — true
    -   service\_sys\_id \(string\) — The system ID of the newly created application service record.
    -   service\_name \(string\) — The name of the created service \(confirmation\).
    -   entry\_point\_type \(string\) — The detected entry point type: "URL" or "TCP".
    -   discovery\_status \(string\) — Status of the asynchronous discovery job \(e.g., "Initiated"\).
    -   http\_status \(integer\) — 201 \(Created\).
    On failure:

    -   success \(boolean\) — false
    -   error\_code \(string\) — Error identifier \(e.g., "MISSING\_SERVICE\_NAME", "INVALID\_ENTRY\_POINT", "INSERT\_FAILED"\).
    -   error\_message \(string\) — Human-readable error description.
    -   http\_status \(integer\) — 400 \(Bad Request\) or 500 \(Server Error\), depending on the failure type.
-   **Behavior**
    -   Entry point format is validated before record creation. If the entry point format is invalid or ambiguous, no record is created and an error is returned.
    -   Service Mapping discovery is triggered asynchronously after successful record creation \(fire-and-forget; does not block the tool response\).
    -   Optional metadata fields are mapped to their corresponding CMDB service record fields. If mapping values \(e.g., "High" to criticality 1\) are provided, they are applied automatically.
    -   The created service record is immediately visible in ServiceNow and available for topology queries via get\_application\_service\_topology.
-   **Example queries**
    -   "Create a new application service called 'Payment Gateway' that monitors the endpoint at https://payments.acme.com"
    -   "I need to onboard our Redis cache into Service Mapping. Create an application service called 'Cache Layer' pointing at host 10.10.5.20 on port 6379"
    -   "Set up a new top-down service called 'Order Processing API' with two entry points: the frontend at https://orders.acme.com and the backend TCP service at host 10.10.5.100 port 8443"
    -   "Create a new application service for our customer-facing checkout flow: Name: Checkout Service, Entry point: https://checkout.acme.com, Description: Handles all checkout and payment flows for the region, Business criticality: High, Classification: Business Service"
    -   "We need to map our new authentication service. Create it in Service Mapping with the entry point https://auth.acme.com, then once it's created show me the topology so I can confirm discovery ran correctly"
-   **Usage notes**
    -   For bulk service creation, invoke createTopDownService multiple times with different service names and entry points. Each invocation is independent.
    -   The service created by this tool can be queried immediately with get\_application\_service\_topology even if discovery is still running.
    -   If you provide all optional metadata fields at creation time, all service properties will be populated in a single call, reducing the number of follow-up edits needed.
    -   For chained workflows, pair createTopDownService with get\_application\_service\_topology to create a service and validate discovery in a single agent turn.

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md)

