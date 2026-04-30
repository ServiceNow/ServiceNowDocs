---
title: Cloud discovery solutions comparison
description: Comparing cloud discovery solutions provides insights on the relative strengths of each solution. The comparison showcases the number of resource types supported by the solutions across AWS, Azure, and GCP. The comparison can help you understand the capabilities of each solution and better manage your CMDB when using one or multiple methods.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: concept
last_updated: "2025-08-18"
reading_time_minutes: 2
keywords: [Service, Graph, Connectors, ITOM, Visibility, Patterns, Discovery, Service Mapping, AWS, Azure, GCP, Cloud]
breadcrumb: [Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Cloud discovery solutions comparison

Comparing cloud discovery solutions provides insights on the relative strengths of each solution. The comparison showcases the number of resource types supported by the solutions across AWS, Azure, and GCP. The comparison can help you understand the capabilities of each solution and better manage your CMDB when using one or multiple methods.

## Discovery and Service Mapping Patterns vs. Service Graph Connectors

ITOM Visibility offers two primary solutions for discovering cloud resources and mapping them into the Configuration Management Database \(CMDB\): Cloud Discovery and Service Mapping Patterns and Cloud Service Graph Connectors.

Patterns are the core of ITOM Visibility's native discovery capabilities. They provide a deeper, more dynamic, and holistic view of your infrastructure. Patterns use a variety of discovery methods: Agentless, agent-based, and cloud-native, to create a unified, business-aware view of your services. By leveraging machine learning, patterns automatically map technical components to their business context, creating rich relationships, and a comprehensive knowledge graph.

Service Graph Connectors, on the other hand, provides fast, point-in-time data ingesting from existing systems. They assist you quickly ingest data from specific sources like public cloud providers \(AWS, Azure, GCP\), endpoint management systems, and security or network tools.

While Service Graph Connectors provides rapid data import, Patterns provide the foundation for ongoing, automated service mapping and deeper operational insights based on regular updates from the ServiceNow Store. This difference is crucial for solving complex challenges like certificate management, firewall auditing, and a wide range of other service and operation use cases.

The choice between patterns and connectors affects coverage, level of detail, the way data is modeled in the CMDB and the frequency of update. While some resource types are supported by both solutions, the data might be populated in different CMDB CI Classes. Understanding these differences helps you plan a consistent and effective discovery strategy.

By reviewing the coverage tables for AWS, Azure, and GCP, you can

-   Identify which resources are supported by patterns, by connectors, or both.
-   Understand how the same resource type may be handled differently \(for example, patterns may bring in all zone data, while connectors may only bring in zones tied to an instance\).
-   Decide on a solution per provider, considering its CI coverage or data model. For example: Use connectors to discover your GCP resources, but use patterns for AWS and Azure.

![Bar chart that compares Patterns and Service Graph Connectors resource types: AWS (83 patterns, 70 SGC), Azure (60 patterns, 22 SGC), and GCP (120 patterns, 107 SGC).](../image/patterns-vs-sgc.jpg "Discovery and Service Mapping Patterns and Service Graph Connectors comparison")

