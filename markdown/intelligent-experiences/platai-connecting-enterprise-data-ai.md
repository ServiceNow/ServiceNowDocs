---
title: Connecting enterprise data for AI
description: Workflow Data Fabric connects enterprise data across systems, governs it through stable contracts, and makes it available to AI agents, workflows, and analytics on the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-connecting-enterprise-data-ai.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Workflow Data Fabric, Connect Hub, Data Catalog, Data Products, Data Interfaces, data fabric tables, enterprise data]
breadcrumb: [Managing data for AI, Enable AI Experiences]
---

# Connecting enterprise data for AI

Workflow Data Fabric connects enterprise data across systems, governs it through stable contracts, and makes it available to AI agents, workflows, and analytics on the ServiceNow AI Platform.

AI capabilities on the ServiceNow AI Platform are only as effective as the data they can access. Workflow Data Fabric is the unified data foundation that addresses a common enterprise challenge: data scattered across dozens of systems, integrations rebuilt team by team, and AI agents lacking the governed context needed to act reliably. Once data is connected and governed through Workflow Data Fabric, any team can discover and reuse it without rebuilding pipelines or compromising data integrity.

## How Workflow Data Fabric supports AI

AI agents, generative AI skills, and agentic workflows consume data through the governed contracts that Workflow Data Fabric provides. When an AI agent needs to retrieve information from an external system to complete a task, or when a workflow needs real-time data from a data warehouse to make a decision, Workflow Data Fabric supplies that data through stable, access-controlled interfaces. This means AI capabilities operate on trusted, contextualized data rather than on ad hoc integrations that may lack governance or break over time.

## Workflow Data Fabric lifecycle

Workflow Data Fabric operates through four phases that separate planning, access, governance, and consumption:

-   **Prepare**

    Explore the Data Catalog to find existing data products and data interfaces that may already meet your needs. ServiceNow Otto for Workflow Data Fabric \(WDF\) provides AI-guided recommendations that help you determine whether to reuse existing data or connect a new source.

-   **Connect**

    Establish secure connections to external systems in Connect Hub. Connect Hub is a unified workspace for discovering, building, and managing integrations between ServiceNow and external systems. Connection admins configure credentials, authentication, and metadata collectors for external data sources including databases, APIs, data lakes, and SaaS applications.

-   **Understand**

    Convert raw connectivity into governed, reusable data. Metadata collectors automatically populate the Data Catalog with discovered schemas, lineage, and governance metadata. Data stewards author data interfaces in the Data Workbench — stable contracts that define how consumers access data — and package them into data products with business context, documentation, and access controls.

-   **Act**

    Discover published data products in the Data Catalog, request access through governance workflows, and consume data through Workflow Studio, dashboards, API queries, and AI agents. Data is consumed exclusively through data interface contracts, preserving governance boundaries and data quality.


## Key components

-   **Connect Hub**

    A unified workspace for discovering, building, and managing integrations. Connect Hub supports prebuilt integration components including spokes and zero copy connectors, and provides access to Model Context Protocol clients for connecting AI agents to external tools.

-   **Data Catalog**

    A self-service discovery layer where consumers browse and evaluate data products, data interfaces, and other cataloged assets. The Data Catalog displays trust scores, lineage, and governance metadata, enabling consumers to request access and confirm data usability before building on it.

-   **Data Workbench**

    The interface where data stewards create data interfaces and data products. Data interfaces are stable, governed contracts that define the schema through which consumers access data. They support single table, JOIN, and UNION patterns, and enforce backward compatibility to protect consumers from breaking changes. Data products package one or more data interfaces with business meaning, documentation, and governance metadata.

-   **Data fabric tables**

    A projection of an external data object that makes external data accessible as if it were a local ServiceNow table, without physically copying the data. Data fabric tables enable AI agents and workflows to query external data in real time using the same patterns they use for instance data.

-   **ServiceNow Otto for Workflow Data Fabric \(WDF\)**

    An AI-guided entry point that helps you discover data fabric tables, connectors, and collectors, and request guidance on how to set up integrations. Describe what you need in natural language and Now Assist recommends whether to reuse existing data or connect a new source, then routes you to the right place.


## Explore further

To connect data sources, define the contracts that govern how that data is accessed, and make it available to AI agents, workflows, and analytics, see [Workflow Data Fabric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/create-integrations-applications.md).

