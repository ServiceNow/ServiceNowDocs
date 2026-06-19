---
title: Exploring Workflow Data Fabric Home
description: Workflow Data Fabric Home is ServiceNow's unified data foundation that connects enterprise data where it lives, governs it through stable contracts, and makes it ready for workflows, analytics, and AI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/exploring-workflow-data-fabric.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [explore]
breadcrumb: [Workflow Data Fabric Home, Workflow Data Fabric]
---

# Exploring Workflow Data Fabric Home

Workflow Data Fabric Home is ServiceNow's unified data foundation that connects enterprise data where it lives, governs it through stable contracts, and makes it ready for workflows, analytics, and AI.

## Workflow Data Fabric Home overview

Workflow Data Fabric addresses a common enterprise challenge: Data is scattered across dozens of systems, integrations are rebuilt team by team, and AI agents lack the governed context they need to act reliably. Workflow Data Fabric Home addresses this challenge so that once data is connected and governed, any team can discover and reuse it without rebuilding pipelines or compromising data integrity.

-   **Now Assist for Workflow Data Fabric \(WDF\)**

    The AI-guided entry point and parent interface for Workflow Data Fabric, powered by Now Assist for WDF. Describe what you need and Now Assist for WDF recommends whether to reuse existing data or connect a new source, and then routes you to the right place.

-   **Connect Hub**

    Where Connection Admins create and manage connections to external systems. From Connect Hub, admins configure credentials and authentication, set up metadata collectors, and grant Data Stewards access to work with connected data.

-   **Data Catalog**

    The self-service discovery layer where consumers browse and evaluate Data Products, Data Interfaces, and other cataloged assets. The Data Catalog displays trust scores, lineage, and governance metadata, enabling consumers to request access and confirm data usability before building on it.

-   **Data Workbench**

    The interface in Workflow Data Fabric Home where Data Stewards create Data Interfaces and Data Products. The Data Workbench is also used to define mappings, set ACLs, and publish or promote assets.


For more information, see [Workflow Data Fabric Home navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/workflow-data-fabric-tutorial.md).

## Workflow Data Fabric Home users

|User|Description|
|----|-----------|
|Connection Admin|Creates and manages connections, configures credentials, sets up metadata collectors, and grants Data Stewards access to connections.|
|Data Steward|Creates and owns all Data products  and Data interfaces. Responsibilities include schema design, governance, metadata management, backward compatibility enforcement, and lifecycle management of all data contracts.|
|WDF Builder|Creates connectors, spokes, and MCP servers to extend the connectivity layer without owning or modifying data contracts.|
|WDF Operator|Builds deterministic and agentic workflows that consume governed data through Data Interfaces. WDF Operators are consumers of contracts, not owners or modifiers.|
|WDF Consumer|Explores the Data Catalog to discover data products, evaluates them for use, requests access, and uses governed data through workflows, analytics, AI agents, or APIs.|

For more information, see [Workflow Data Fabric Home roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/installed-with-workflow-data-fabric.md).

## Workflow Data Fabric Home benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Discover and reuse existing data connections.|Data Catalog, Connect Hub|All users|
|Find data assets through marketplace-style browsing with trust scores, lineage, and semantic search.|Data Catalog|WDF Consumer, WDF Builder|
|Get AI-guided recommendations.|Now Assist for Workflow Data Fabric|All users|
|Package related Data Interfaces with business meaning, documentation, and governance metadata.|Data Workbench, Data products|WDF Consumer, Data Steward|
|Support single table, JOIN, UNION, bi-directional synchronization, and aggregation patterns.|Data Workbench, Data interfaces|Data Steward|
|Continuously discover schemas, build lineage, and enrich governance metadata without manual effort.|Metadata collectors|Data Steward, WDF Consumer|
|Provide trusted, contextualized data that AI agents and workflows can safely consume.|Data products, Metadata|WDF Operator|

## What to explore next

To learn more about configuring and using Workflow Data Fabric Home, see:

-   [Configuring Workflow Data Fabric Home](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/configuring-workflow-data-fabric.md)
-   [Now Assist for Workflow Data Fabric \(WDF\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/now-assist-for-workflow-data-fabric-landing.md)
-   [Connect to external systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)
-   [Data Catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/data-catalog.md)
-   [Data Products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/data-products.md)
-   [Workflow Data Fabric Home Reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/workflow-data-fabric-reference.md)

