---
title: Workflow Data Fabric key terms
description: Key terms used in Workflow Data Fabric.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Workflow Data Fabric key terms

Key terms used in Workflow Data Fabric.

|Term|Description|
|----|-----------|
|Workflow Data Fabric|Workflow Data Fabric is a unified data foundation that connects to enterprise data across systems, contextualizes it with metadata and stable contracts, making it available to workflows, analytics, and AI agents.|
|Workflow Data Fabric Home|The AI-guided entry point and parent interface for Workflow Data Fabric, powered by Now Assist for WDF. It provides natural language search across the catalog, recommendations on reuse versus building new, and navigation to specific tasks like Connect Hub.|
|Data product|A governed, reusable package built from one or more Data Interfaces that represent a business concept, such as shipment, invoice, or project. Data products provide a standardized, governed, and discoverable interface so it’s reliable, reusable, and easy to consume by developers, analysts, and AI agents. Data products include metadata, documentation, ownership, and access control, and are published to the Data Catalog for discovery.|
|Data interface|A stable, governed data contract that defines the schema through which consumers access data. A Data interface can represent a single table, joined tables, or a union of multiple sources, and enforces backward compatibility to protect consumers from breaking changes.|
|Data fabric table|A ServiceNow projection of an external data object that makes external data accessible as if it were a local ServiceNow table, without physically copying the data.|
|Data Workbench|The interface in Workflow Data Fabric Home where Data Stewards create Data Interfaces and Data Products. The Data Workbench is also used to define mappings, set ACLs, and publish or promote assets to Production.|
|Metadata Collector|An automated scanner that runs against a connected data source to discover schemas, build lineage relationships, and populate governance metadata into the Data Catalog.|
|Connectors|Prebuilt integration components that define communication with specific external applications. A connector acts as a translator between ServiceNow and the target system, providing actions, triggers, and data-mapping capabilities.|
|Connection|A secure, governed access path between ServiceNow and an external data source, such as a database, SaaS application, REST API, event stream, or another ServiceNow instance.|
|Spoke|A packaged, reusable integration available from the ServiceNow Store that provides prebuilt actions for common third-party systems \(such as Azure DevOps, Salesforce, or Jira\), enabling quick connectivity without custom development.|
|MCP Server \(Model Context Protocol\)|A server that provides structured context to AI agents rather than moving data. It acts as a context broker, giving AI agents governed, semantically rich information to inform their decisions and actions.|
|Connect Hub|The interface in Workflow Data Fabric Home where Connection Admins create and manage connections to external systems. From Connect Hub, admins configure credentials and authentication, set up metadata collectors, and grant Data Stewards access to work with connected data.|
|Trust Score|A signal visible in the Data Catalog that helps consumers evaluate the quality, governance, and reliability of a data asset before building on it.|
|Mapping|Mapping describes how data from different sources line up to the data product’s interface. It’s the bridge between raw data and the trusted version inside the data product.|
|Knowledge graph|Data Products are linked semantically by ontology, taxonomy, and metadata forming a knowledge graph from which you can query and build reasoning across domains.|
|Data Catalog|The self-service discovery layer where consumers browse and evaluate Data Products, Data Interfaces, and other cataloged assets. The Data Catalog displays trust scores, lineage, and governance metadata, enabling consumers to request access and confirm data usability before building on it.|
|Zero Copy Connector \(ZCC\)|An integration mechanism that provides real-time query access to external data without moving or copying it into ServiceNow. Zero Copy Connectors are best suited for large data volumes and analytics use cases where data freshness matters.|

**Parent Topic:**[Workflow Data Fabric Home Reference](../concept/workflow-data-fabric-reference.md)

