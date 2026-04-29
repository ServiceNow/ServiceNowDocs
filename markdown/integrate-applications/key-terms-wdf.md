---
title: Workflow Data Fabric key terms
description: Key terms used in Workflow Data Fabric.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Workflow Data Fabric Home, Workflow Data Fabric]
---

# Workflow Data Fabric key terms

Key terms used in Workflow Data Fabric.

|Term|Description|
|----|-----------|
|Workflow Data Fabric|Workflow Data Fabric is a unified data foundation that connects to enterprise data across systems, contextualizes it with metadata and stable contracts, making it available to workflows, analytics, and AI agents.|
|Workflow Data Fabric Home|The AI-guided entry point and parent interface for Workflow Data Fabric, powered by Now Assist for WDF. It provides natural language search across the catalog, recommendations on reuse versus building new, and navigation to specific tasks like Connect Hub.|
|Data fabric table|A ServiceNow projection of an external data object that makes external data accessible as if it were a local ServiceNow table, without physically copying the data.|
|Connectors|Prebuilt integration components that define communication with specific external applications. A connector acts as a translator between ServiceNow and the target system, providing actions, triggers, and data-mapping capabilities.|
|Connection|A secure, governed access path between ServiceNow and an external data source, such as a database, SaaS application, REST API, event stream, or another ServiceNow instance.|
|Spoke|A packaged, reusable integration available from the ServiceNow Store that provides prebuilt actions for common third-party systems \(such as Azure DevOps, Salesforce, or Jira\), enabling quick connectivity without custom development.|
|Connect Hub|The interface in Workflow Data Fabric Home where Connection Admins create and manage connections to external systems. From Connect Hub, admins configure credentials and authentication, set up metadata collectors, and grant Data Stewards access to work with connected data.|
|Zero Copy Connector \(ZCC\)|An integration mechanism that provides real-time query access to external data without moving or copying it into ServiceNow. Zero Copy Connectors are best suited for large data volumes and analytics use cases where data freshness matters.|

**Parent Topic:**[Workflow Data Fabric Home Reference](../concept/workflow-data-fabric-reference.md)

