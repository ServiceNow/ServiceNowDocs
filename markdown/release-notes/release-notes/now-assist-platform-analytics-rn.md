---
title: Now Assist in Platform Analytics release notes
description: Now Assist for Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through Generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-25"
reading_time_minutes: 4
---

# Now Assist in Platform Analytics release notes

Now Assist for Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through Generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics.

## Now Assist in Platform Analytics highlights

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Create "explorations"—editable documents where you analyze data with the help of AI. Refine responses, add your own input, and collaborate with others to make data-informed decisions faster.

Previous Patch releases

-   Generate and export Platform Analytics artifacts from conversational interactions in the Now Assist panel.
-   Benefit from a single, smooth experience in asking questions across all Now Assist for Platform Analytics skills, as well as other applications that incorporate Platform Analytics and AI, through a shared backend.

See [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-in-platform-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) for more information.

**Important:** Now Assist for Platform Analytics applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New features, applications, and skills

-   **[Gather insights, plan, and collaborate in the AI Data Explorer](https://www.servicenow.com/docs/access?context=now-assist-explorer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US) \(January 2026\)**

    Ask quick questions, receive tailored recommendations, and collaborate with AI and your colleagues to build long-term analysis. Enable teams to discuss and act on findings instantly. Centralize insights and narratives for better decision making. Guide users with contextual insights and suggestions.

    Main features include:

    -   [Optional deeper level of analysis](https://www.servicenow.com/docs/access?context=hidden-insights&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Add a data visualization from an exploration to a dashboard](https://www.servicenow.com/docs/access?context=add-data-viz-from-expl-to-dboard&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Share explorations with tagged users](https://www.servicenow.com/docs/access?context=share-now-assist-explorer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Duplicate an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-duplicate-exploration&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Duplicate an answer in an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-dup-del-question-resp&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Summarize an exploration](https://www.servicenow.com/docs/access?context=summarize-exploration&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    AI Data Explorer leverages Query Generation to translate natural language questions into actionable insights. Query Generation enables users of AI Data Explorer to analyze their data and access a broader range of data sets. Key capabilities include:

    -   [Ability to add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)
    -   [Workflow Data Fabric table support](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
    -   [Database view support](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)

## Changed features

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.

-   **[Query Generation skills are active by default](https://www.servicenow.com/docs/access?context=enable-query-generation&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    If the Generative AI Controller plugin is activated, the skills for Query Generation are activated by default.

-   **[Greater visibility into the Query Generation process](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    When you call Query Generation from AI Data Explorer or another application, you see each state that the query and response goes through before completing.

-   **[Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Query Generation supports related table conditions and dot-walking in queries.

-   **[Get insights and visualizations for Workflow Data Fabric tables](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Ask AI Data Explorer information about Workflow Data Fabric data and get insightful responses. You must first add the Workflow Data Fabric tables to the Query Generation Semantic Table Configuration table.

-   **[Use database views in queries](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Generate visualizations or ask AI Data Explorer about data kept in database views, like SLA data. You have to add the database views to the Semantic Table Configuration table.


-   **[Add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Choose which tables your users can query with generative AI for data analysis.

-   **[Monitor the health of the Query Generation back end](https://www.servicenow.com/docs/access?context=querygen-health-page&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    View the state of Now Assist for Platform Analytics LLM, plugins, system properties, components, and dependent products.


## Activation information

AI Data Explorer is available from the ServiceNow Store.

Query Generation, Analytics Generation, and the dashboard and data visualization export skill are installed with Generative AI Controller, which is included as a dependency of all Now Assist applications.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

After installation, activate the relevant skills. For more information, see the relevant Configure topics under [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-in-platform-analytics&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

## Plugin information

-   **[New plugins](https://www.servicenow.com/docs/access?context=c_ServiceNowPlugins&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The following plugins are new in Yokohama:

    AI Data Explorer \(sn\_pa\_ai\_canvas\): The AI Data Explorer application allows users to explore data with help of AI, gather and organize findings, and collaborate with other users.


## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US)**

    Details of the data visualizations, filters, and dashboards that Now Assist for Platform Analytics skills generate.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

