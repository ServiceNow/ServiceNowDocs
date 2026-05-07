---
title: Workflow Data Fabric integration with Knowledge Graph
description: Knowledge Graph supports Workflow Data Fabric to fetch third party information securely without copying the data.
locale: en-US
release: australia
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Knowledge Graph, Knowledge Graph, Enable AI experiences]
---

# Workflow Data Fabric integration with Knowledge Graph

Knowledge Graph supports Workflow Data Fabric to fetch third party information securely without copying the data.

The integration of Workflow Data Fabric \(WDF\) with the Knowledge Graph allows organizations to seamlessly connect external and internal data sources. This integration extends the functionalities of the Knowledge Graph to external data, ensuring real-time access and enabling advanced insights, workflow automation, and personalization using external data.

The key feature of Workflow data fabric integration with Knowledge Graph are:

-   Real-Time Access: Zero Copy connectors from WDF and the semantic layer of the Knowledge Graph ensure that external data is accessible in real-time.
-   Deep Data Connection: WDF tables are automatically included in the Enterprise Graph, enhancing the connectivity and utility of external data within the ServiceNow platform.
-   Natural Language Query Support: Users can ask natural language queries \(NLQ\) in Virtual Agent and AI Agents, leveraging both external \(WDF\) and internal data.

The benefits of using Workflow data fabric integration in Knowledge Graph are:

-   Requestors and Fulfillers: Can ask NLQ questions and receive insights from external \(WDF\) tables integrated with the KG schema.
-   Admins: Can create a KG schema with WDF tables and link it to the Now Assist panel, AI Agents, or Now Assist in Virtual Agent.

Admins can add WDF tables to the Knowledge Graph just like any other internal table. However, only WDF tables configured with a primary key are supported.

Here are some integration best practices:

-   Primary Key Requirement: Always add a primary key to your WDF table during configuration. This is mandatory for supporting WDF tables in the Knowledge Graph.
-   Meaningful Naming: Use clear and meaningful names when creating WDF tables. Add synonyms to your tables in the Knowledge Graph schema as needed to improve the accuracy of natural language queries.

Here is some example use cases:

Snowflake and Google BigQuery Integration: WDF tables sourced from Snowflake and Google BigQuery can be added to the Knowledge Graph schema, allowing users to query and analyze data from these external sources within ServiceNow.

![WDF tables](../Images/snowflake-googl-example-kg.png)

