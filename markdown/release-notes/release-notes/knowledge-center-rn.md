---
title: Knowledge Center release notes
description: The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 5
---

# Knowledge Center release notes

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.

## Knowledge Center highlights for the Australia release

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Use the Article Health Score feature to view an article's quality score and get guidance to improve quality at the article level.
-   Use Knowledge Health Score to understand content quality across the Knowledge Base and drill down for more detailed insights.
-   Improve the clarity and accessibility of your articles with the Reading Ease scan that analyzes word count, sentence structure, and syllable count through an LLM-powered prompt.
-   Create knowledge articles with Now Assist using files stored in Box.
-   Create knowledge articles from Now Assist using files stored in Box.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   Use Knowledge Center to manage and distribute organizational knowledge through a centralized interface.
-   Enhance productivity and reduce redundant work so that users have access to accurate information.
-   Format content within a knowledge article using editing tools in the article editor.
-   Improve the quality and health of knowledge articles with article optimization scans.
-   Merge duplicate knowledge articles with Now Assist to improve content quality, maintain source references, and keep your Knowledge Base clear and reliable.

See [Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-center.md) for more information.

**Note:** Knowledge Center is available in the ServiceNow Store. For details, see the **Activation information** section of these release notes.

## Knowledge Center features

The following features are new in this release.

-   **[Knowledge Health score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-health-score.md)**

    Track Knowledge Base level quality by using Knowledge Base health score.

-   **[Search knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/search-knowledge-article.md)**

    Build a complete and accurate Knowledge Base. Focus on continuous improvement by discovering and filling content gaps, removing redundant information, and optimizing existing articles for better quality.

-   **[Create knowledge articles using Now Assist and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)**

    The Knowledge Center now integrates with **Box**. This enables authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Article Optimization with Reading Ease scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-reading-ease-scan.md)**

    The AI-based **Reading Ease** scan is integrated into the article optimization feature of the Knowledge Center, scans articles for readability. It provides actionable recommendations, and supports ongoing article improvement.


-   **[Search knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/search-knowledge-article.md)**

    Build a complete and accurate Knowledge Base. Focus on continuous improvement by discovering and filling content gaps, removing redundant information, and optimizing existing articles for better quality.

-   **[Knowledge Center Article Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-center-article-optimization.md)**

    Improve the quality and health of your knowledge articles by using the Article Optimization tool in the Knowledge Center to scan the articles, and get instant, actionable feedback.

-   **[Knowledge Center article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-article-editor.md)**

    Use the editing tools in the Knowledge Center to format knowledge article content such as text, images, and media.

-   **[Potential knowledge gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/understanding-knowledge-gaps.md)**

    Proactively identify and fill potential knowledge gaps. Identify missing knowledge articles and recurring issues that have incomplete or no knowledge article to refer to.

-   **[Merge duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/merge-duplicate-articles.md)**

    Merge selected duplicate knowledge articles into a new consolidated article using Now Assist in Knowledge Management. The merge preserves references to source articles and helps maintain a clean, high‑quality Knowledge Base.

-   **[Add a knowledge block to a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-add-knowledge-blocks-to-a-knowledge-article.md)**

    Insert one or more knowledge blocks into a knowledge article within a Knowledge Base. Each knowledge block is secured by user criteria, which control who can read or not read the content in an article.

-   **[Article optimization with article length scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/article-optimization-with-article-length-scan.md)**

    The article length scan is a script‑based, non‑AI scan that runs in the background while authors work on articles. This scan evaluates articles against two length‑based criteria, namely: minimum length for search engine optimization, and maximum length for AI search. Articles with fewer than 300 words are flagged for search engine optimization, and don't appear in search results. Articles exceeding 10,000 words are flagged for AI search indexation, and don't appear in AI‑powered search results.


## UI changes

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)

-   **[Knowledge Center Home Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-home-page.md)**

    The Knowledge Center home page includes article health score, knowledge health score, and adoption metrics to support process flow and user experience. It also includes dashboards and features such as article optimization, knowledge gap identification, and duplicate article management. The article editor is integrated with article optimization support.


-   **[Knowledge Center article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-article-editor.md)**

    The article editor displays a word count indicator next to the editor size controls. Authors can see the total number of words in an article as they write, helping them stay within recommended limits.


## Activation information

Knowledge Center is available by default to all roles in Knowledge Management.

## Plugin information

-   **Knowledge Center plugin**

    The following plugin is new in Australia:

    Knowledge Center \(**com.snc.knowledge\_center**\): Knowledge Center helps you manage knowledge articles from a single interface equipped with dashboards, insights, and AI-powered features.


## Related ServiceNow applications and features

-   **[CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-workspaces-configure.md)**

    The ServiceNow® CSM Configurable Workspace and ServiceNow® CSM Agent Workspace enable customer service agents to read Knowledge articles attached to their cases and gain additional information that helps them resolve cases more efficiently.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/fsm-application-landing-page.md)**

    Enable field service agents to read Knowledge articles that are attached to their work order tasks while they're offline through the Now Mobile Agent app. For more information, see [Knowledge articles on ServiceNow Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/access-information-you-need-mobile.md).

-   **[Communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/create-knowledge-from-communities.md)**

    Harvest Knowledge information from posts on a Community site. Create structured Knowledge articles from unstructured discussions around a question.

-   **[Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_CreateKnowledge.md)**

    Create structured Knowledge articles from information generated from a problem form that could be useful to solve similar issues.

-   **[Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/create-a-knowledge-article.md)**

    Resolve issues by searching for Knowledge articles from an incident. Flag issues with an article, edit articles from incidents, and report knowledge gaps while resolving an incident. Formalize tacit knowledge by creating articles from an incident using article templates.

-   **[Employee Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/employee-service-management-overview.md)**

    Use Knowledge blocks with HR Knowledge Management to simplify HR Knowledge authoring for writers and Knowledge consumption for readers. Enable an HR agent to identify cases that have insufficient knowledge coverage and to report knowledge gaps using the Demand Insights for HR Cases dashboard. For more information, see [Demand Insights for HR Cases dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/demand-insights-hrcases-dashboard.md).


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-capabilities-rn-landing.md)

