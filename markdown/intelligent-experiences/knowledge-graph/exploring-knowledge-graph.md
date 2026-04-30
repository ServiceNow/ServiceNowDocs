---
title: Exploring Knowledge Graph
description: Knowledge Graph provides a connected representation of data that maps entities and their relationships, adding context and meaning to information to enable intelligent search, insights, and AI-driven experiences.
locale: en-US
release: yokohama
product: Knowledge Graph
classification: knowledge-graph
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Knowledge Graph, Enable AI experiences]
---

# Exploring Knowledge Graph

Knowledge Graph provides a connected representation of data that maps entities and their relationships, adding context and meaning to information to enable intelligent search, insights, and AI-driven experiences.

## Knowledge Graph overview

ServiceNow Knowledge Graph application enhances the Now Platform by creating a semantic layer that connects data, relationships, and context across the enterprise. It structures information as a graph of entities and connections, bringing context and meaning to the available raw data. By leveraging AI, it powers personalized and intelligent experiences across the Now Assist ecosystem including Now Assist Virtual Agent, AI Agents, and AI Search to deliver more relevant insights and automation.

By linking data and embedding semantic meaning, ServiceNow Knowledge Graph transforms raw data into actionable knowledge, fueling faster resolutions, richer insights, and more personalized AI-powered experiences.

ServiceNow Knowledge Graph application:

1.  Natural language queries: Allow users to query structured ServiceNow data conversationally—for example, “Who is my manager?”, “What’s the status of my incident?”, or “What assets are assigned to me.”
2.  User context: Provide Now Assist Virtual Agent and AI Agents with contextual information such as role, department, or location to deliver personalized and relevant responses.
3.  Slot-filing: Simplify user interactions by automatically populating known information in forms or chat requests, reducing effort and friction.
4.  Smarter AI Agents: Empower agents to retrieve insights, facts, and relationships directly from the knowledge graph to automate actions and improve accuracy.
5.  Integration with Workflow Data Fabric: Use an integrated data layer that gives real-time, secure, and unified access to data from any source without duplicating it, enabling faster, data-rich workflows across the platform.

## Knowledge Graph components

ServiceNow Knowledge Graph is a graphical representation of real-world entities \(tables\) and their relationships, stored in a database. Each graphical representation is called as a Knowledge Graph Schema that consist of relevant entities called nodes. The relationship between each entity is called an edge.

To create, edit and manage Knowledge Graph schemas for your specific use cases, ServiceNow Knowledge Graph has introduced, Knowledge Graph designer.

Users can use these schema to customize and extend Knowledge Graph integrations with Now Assist Virtual Agent and AI agents, and Now Assist Panel. Servicenow also provides some Prebuilt integrations, that connect the Knowledge Graph with Now Assist Virtual Agent and AI agents, and other ServiceNow applications, enabling seamless AI-powered workflows and personalized experiences.

## Knowledge Graph Designer

Knowledge Graph Designer is a dedicated, no-code UI where Knowledge Graph administrators \(kg\_admins\) can effortlessly:

-   Design and manage Knowledge Graph schemas, and configure the related nodes \(tables\), properties \(columns\), and their relationships.
-   Analyze results of the Knowledge Graph APIs integrated in downstream products by auditing the schema using natural language queries and achieved responses.

The Knowledge Graph Designer streamlines the entire process, from schema creation and data ingestion to performance monitoring and results analysis. The new approach confirms a scalable, flexible, and intuitive way for Knowledge modeling.

## Prebuilt Integrations

By unifying Knowledge across platforms and integrating with Now Assist, AI Search, AI agents, and skill kit, the prebuilt integrations of Knowledge Graph helps the customer drive productivity, enhance decision-making, and unlock the full potential of enterprise data, while maintaining robust data governance and permission controls.

In this release, the available prebuilt integrations are:

1.  Integration with Now Assist Virtual Agent and AI agents for User Context: Helps users with personalized responses.
2.  Integration with Now Assist Virtual Agent for Slot filling: Helps pre-fill the slots for Virtual Agent topics using the Natural Language Querying feature of Knowledge Graph.
3.  Integration with Now Assist Virtual Agent for Employee schema: Helps requesters with personalized responses on people queries and Natural Language queries. Also supports people citation card. By default the user NLQ graph is connected which is used for people queries but you also have sample graph schema for other employee queries. To see more sample graphs for employee queries refer, [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069778).
4.  Integration with AI agents as a tool: Used to retrieve results in Natural Language and perform follow up tasks that are assigned to the AI agents.

## Knowledge Graph users

|User role|KG Functionality|Description|
|---------|----------------|-----------|
|Knowledge Graph Admin \(kg\_admin\)|Knowledge Graph Designer|The Knowledge Graph Admin can create and manage Knowledge Graph schemas.|
|Requester|Prebuilt integration with Virtual Agent and Agentic AI|Helps requesters with personalized answers and fewer conversation turns with pre-filled slots for LLM topics and skills.|

## Knowledge Graph benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Enhance user experience \(with prebuilt integration for downstream products like Now Assist Virtual Agent and Agentic AI\)|Provides accurate data with minimal user effort.|Requester|
|Simple and easy to use|Creates a complex data model called Knowledge Graph schema with numerous entities and their relation within a few steps.|kg\_admin|
|Easy to manage|Editing Knowledge Graph schemas to add new nodes or edges is simple.|kg\_admin|
|Customizable Knowledge Graph schema|Provides an option to copy the ServiceNow Knowledge Graph schemas for customization.|kg\_admin|
|Test a Knowledge Graph schema|Provides an option to test a Knowledge Graph schema by running a query.|kg\_admin|
|Use Workflow Data Fabric to retrieve information without saving or copying them from the source entity. This ensures efficiency and security.|Leverage Workflow Data Fabric tables in Knowledge Graph to retrieve data.|Requester|
|Create a Knowledge Graph schema with Workflow Data Fabric tables.|To create and manage Workflow Data Fabric tables, see[Managing data fabric tables in Workflow Data Fabric Hub](https://www.servicenow.com/docs/access?context=managing-data-fabric-tables-wdf&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)|kg\_admin|

## What to explore next

To learn more about configuring and using Knowledge Graph, see:

-   [Configuring Knowledge Graph](../Task/configuring-knowledge-graph.md)
-   [Using Knowledge Graph Designer](../Task/using-knowledge-graph-designer.md)
-   [Reference for Knowledge Graph](../Reference/reference-for-knowledge-graph.md)

