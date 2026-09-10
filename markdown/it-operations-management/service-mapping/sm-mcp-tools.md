---
title: Service Mapping MCP tools reference
description: Details on the six Service Mapping MCP tools, including their inputs, outputs, and example natural-language queries for use with Claude, and service creation workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/sm-mcp-tools.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 7
keywords: [MCP tools, Service Mapping, get\_all\_application\_service\_names, get\_all\_application\_service\_for\_server, get\_application\_service\_topology, get\_server\_impact\_graph, get\_unmapped\_topology, create\_top\_down\_service, reference, Now Assist, CMDB]
breadcrumb: [Service Mapping MCP tools, AI in Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Service Mapping MCP tools reference

Details on the six Service Mapping MCP tools, including their inputs, outputs, and example natural-language queries for use with Claude, and service creation workflows.

The CMDB MCP Server exposes six tools that an MCP-compatible AI client can invoke to retrieve application service data from a ServiceNow instance and create application services. Five tools are read-only and do not create, update, or delete records. One tool, create\_top\_down\_service, creates application service records and initiates Service Mapping discovery.

The create\_top\_down\_service tool requires the sm\_mcp\_admin role. The five read-only tools require sm\_mcp\_user.

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

## get\_all\_application\_service\_for\_server

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
    -   "Use the ServiceNow Service Mapping tool, get\_all\_application\_service\_for\_server, to find which services contain server emse-10152008.servicenow.com"
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

    Application services with a large number of member CIs and edges \(more than 50 members\) return a significant volume of data. When querying topology for large services, ask Claude for a summary or specific counts to avoid reaching message-length limits on the Claude free tier.


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

Starting from a single server or application CI, returns the CIs reachable from it by observed TCP traffic only. This tool doesn't traverse CMDB relationships. Use it together with get\_server\_impact\_graph, which returns the fused CMDB-relationship-and-traffic view, to see what a CMDB-only map is missing.

-   **Input**

    **ci**: Required. The name or system ID of the starting server or application CI.

-   **Output**

    An adjacency graph of the CIs reached by traffic-only traversal. The response includes:

    -   An adjacency list and CI names for the traversed nodes
    -   The starting server or application CI
    -   A stop reason for the traversal, for example reaching the maximum depth or exhausting all connections
    -   The count of CIs visited
    -   The count of traffic edges found
    -   A fixed reminder that CMDB relationships are excluded and to use get\_server\_impact\_graph for the fused view
    If the input name matches more than one CI, the response also includes a warning noting that the tool resolved to the first match and recommending a system ID for a deterministic result. If the specified CI doesn't exist, or exists but isn't a supported class, the tool returns an error identifying which case applies.

-   **Example queries**
    -   "Use the ServiceNow Service Mapping tool, get\_unmapped\_topology, to show me what's connected to server db-cluster-02 by traffic only."
    -   "Use the ServiceNow Service Mapping tool, get\_unmapped\_topology, starting from application server app-01."

## create\_top\_down\_service

Creates an application service record from one or more entry points \(HTTP URLs or TCP host-and-port pairs\). The user provides a unique service name and at least one entry point that isn't already used by another service. The user can also provide optional metadata details. Each entry point's type is automatically detected from its format.

-   **Role requirement**

    Requires the sm\_mcp\_admin role. This tool has an operation-level ACL evaluated in addition to the endpoint-level ACL that applies to all six tools. Users with only sm\_mcp\_user role receive a 403 authorization error.

-   **Input**

    Required:

    -   name \(string\) — A unique name for the application service.
    -   entry\_points \(array\) — One or more entry points. Each entry point is either a URL string \(e.g., "https://payments.acme.com"\) or an object with host and port for a TCP endpoint \(e.g., \{host: "10.10.5.20", port: 6379\}\). At least one entry point is required.
    Optional:

    -   short\_description \(string\) — A brief description of the service purpose.
    -   business\_criticality \(string or integer\) — Service criticality level, set on the business\_criticality field as provided.
    -   service\_classification \(string\) — Service classification category \(e.g., "Business Service", "Application Service"\). Maps to the service\_classification field.
    -   owned\_by \(string\) — Owner user name or system ID.
    -   support\_group \(string\) — Support group name or system ID for operational support assignment.
    -   operational\_status \(string\) — Operational status \(e.g., "Operational", "Pilot", "Planned"\). Defaults to Operational if not provided.
-   **Output**

    On success:

    -   success \(boolean\) — true
    -   service\_sys\_id \(string\) — The system ID of the newly created application service record.
    -   http\_status \(integer\) — 201 \(Created\).
    On failure:

    -   success \(boolean\) — false
    -   error\_code \(string\) — One of missing\_name, invalid\_entry\_points, duplicate\_name, duplicate\_entry\_point, service\_insert\_failed, endpoint\_insert\_failed, or endpoint\_link\_failed.
    -   error\_message \(string\) — Human-readable error description.
    -   http\_status \(integer\) — 400 for missing\_name or invalid\_entry\_points, 409 for duplicate\_name or duplicate\_entry\_point, 500 for the remaining error codes.
-   **Behavior**
    -   Entry point format is validated before record creation. If any entry point format is invalid, no record is created and an error is returned.
    -   A service name or entry point already used by another service is rejected rather than merged into the existing record.
    -   Optional metadata fields are set directly on their corresponding CMDB service record fields, with no value translation. Provide values in the format the target field accepts.
    -   If the service record is created but a later step, such as linking an entry point, fails, the created service record is rolled back rather than left partially created.
    -   The created service record is immediately visible in ServiceNow and available for topology queries via get\_application\_service\_topology.
-   **Example queries**
    -   "Create a new application service called 'Payment Gateway' that monitors the endpoint at https://payments.acme.com"
    -   "I need to onboard our Redis cache into Service Mapping. Create an application service called 'Cache Layer' pointing at host 10.10.5.20 on port 6379"
    -   "Set up a new top-down service called 'Order Processing API' with two entry points: the frontend at https://orders.acme.com and the backend TCP service at host 10.10.5.100 port 8443"
    -   "Create a new application service for our customer-facing checkout flow: Name: Checkout Service, Entry point: https://checkout.acme.com, Description: Handles all checkout and payment flows for the region, Business criticality: High, Classification: Business Service"
    -   "We need to map our new authentication service. Create it in Service Mapping with the entry point https://auth.acme.com, then once it's created show me the topology so I can confirm it exists"
-   **Usage notes**
    -   To give one service multiple entry points, pass them all in a single entry\_points array rather than calling the tool once per entry point.
    -   For bulk service creation across separate services, invoke create\_top\_down\_service multiple times with different service names. Each invocation is independent.
    -   The service created by this tool can be queried immediately with get\_application\_service\_topology.
    -   If you provide all optional metadata fields at creation time, all service properties will be populated in a single call, reducing the number of follow-up edits needed.

**Parent Topic:**[Service Mapping MCP tools](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/service-mapping-mcp-server.md)

