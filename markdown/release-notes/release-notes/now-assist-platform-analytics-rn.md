---
title: Now Assist in Platform Analytics release notes
description: Now Assist in Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through Generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics. Now Assist in Platform Analytics applications were enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Now Assist in Platform Analytics release notes

Now Assist in Platform Analytics consists of several skills and applications that let you generate and work with Platform Analytics objects through Generative AI. These skills let you analyze your business data through conversational interactions, without a technical knowledge of Platform Analytics. Now Assist in Platform Analytics applications were enhanced and updated in the Australia release.

## Now Assist in Platform Analytics highlights for the Australia release

-   AI-Generated Insights: Ask questions in natural language and see them turned into documented insights and visualizations. AI guides your analysis and suggests follow-up questions to deepen your exploration. Switch between two powerful modes, Standard analysis and Extended analysis, to uncover hidden insights.
-   Integration with External Data: Extend supported data sources and enable seamless integration with external systems through Data Fabric tables to gain more complete insights across the company’s diverse data.
-   Document Editing and Organization: Shape your data story exactly as you need it. Collect, edit, and organize insights directly within your exploration.
-   Collaboration with Other Users: Transform data analysis by working simultaneously with colleagues in a shared space to refine analyses, align on insights, and accelerate data-driven decisions.
-   Smart Integration with Contextual Intelligence: Trigger AI Data Explorer instantly from any application, list, or data visualization to access powerful insights enhanced by contextual awareness and usage patterns to highlight the data that matter most to you.

See [Now Assist in Platform Analytics](https://www.servicenow.com/docs/access?context=now-assist-platform-analytics&version=australia&pubname=australia-now-intelligence&ft:locale=en-US) for more information.

**Important:** Now Assist in Platform Analytics applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Changed in this release

-   **[Explore data from protected scopes](https://www.servicenow.com/docs/access?context=enable-aide-secure-scope-apps&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Provide access to protected application scopes to AI Data Explorer and Query Generation, and you can use data from those application tables in explorations. \(Query Generation bundle 5.2\)

-   **[Improvements to how segments are handled](https://www.servicenow.com/docs/access?context=querygen-segments&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    -   Manual segments are re-ranked to take priority over automatically generated segments.
    -   Prompt changes made to better support manual segments.
    -   More segments are passed to the LLM to increase the chance of the correct segment getting selected. Twelve segments are passed instead of three.
    -   Segments longer than 2000 characters are dropped to prevent context window bloat.
    \(Query Generation bundle 5.2\)

-   **[Customize semantic metadata in configuration tables](https://www.servicenow.com/docs/access?context=customize-semantic-metadata&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Customize semantic descriptions and usage instructions in the table and column configuration tables. Unlike the previous method of editing Entity and Dimension records, these changes can be transferred between instances through update sets.

-   **[View recommended actions](https://www.servicenow.com/docs/access?context=expl-view-recommended-actions&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    AI Data Explorer can suggest actions based on the insights that it generates in an exploration.

-   **[Ask questions about FX currency data](https://www.servicenow.com/docs/access?context=qg-supported-query-operations&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Query Generation now supports the FXCurrency \(Currency 2\) data type. This means that you can use AI Data Explorer to explore financial operations data, including those within Source-to-Pay Operations.

-   **[Benefit from improvements to segments](https://www.servicenow.com/docs/access?context=querygen-segments&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Segments are reusable definitions in Query Generation that provide non-obvious context to assist the semantic layer or LLM to select the correct dimension and values. Users can create manual segments via a new form. A scheduled job synchronizes manual and autogenerated segments. This job also cleans up segments to help surface the correct segments and reduce noise.

    Manual segments are re-ranked to take priority over automatically generated segments.

    Domain separation is also now supported, with a Domain field on the Segments table. Segments based on reports and filters inherit the source domain. Manual segments have domains that are passed up to the Segments table on synchronization. Segments are not supported for indicator sources or modules on domain-separated instances.


## Activation information

Now Assist applications for Platform Analytics are either included by default or you can install them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Platform Analytics experience](https://www.servicenow.com/docs/access?context=par-workspace&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)**

    Details of the data visualizations, filters, and dashboards that Now Assist for Platform Analytics skills generate.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Platform Analytics release notes](analytics-intel-report-rn-landing.md)

