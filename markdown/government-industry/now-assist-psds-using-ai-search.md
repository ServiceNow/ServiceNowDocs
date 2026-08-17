---
title: Using AI Search in ServiceNow Otto for Public Sector Digital Services \(PSDS\)
description: Agents can search for information with single turn Q&amp;A using the AI Search feature in ServiceNow Otto for Public Sector Digital Services \(PSDS\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/government-industry/now-assist-psds-using-ai-search.html
release: zurich
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, ServiceNow Otto for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Using AI Search in ServiceNow Otto for Public Sector Digital Services \(PSDS\)

Agents can search for information with single turn Q&amp;A using the AI Search feature in ServiceNow Otto for Public Sector Digital Services \(PSDS\).

The ServiceNow Otto in AI Search application uses GenAI to extract actionable Q&amp;A Genius Result answers from the knowledge articles that are found in the Service Portal, Virtual Agent, Employee Center, and global searches. By using this application, an agent can improve the customer's experience by retrieving the relevant content from the knowledge base and generating concise answers. For more information, see [ServiceNow Otto for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/now-assist-ais.md).

## Legislation summarization

The ServiceNow Otto AI Search for CSM Workspace​ plugin synthesizes and summarizes information from multiple knowledge bases to deliver relevant, actionable AI-generated or AI-selected answers to search queries in a conversational format​.

Agents can use AI Search to pose a query directly in the search bar in the CSM Configurable Workspace, which will then generate an answer to their question by parsing and summarizing content from one or more knowledge bases. This single-turn, conversational search result replaces a long list of possible matches, and can help improve agent response accuracy and relevancy by allowing agents to review a summary of relevant content before responding to customers.

## Search configurations

A search application configuration specifies the search engine and the settings to use for search in a ServiceNow AI Platform application. The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration is provided with the CSM Configurable Workspace store app. To access this configuration, navigate to **AI Search &gt; Search Experience &gt; Search Applications.**

An admin can define and customize the source tables and knowledge bases that the ServiceNow Otto AI Search indexes data from by customizing the search profiles within the search application configuration for ServiceNow Otto for Public Sector Digital Services \(PSDS\).

For more information on search application configurations, see [Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/defining-search-app-cfgs-ais.md). For more information on how to set up and customize AI Search for use with ServiceNow Otto for Public Sector Digital Services \(PSDS\), see [Configure AI search for ServiceNow Otto for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/government-industry/now-assist-psds-configuring-ai-search-toggle.md).

