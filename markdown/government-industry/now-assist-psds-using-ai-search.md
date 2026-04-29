---
title: Using AI Search in Now Assist for Public Sector Digital Services \(PSDS\)
description: Agents can search for information with single turn Q&amp;A using the AI Search feature in Now Assist for Public Sector Digital Services \(PSDS\).
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Using AI Search in Now Assist for Public Sector Digital Services \(PSDS\)

Agents can search for information with single turn Q&amp;A using the AI Search feature in Now Assist for Public Sector Digital Services \(PSDS\).

The Now Assist in AI Search application uses Now LLM Service to extract actionable Q&amp;A Genius Result answers from the knowledge articles that are found in the Service Portal, Virtual Agent, Employee Center, and global searches. By using this application, an agent can improve the customer's experience by retrieving the relevant content from the knowledge base and generating concise answers. For more information, see [Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Legislation summarization

The Now Assist AI Search for CSM Workspace​ plugin synthesizes and summarizes information from multiple knowledge bases to deliver relevant, actionable AI-generated or AI-selected answers to search queries in a conversational format​.

Agents can use AI Search to pose a query directly in the search bar in the CSM Configurable Workspace, which will then generate an answer to their question by parsing and summarizing content from one or more knowledge bases. This single-turn, conversational search result replaces a long list of possible matches, and can help improve agent response accuracy and relevancy by allowing agents to review a summary of relevant content before responding to customers.

![Answer generated to agent query in CSM Configurable Workspace for Public Sector](../image/ais-psds.png "Generative AI Q&A in CSM Configurable Workspace")

## Search configurations

A search application configuration specifies the search engine and the settings to use for search in a ServiceNow AI Platform application. The **\[CSM AIS\] Configurable Workspace Search Config** search application configuration is provided with the CSM Configurable Workspace store app. To access this configuration, navigate to **AI Search &gt; Search Experience &gt; Search Applications.**

An admin can define and customize the source tables and knowledge bases that the Now Assist AI Search indexes data from by customizing the search profiles within the search application configuration for Now Assist for Public Sector Digital Services \(PSDS\).

For more information on search application configurations, see [Search application configurations](https://www.servicenow.com/docs/access?context=defining-search-app-cfgs-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US). For more information on how to set up and customize AI Search for use with Now Assist for Public Sector Digital Services \(PSDS\), see [Configure AI search for Now Assist for Public Sector Digital Services \(PSDS\)](now-assist-psds-configuring-ai-search-toggle.md).

