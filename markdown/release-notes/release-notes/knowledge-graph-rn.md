---
title: Knowledge Graph release notes
description: The ServiceNow Knowledge Graph enables you to create and manage a Knowledge Graph schema for default integrations with Virtual Agent. Knowledge Graph was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Knowledge Graph release notes

The ServiceNow® Knowledge Graph enables you to create and manage a Knowledge Graph schema for default integrations with Virtual Agent. Knowledge Graph was enhanced and updated in the Zurich release.

## Knowledge Graph highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   The Knowledge Graph landing page now includes a dedicated tagging section that allows users to create, edit, and manage tags.
-   Tagging configuration has been enhanced to support table synonyms, column synonyms, data filters and column filters to improve the accuracy of natural language queries.
-   Added an interactive guided tour for admins, providing step-by-step walk through of key features and configurations to simplify setup.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Users can use the new Enterprise Graph Knowledge Graph schema to map all instance tables and their relationships, enabling natural language queries across the entire database. It simplifies setup by eliminating custom schema creation and supports enhanced query accuracy.
-   Admins can create and use tags to prioritize relevant tables for specific use cases.
-   Users have the option to select Enterprise Graph\(small\) mode to restricts queries to tables in specified tags for narrower use cases, improving runtime speed and requiring tag specification.
-   Knowledge Graph now supports aggregate queries.

[Zurich Patch 2](../quality/zurich-patch-2.md)

-   Admins can create Knowledge Graph schema with Workflow Data Fabric tables that enables users to retrieve data from different systems without moving them. This ensures efficiency and security when working with external tables. This enables Knowledge Graph functionality to external tables

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Supports nodes from parent and grandparent nodes in the hierarchy.
-   Supports Configuration Management Database \(CMDB\) queries in Now Assist panel.

Zurich EA

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Knowledge Graph in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist platform. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.

See [Knowledge Graph](https://www.servicenow.com/docs/access?context=knowledge-graph-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Knowledge Graph is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Knowledge Graph features

-   **[Tagging in Knowledge Graph Designer](https://www.servicenow.com/docs/access?context=tagging-in-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The Knowledge Graph landing page now includes a dedicated tagging section that allows users to create, edit, and manage tags.


-   **[Using Enterprise graph schema](https://www.servicenow.com/docs/access?context=global-graph-schema&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enterprise Graph is a pre-configured Knowledge Graph schema that eliminates the need for custom schema creation in KG designer. By mapping all tables, the Enterprise Graph schema enhances the breadth of query capabilities, enabling database queries across all instance tables.


-   **[Tagging in Knowledge Graph Designer](https://www.servicenow.com/docs/access?context=tagging-in-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Tags are lists of key tables that are important for answering natural language questions. They provide hints to Enterprise Graph on which tables to prioritize when retrieving information, thereby improving the accuracy of results.


-   **[Test a Knowledge Graph schema](https://www.servicenow.com/docs/access?context=test-a-knowledge-graph-schema&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Enter a query and test the Knowledge Graph schema using different LLM options. You can also add previous conversations before you run the query.


-   **[Configure LLM for Knowledge Graph](https://www.servicenow.com/docs/access?context=configure-gpt-4-0-for-knowledge-graph&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Select and configure between Now LLM Service, Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow third-party model strategy.


## UI changes

-   **[Using Knowledge Graph Designer](https://www.servicenow.com/docs/access?context=using-knowledge-graph-designer&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Knowledge Graph is a ServiceNow AI Platform feature that is active on installation, by default.

## Additional requirements

Ensure that your instance is upgraded to XP7.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    ServiceNow® Now Assist uses generative AI that is designed to enhance user productivity and efficiency through conversation and proactive experiences.

-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search ServiceNow® Store application combines the power of search with the Now LLM Service generative AI model to answer questions in user searches with actionable AI-generated summaries of relevant Knowledge articles.

-   **[Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Unlock your enterprise productivity with ServiceNow® Virtual Agent. Increase deflections by empowering your employees and customers to serve themselves using a friendly messaging interface, featuring prebuilt conversations powered by artificial intelligence.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

