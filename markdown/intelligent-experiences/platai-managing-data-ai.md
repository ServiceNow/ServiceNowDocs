---
title: Managing data for AI
description: Build the data foundation and search infrastructure that AI capabilities depend on to deliver accurate, relevant results.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-managing-data-ai.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [AI data management, Workflow Data Fabric, Knowledge Graph, Now Assist Data Kit, AI Search, Now Assist in AI Search, External Content Connectors]
breadcrumb: [Enable AI Experiences]
---

# Managing data for AI

Build the data foundation and search infrastructure that AI capabilities depend on to deliver accurate, relevant results.

The quality and accessibility of your enterprise data directly determines how effective your AI capabilities are. Generative AI outputs are grounded in the content your instance provides. If that content is outdated, incomplete, or poorly structured, AI-generated summaries, answers, and recommendations reflect those gaps.

## Connecting enterprise data

Workflow Data Fabric is the unified data foundation that connects enterprise data where it lives, governs it through stable contracts, and makes it ready for workflows, analytics, and AI. Data is often scattered across dozens of systems, and integrations are rebuilt team by team. Workflow Data Fabric addresses this challenge so that once data is connected and governed, any team can discover and reuse it without rebuilding pipelines or compromising data integrity. To learn about connecting enterprise data where it lives, governing it through stable contracts, and making it ready for AI, see [Connecting enterprise data for AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-connecting-enterprise-data-ai.md).

## Knowledge Graph

Knowledge Graph creates a connected representation of data that maps entities and their relationships, adding context and meaning to information across your enterprise. This semantic layer enhances Virtual Agent, AI agents, and generative AI skills by enabling natural language queries against structured data, providing user context such as role, department, and location for personalized responses, and simplifying interactions through automatic slot-filling in forms and chat requests. To map the entities and relationships that give AI the context for natural language queries, personalized responses, and automatic slot-filling, see [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/knowledge-graph/knowledge-graph-landing.md).

## AI Data Kit

AI Data Kit enables you to add datasets to a data catalog and create data collections for evaluation in the ServiceNow SDK. When the base system generative AI skills don't fit your needs, AI Data Kit provides the tools for creating custom datasets that can be used to develop and evaluate custom AI capabilities on your instance. To build custom datasets and data collections for developing and evaluating AI capabilities in the ServiceNow SDK, see [AI Data Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-data-kit/now-assist-data-kit-landing.md).

## AI Search

AI Search is the retrieval layer that powers search experiences across the ServiceNow AI Platform®. AI Search indexes content from your instance and from connected external sources, then delivers relevant results through platform applications such as Global Search, Service Portal, Employee Center, and workspaces. Configuring AI Search effectively, including defining search sources, search profiles, and relevancy settings, is one of the highest-impact steps in your AI implementation. To learn about configuring the search sources, profiles, and relevancy settings that power retrieval across Global Search, portals, and workspaces, see [AI Search on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-ai-search-ai-platform.md).

## External Content Connectors

External Content Connectors index content and metadata from external source systems such as Confluence, SharePoint Online, Google Drive, and other supported repositories, making those systems searchable through AI Search. Indexing preserves the original user access permissions from the source system, so users only see content they are authorized to access. Connector administrators schedule content crawls and permission crawls to keep indexed content current. To learn about making external systems searchable through AI Search while preserving source permissions, see [External Content Connectors on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/platai-external-content-connectors.md).

**Note:** Data quality is an ongoing effort. Establish regular review cycles for your knowledge base, search sources, and AI training data to maintain the quality of AI outputs as your organization evolves.

