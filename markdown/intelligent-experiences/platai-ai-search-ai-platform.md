---
title: AI Search on the ServiceNow AI Platform
description: AI Search is how the ServiceNow AI Platform finds and delivers the information you need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/platai-ai-search-ai-platform.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing data for AI, Enable AI Experiences]
---

# AI Search on the ServiceNow AI Platform

AI Search is how the ServiceNow AI Platform finds and delivers the information you need.

AI Search does not operate as a standalone search engine. It is embedded in the ServiceNow AI Platform so that every AI feature has a consistent, intelligent retrieval layer to draw from. AI Search automatically locates the most relevant information from across your ServiceNow environment and makes it available to AI features.

The ServiceNow AI Platform brings together the services, models, and infrastructure that power AI-driven experiences across ServiceNow. AI Search is a core component of that platform. It is the layer responsible for finding and delivering relevant information whenever an AI feature needs it, whether that feature is generating a response, completing a task, or helping a user find what they need.

AI Search retrieves information from the sources you configure and connects AI features such as Now Assist, AI agents, and virtual assistants to your organization's data. These sources include:

-   Native platform data: Tables, records, knowledge articles, catalog items, and other structured data within your ServiceNow instance.
-   External enterprise content: Documents and data from external repositories that are connected through External Content Connectors.
-   Custom indexed sources: Table and data sources you configure in AI Search to make content available for search applications, AI agents, and Now Assist.

The content AI Search can access is determined entirely by configuration. Sources must be indexed to be visible to AI Search and to be used by AI features.

## How AI Search works on the ServiceNow AI Platform

AI features on the ServiceNow AI Platform follow a Retriveal-Augmented Generation \(RAG\) request pattern. AI Search is the retrieval half of that pattern. Without it, AI features on the ServiceNow AI Platform lose their connection to your data and can't return responses that are accurate or relevant to your environment.

RAG request pattern:

1.  A request is received. A user asks a question, issues a command, or triggers an AI feature, a virtual assistant, or a search interface.
2.  AI Search retrieves relevant information, and processes the request using keyword matching, context, and machine learning-based ranking. It queries across your configured sources and returns the most relevant content.
3.  The retrieved context is passed to the AI feature. The results from AI Search provide the factual foundation that generative AI, AI agents, and other AI features use to generate responses, take actions, and present answers.
4.  The user receives a grounded response. As the response is built on retrieved enterprise data, not general AI knowledge alone, it reflects your organization's actual environment, records, and context.

## AI Search Admin

The AI Search Admin console makes it easy to integrate advanced AI Search features. It is a central hub for managing and monitoring AI Search capabilities across search applications. System administrators can use the AI Search Admin console to set up and manage AI Search in search applications, track AI Search activity, add features to AI Search, or access AI Search resources.

For more details, see [AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ais-admin-console.md).

## ServiceNow Otto for AI Search

ServiceNow Otto for AI Search combines AI Search retrieval with generative AI to deliver answers alongside search results. When a user submits a question, AI Search retrieves the most relevant content from your configured sources and provides it to the LLM, which generates a contextual response grounded in that content. These AI-generated answers appear as Genius Results in Global Search, Service Portal, Employee Center, and the Virtual Agent, helping users resolve issues through self-service without contacting support.

For more details, see [ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/now-assist-ais.md).

## What happens without AI Search

AI Search is not an optional add-on to the ServiceNow AI Platform. It is the component that gives AI features access to information. Without AI Search:

-   AI can't ground its responses in your organization's knowledge base, records, or catalog. Answers become generic or incomplete.
-   AI agents can't locate the necessary records, tasks, or data. Automated workflows stall or produce inaccurate results.
-   Virtual assistants can't surface relevant self-service content or route users to the right resources.
-   Search experiences fall back to basic keyword matching, losing the semantic understanding, intent recognition, and relevance ranking that AI Search provides.

When AI Search is configured and maintained, the entire ServiceNow AI Platform benefits. AI Search continuously improves its relevance ranking based on user activity and engagement, which means AI features become more accurate and useful over time.

## Instance requirements

To set up AI Search as part of the ServiceNow AI Platform:

-   Activate and configure AI Search on your instance.
-   Define data sources for AI Search indexing.
-   Create search profiles for your applications, virtual assistants, and AI agents.
-   Connect Now Assist to your search profile to activate generative AI features.

For configuration steps, administration guidance, and integration details, see [Using AI Search Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/using-ais-admin-console.md).

