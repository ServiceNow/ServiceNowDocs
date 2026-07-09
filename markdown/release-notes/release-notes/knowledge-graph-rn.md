---
title: Knowledge Graph release notes
description: The ServiceNow Knowledge Graph enables you to create and manage knowledge graph schema for the out of the box \(OOTB\) integrations for Virtual Agent. Knowledge Graph is a new Now Assist platform capability in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-27"
reading_time_minutes: 5
---

# Knowledge Graph release notes

The ServiceNow® Knowledge Graph enables you to create and manage knowledge graph schema for the out of the box \(OOTB\) integrations for Virtual Agent. Knowledge Graph is a new Now Assist platform capability in the Yokohama release.

## Knowledge Graph highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Knowledge Graph now supports aggregate queries.
-   Improved accuracy for Now LLM Service.

[Yokohama Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-8.md)

-   Admins can create Knowledge Graph schema with Workflow Data Fabric tables that enables users to retrieve data from different systems without moving them. This ensures efficiency and security when working with external tables.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Knowledge Graph in addition to Now LLM Service and Azure OpenAI
-   Select your preferred large language model \(LLM\) provider for Now Assist platform. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Supports nodes from parent and grandparent nodes from the hierarchy.
-   Supports CMDB queries in Now Assist panel.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Seamlessly integrated with Now Assist in Virtual Agent, AI Agents and AI Search enabling personalized search results and context driven skills execution.
-   Seamless Integration with Now Assist in Virtual Agent for Natural Language Query.
-   Use Knowledge Graph as a tool to complete custom tasks for AI Agents.

[Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)

-   Knowledge Graph helps you in transforming large amount of data into a semantic representation, fostering more connected and customized user experiences.
-   Knowledge Graph boosts Virtual Agent by enabling large language models \(LLMs\) to provide contextually relevant responses tailored to each user.
-   Knowledge Graph creates a complex data model called Knowledge Graph schema with numerous entities and their relation within a few steps.
-   Knowledge Graph admins can use Knowledge Graph to create and manage the Knowledge Graph schemas. These Knowledge Graph schemas are the customized Knowledge Graph that consist of nodes, node properties, and edges.

See [Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/knowledge-graph-landing.md) for more information.

**Important:** Knowledge Graph is enabled automatically in your BU Generative AI Application. For details, see the "Activation information" section of these release notes.

## Knowledge Graph features

-   **[Test a Knowledge Graph schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/test-a-knowledge-graph-schema.md)**

    Enter a query and test the Knowledge Graph schema using different LLM options. You can also add previous conversations before you run the query.


-   **[Access Knowledge Graph Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/access-knowledge-graph-designer.md)**

    Knowledge Graph now has a new NLQ graph schema available prebuilt along with user profile schema. See [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2069778) for schema attributes.


-   **[Leverage Knowledge Graph prebuilt integration with Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/example-use-case-for-knowledge-graph.md)**

    Knowledge Graph provides the following new prebuilt integrations:

    -   Integration with Now Assist Virtual Agent: Helps requesters with personalized responses on people queries and Natural Language queries. Also supports people citation card.

-   **[Leverage Knowledge Graph prebuild integration with AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/leverage-knowledge-graph-prebuild-integration-with-agentic-ai.md)**

    Knowledge Graph provides the following prebuilt integrations:

    -   Integration with Now Assist AI agents for User Context: Helps users with personalized responses.
    -   Integration with AI agents as a tool: Used to perform specific tasks that are assigned to the AI agents.

-   **[Exploring Knowledge Graph](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-knowledge-graph.md)**

    Knowledge Graph helps requesters with personalized responses using its Integration with Now Assist Virtual Agent for User Context.

    Use Knowledge Graph integration with Now Assist Virtual Agent for Slot filling to helps pre-fill the slots for Virtual Agent topics using Natural Language Querying feature of Knowledge Graph.

-   **[Leverage Knowledge Graph prebuilt integration with Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/example-use-case-for-knowledge-graph.md)**

    Use the Knowledge Graph integrations with Now Assist Virtual Agent to utilize Knowledge Graph APIs built with LLM models, for personalized responses and slot-filling fields to execute LLM topics and skills in Virtual Agent.

-   **[Using Knowledge Graph Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/using-knowledge-graph-designer.md)**

    Use Knowledge Graph designer to manage Knowledge Graph schemas, their nodes, node properties and edges. You can also use the interface to create, edit, duplicate, or delete a Knowledge Graph schema.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Knowledge Graph is a ServiceNow AI Platform feature that is active by default if you have downloaded the Generative AI for BU.

## Additional requirements

Ensure that your instance is upgraded to XP7.

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/now-assist-ais.md)**

    The Now Assist in AI Search ServiceNow® Store application combines the power of search with the Now LLM Service generative AI model to answer questions in user searches with actionable AI-generated summaries of relevant Knowledge articles.

-   **[Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/virtual-agent-landing-page.md)**

    Unlock your enterprise productivity with ServiceNow® Virtual Agent. Increase deflections by empowering your employees and customers to serve themselves using a friendly messaging interface, featuring prebuilt conversations powered by artificial intelligence.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

