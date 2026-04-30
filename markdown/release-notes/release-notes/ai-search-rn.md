---
title: AI Search release notes
description: The ServiceNow AI Search application provides a consumer-grade search experience for ServiceNow AI Platform users. AI Search was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-02-20"
reading_time_minutes: 4
---

# AI Search release notes

The ServiceNow® AI Search application provides a consumer-grade search experience for ServiceNow AI Platform® users. AI Search was enhanced and updated in the Xanadu release.

## AI Search highlights for the Xanadu release

[Xanadu Patch 3](../quality/xanadu-patch-3.md):

-   Expand search recall by indexing content from knowledge blocks.

Xanadu:

-   Surface information across multiple CMDB tables with NLQ Genius Results.
-   Increase search precision for Japanese phrases that include nakaguro \(中黒, middle dot\) characters.
-   Scroll through multiple Genius Result answer cards in a carousel to select the most actionable answer for your question.

See [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

## Important information for upgrading AI Search to Xanadu

[Xanadu Patch 3](../quality/xanadu-patch-3.md):

-   After you upgrade to Xanadu Patch 3 from an earlier release, make knowledge block content searchable by reindexing all your indexed sources that include knowledge articles. For details on reindexing, see [Perform a full table index or reindex for a single AI Search indexed source](https://www.servicenow.com/docs/access?context=index-single-source-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) or [Perform a full table index or reindex for multiple AI Search indexed sources](https://www.servicenow.com/docs/access?context=index-multiple-sources-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Xanadu:

After you upgrade to Xanadu from an earlier release, perform the following steps to add the Dashboards, data visualizations, and KPIs navigation tabs to global search results in AI Search for Next Experience:

1.  Update the AI Search for Next Experience ServiceNow Store application to version 4 or later. For update instructions, see [Install an update to a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallUpdates&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
2.  Commit the update set provided in the [AI Search for Next Experience 4.0 PAR tables update sets \(KB1644544\)](https://support.servicenow.com/kb_view.do?sysparm_article=KB1644544) article in the Now Support Knowledge Base. To learn more about update sets, see [System update sets](https://www.servicenow.com/docs/access?context=system-update-sets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

## New in the Xanadu release

-   **\([Xanadu Patch 9](../quality/xanadu-patch-9.md)\) Improve semantic search with third-party embedding models**

    Use custom and third-party embedding models supported by the AI Search RAG application to generate more accurate and relevant semantic search results.


-   **\([Xanadu Patch 3](../quality/xanadu-patch-3.md)\) [Knowledge block content indexing](https://www.servicenow.com/docs/access?context=index-single-source-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When you index knowledge articles for search, AI Search now includes content from knowledge blocks to improve search recall.

-   **[NLQ Genius Results support searching for multiple CMDB tables](https://www.servicenow.com/docs/access?context=genius-result-nlq-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When your search includes terms that could match multiple CMDB tables, NLQ Genius Result answers display a drop-down list of potential CMDB table matches for each affected term. Use these drop-down lists to select the CMDB tables that you want to surface information for.

-   **[Middle dot support for Japanese](https://www.servicenow.com/docs/access?context=international-language-support-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Increase search precision for Japanese phrases that include nakaguro \(中黒, middle dot\) characters. When indexing Japanese text or searching in Japanese, AI Search preserves individual terms separated by a nakaguro instead of merging them into a single term.


## UI changes

-   **[Service Portal and Virtual Agent display Genius Result answer cards in a carousel](https://www.servicenow.com/docs/access?context=use-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When a search returns multiple Genius Result answers, Service Portal and Virtual Agent display Genius Result answer cards in a carousel instead of a list. The modified UI lets you scroll through multiple Genius Result answers while keeping your search query's regular results more accessible on the results screen.


## Changed in this release

-   **[Facets display refinement filters in the search user's language](https://www.servicenow.com/docs/access?context=create-facet-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When displaying reference field values as facet refinement filters, AI Search uses field value translations for the search user's language if available. If no translations are available for the user's language, AI Search uses translations for the system language.

-   **[Late binding security implementation preserves correct click rank search signals](https://www.servicenow.com/docs/access?context=content-security-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When late binding security removes inaccessible results, click rank search signals correctly reflect the final result ordering.


## Deprecations

Starting with the Now Assist in AI Search 8.0 release, the External Content Q&amp;A Genius Results feature is being prepared for future deprecation. It will continue to be supported until it is deprecated. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

AI Search is a ServiceNow AI Platform feature that is active by default.

## Browser requirements

AI Search doesn’t support Internet Explorer.

## Localization information

AI Search supports international languages. For details of language support by feature, see [Internationalization support for AI Search](https://www.servicenow.com/docs/access?context=international-language-support-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Advanced AI Search Management Tools](https://www.servicenow.com/docs/access?context=adv-ais-mgmt-tools-content-pack&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The Advanced AI Search Management Tools application adds new functionality to AI Search:

    -   Administrators can review dashboards with metrics, trends, and reports relating to AI Search usage and configuration.
    -   Administrators can test searches with the Search Preview UI to understand users' search results.
    -   Administrators with High Security access can bypass search source and content security filters in the Search Preview UI to see how these filters affect users' search results.
-   **[Now Assist in AI Search](https://www.servicenow.com/docs/access?context=now-assist-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The Now Assist in AI Search application combines the power of search with the Now LLM Service agentic AI model to answer questions in user searches with actionable AI-generated answers from relevant Knowledge articles.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Administrators can activate the ServiceNow® Knowledge Management Advanced plugin to install the FAQ \[kb\_template\_faq\] table. AI Search can return records in this table as Q&amp;A Genius Result answers for common user search questions.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

