---
title: Exploring Knowledge Graph
description: Knowledge Graph provides a customized user experience for enterprises by creating and managing Knowledge Graph schemas that are represented by nodes, node properties, and edges.
locale: en-US
release: xanadu
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Knowledge Graph, Now Assist, Enable AI experiences]
---

# Exploring Knowledge Graph

Knowledge Graph provides a customized user experience for enterprises by creating and managing Knowledge Graph schemas that are represented by nodes, node properties, and edges.

## Knowledge Graph overview

ServiceNow Knowledge Graph application provides two main functionalities:

1.  Knowledge Graph designer: A user-friendly interface to manage Knowledge Graph schemas and their nodes, node properties, and edges.
2.  Prebuilt integrations: Integrations with Now Assist Virtual Agent and AI agents.

## Knowledge Graph Designer

Knowledge Graph Designer is a dedicated, no-code UI where Knowledge Graph administrators \(kg\_admins\) can effortlessly:

-   Design and manage Knowledge Graph schemas, including configuring nodes \(tables\), properties \(columns\), and relationships.
-   Analyze results of the Knowledge Graph APIs integrated in downstream products by auditing the schema using natural language queries and achieved responses.

The Knowledge Graph Designer streamlines the entire process, from schema creation and data ingestion to performance monitoring and results analysis. The new approach confirms a scalable, flexible, and intuitive way for Knowledge modeling.

## Prebuilt Integrations

By unifying Knowledge across platforms and integrating with Now Assist, AI Search, AI agents, and skill kit, the prebuilt integrations of Knowledge Graph helps the customer drive productivity, enhance decision-making, and unlock the full potential of enterprise data, while maintaining robust data governance and permission controls.

In this release, the available prebuilt integrations are:

1.  Integration with Now Assist Virtual Agent and AI agents for User Context: Helps users with personalized responses.
2.  Integration with Now Assist Virtual Agent for Slot filling: Helps pre-fill the slots for Virtual Agent topics using the Natural Language Querying feature of Knowledge Graph.
3.  Integration with Now Assist Virtual Agent for Employee schema: Helps requesters with personalized responses on people queries and Natural Language queries. Also supports people citation card. By default the user NLQ graph is connected which is used for people queries but you also have sample graph schema for other employee queries. For more details see [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069778).
4.  Integration with AI agents as a tool: Used to retrieve results in Natural Language and perform follow up tasks that are assigned to the AI agents.

## Knowledge Graph users

|User role|KG Functionality|Description|
|---------|----------------|-----------|
|Knowledge Graph Admin \(kg\_admin\)|Knowledge Graph Designer|The Knowledge Graph Admin can create and manage Knowledge Graph schemas.|
|Requester|Prebuilt integration with Virtual Agent and Agentic AI|Helps requesters with personalized answers and fewer conversation turns with pre-filled slots for LLM topics and skills.|

## Knowledge Graph benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Enhance user experience \(with prebuilt integration for downstream products like Now Assist Virtual Agent and Agentic AI\)|Provides accurate data with minimal user effort.|Requesters|
|Simple and easy to use|Creates a complex data model called Knowledge Graph schema with numerous entities and their relation within a few steps.|kg\_admin|
|Easy to manage|Editing Knowledge Graph schemas to add new nodes or edges is simple.|kg\_admin|
|Customizable Knowledge Graph schemas|Provides an option to copy the ServiceNow Knowledge Graph schemas for customization.|kg\_admin|
|Test a Knowledge Graph schema|Provides an option to test a Knowledge Graph schema by running a query.|kg\_admin|

## What to explore next

To learn more about configuring and using Knowledge Graph, see:

-   [Configuring Knowledge Graph](../Task/configuring-knowledge-graph.md)
-   [Using Knowledge Graph Designer](../Task/using-knowledge-graph-designer.md)
-   [Reference for Knowledge Graph](../Reference/reference-for-knowledge-graph.md)

