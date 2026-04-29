---
title: Workflow Data Fabric Home roles
description: Several user roles are installed with activation of the ServiceNow WDF Unified Hub plugin.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Workflow Data Fabric Home roles

Several user roles are installed with activation of the ServiceNow WDF Unified Hub plugin.

## Roles installed

<table id="table_uvc_lc3_hhc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Connection Admin

 \[connection\_admin\]

</td><td>

Create and manage connections, configure credentials, set up metadata collectors, and grant Data Stewards access to connections.

</td><td>

-   \[df\_data\_steward\]
-   \[external\_app\_install\_admin\]
-   \[agent\_admin\]
-   \[credential\_admin\]
-   \[web\_service\_admin\]
-   \[sn\_nowassist\_wdf.creator\_admin\]

</td></tr><tr><td>

Data Steward

 \[df\_data\_steward\]

</td><td>

Create and own all Data products  and Data interfaces. Responsibilities include schema design, governance, metadata management, backward compatibility enforcement, and lifecycle management of all data contracts.

</td><td>

-   \[sn\_nowassist\_wdf.creator\_admin\]
-   \[wdf\_consumer\]

</td></tr><tr><td>

WDF Builder

 \[wdf\_builder\]

</td><td>

Create connectors, spokes, and MCP servers to extend the connectivity layer without owning or modifying data contracts.

</td><td>

-   \[wdf\_consumer\]
-   \[sn\_nowassist\_wdf.creator\_admin\]
-   \[connection\_admin\]
-   \[template\_editor\_global\]
-   \[action\_designer\]
-   \[sn\_appclient.app\_client\_user\]
-   \[sn\_g\_app\_creator.app\_creator\]

</td></tr><tr><td>

WDF Operator

 \[wdf\_operator\]

</td><td>

Build deterministic and agentic workflows that consume governed data through Data Interfaces. WDF Operators are consumers of contracts, not owners or modifiers.

</td><td>

-   \[fd\_read\]
-   \[now.assist.creator\]
-   \[flow\_designer\]
-   \[sn\_nowassist\_wdf.creator\_admin\]
-   \[sn\_mcp\_client.viewer\]
-   \[wdf\_consumer\]

</td></tr><tr><td>

WDF Consumer

 \[wdf\_consumer\]

</td><td>

Explore the Data Catalog to discover data products, evaluate them for use, request access, and use governed data through workflows, analytics, AI agents, or APIs.

</td><td>

\[sn\_nowassist\_wdf.creator\_admin\]

</td></tr></tbody>
</table>**Parent Topic:**[Workflow Data Fabric Home Reference](../concept/workflow-data-fabric-reference.md)

