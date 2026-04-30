---
title: Now Assist in Platform Analytics release notes
description: Now Assist for Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through Generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-25"
reading_time_minutes: 5
---

# Now Assist in Platform Analytics release notes

Now Assist for Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through Generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics.

## Now Assist for Platform Analytics highlights

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Create "explorations"—editable documents where you analyze data with the help of AI. Refine responses, add your own input, and collaborate with others to make data-informed decisions faster.

Previous Patch releases

-   Generate and export Platform Analytics artifacts from conversational interactions in the Now Assist panel.
-   Benefit from a single, smooth experience in asking questions across all Now Assist for Platform Analytics skills, as well as other applications that incorporate Platform Analytics and AI, through a shared backend.

See [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) for more information.

**Important:** Now Assist for Platform Analytics applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New features, applications, and skills

-   **[Gather insights, plan, and collaborate in the AI Data Explorer](https://www.servicenow.com/docs/access?context=now-assist-explorer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) \(December 2025\)**

    Ask quick questions, receive tailored recommendations, and collaborate with AI and your colleagues to build long-term analysis. Enable teams to discuss and act on findings instantly. Centralize insights and narratives for better decision making. Guide users with contextual insights and suggestions.

    Main features include:

    -   [Extended analysis](https://www.servicenow.com/docs/access?context=hidden-insights&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) generates a deeper level of analysis that can reveal new insights, enabling you to make more informed decisions.
    -   [Add a data visualization from an exploration to a dashboard](https://www.servicenow.com/docs/access?context=add-data-viz-from-expl-to-dboard&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Share explorations with tagged users](https://www.servicenow.com/docs/access?context=share-now-assist-explorer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Duplicate an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-duplicate-exploration&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Duplicate an answer in an exploration](https://www.servicenow.com/docs/access?context=nowass-expl-dup-del-question-resp&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Summarize an exploration](https://www.servicenow.com/docs/access?context=summarize-exploration&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    AI Data Explorer leverages Query Generation to translate natural language questions into actionable insights. Query Generation enables users of AI Data Explorer to analyze their data and access a broader range of data sets. Key capabilities include:

    -   [Ability to add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
    -   [Workflow Data Fabric table support](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)
    -   [Database view support](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)

## Changed features

-   **[View recommended actions](https://www.servicenow.com/docs/access?context=expl-view-recommended-actions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://www.servicenow.com/docs/access?context=qg-supported-query-operations&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://www.servicenow.com/docs/access?context=querygen-segments&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

    Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments are not supported for indicator sources or modules on domain-separated instances.


-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Dashboard and data visualization export skill is active by default](https://www.servicenow.com/docs/access?context=export-db-dv-now-assist-panel&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US) \(January 2026\)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 5\): If this skill was previously unconfigured, it is turned on automatically \(the skill was never configured and turned on, then turned off again\). If the skill was previously turned on, then off, it remains inactive.

-   **[Query Generation skills are active by default](https://www.servicenow.com/docs/access?context=enable-query-generation&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    If the Generative AI Controller plugin is activated, the skills for Query Generation are activated by default. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Greater visibility into the Query Generation process](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    When you call Query Generation from AI Data Explorer or another application, you see each state that the query and response goes through before completing.

-   **[Multi-table source support](https://www.servicenow.com/docs/access?context=ask-expl-questions&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Query Generation supports related table conditions and dot-walking in queries.

-   **[Get insights and visualizations for Workflow Data Fabric tables](https://www.servicenow.com/docs/access?context=create-integrations-applications&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)**

    Ask AI Data Explorer information about Workflow Data Fabric data and get insightful responses. You must first add the Workflow Data Fabric tables to the Query Generation Semantic Table Configuration table.

-   **[Use database views in queries](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Generate visualizations or ask AI Data Explorer about data kept in database views, like SLA data. You have to add the database views to the Query Generation Semantic Table Configuration table.


-   **[Add tables to the semantic data layer](https://www.servicenow.com/docs/access?context=add-table-semantic-layer&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Choose which tables your users can query with generative AI for data analysis.

-   **[Monitor the health of the Query Generation back end](https://www.servicenow.com/docs/access?context=querygen-health-page&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    View the state of Now Assist for Platform Analytics LLM, plugins, system properties, components, and dependent products.


## Activation information

AI Data Explorer is available from the ServiceNow Store.

Query Generation, Analytics Generation, and the dashboard and data visualization export skill are installed with Generative AI Controller, which is included as a dependency of all Now Assist applications.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

After installation, activate the relevant skills. For more information, see the relevant Configure topics under [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    AI Data Explorer \(sn\_pa\_ai\_canvas\): The AI Data Explorer application allows users to explore data with help of AI, gather and organize findings, and collaborate with other users.


## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)**

    Details of the data visualizations, filters, and dashboards that Now Assist for Platform Analytics skills generate.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

