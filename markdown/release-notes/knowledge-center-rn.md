---
title: Knowledge Center release notes
description: The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.The September 2026 release extends Health score configuration with Duplicate score and, identification of stale and expiring articles to the Article Optimization scan.The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/knowledge-center-rn.html
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [ServiceNow AI Platform capabilities release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# Knowledge Center release notes

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.

## About Knowledge Center



-   Prioritize what matters most by assigning custom weights to individual scans at both the Article and Knowledge Base level in the Health Score configuration page.
-   Catch outdated content with the new stale and expiring article detection in the Article Optimization scan, available at both the article and knowledge base level.
-   Enrich AI-generated articles with SharePoint content by connecting ServiceNow Otto to a Microsoft SharePoint site via an external content connection \(XCC\). SharePoint now appears as a source option in Knowledge Center, letting Otto search, aggregate, and summarize relevant content to speed up article creation.
-   Fix image accessibility issues automatically with confidence-based auto-fix for the AI-based Image Alt Tag scan \(note: the AO auto publish flag is now called Enable automatic updating and publishing of articles from AO findings\).
-   Undo automated changes with confidence using the new system property that lets you define how long you have to revert auto-merged or auto-updated articles \(note: the auto merge publish flag is now called Enable automatic merging and publishing of duplicate articles\).
-   Spot duplicate content at a glance with the new Duplicate Score. It's now factored into the overall Article Health Score alongside Article Optimization. View it all in a redesigned side panel showing Health Score, Optimization issues, Usage insights, and Duplicate content alerts.
-   Close HR knowledge gaps faster by including HR case data in gap analysis. HR-related gaps now surface in Knowledge Center alongside existing IT and CSM gaps.

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)

-   ServiceNow Otto® is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Automatically update the knowledge article titles and header tags, findings generated from the Article Optimization scans based on the confidence score.
-   Automatically merge duplicate knowledge articles that are identified using identify duplicate articles skill.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)

-   Use the Article Health Score feature to view an article's quality score and get guidance to improve quality at the article level.
-   Use Knowledge Health Score to understand content quality across the Knowledge Base and drill down for more detailed insights.
-   Improve the clarity and accessibility of your articles with the Reading Ease scan that analyzes word count, sentence structure, and syllable count through an LLM-powered prompt.
-   Create knowledge articles with Now Assist using files stored in Box.
-   Create knowledge articles from Now Assist using files stored in Box.

[Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)

-   Use Knowledge Center to manage and distribute organizational knowledge through a centralized interface.
-   Enhance productivity and reduce redundant work so that users have access to accurate information.
-   Format content within a knowledge article using editing tools in the article editor.
-   Improve the quality and health of knowledge articles with article optimization scans.
-   Merge duplicate knowledge articles with Now Assist to improve content quality, maintain source references, and keep your Knowledge Base clear and reliable.

See [Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-center.md) for more information.

## Activation and other requirements

**Note:** Knowledge Center is available in the ServiceNow Store. For details, see the **Activation information** section of these release notes.

-   **Activation information**

    Knowledge Center is available by default to all roles in Knowledge Management.

    To use auto-update, enable the **Article Optimization** skill and the `sn_km_center.ao_auto_update.enabled` system property. This property is enabled by default. Enable **AO auto publish enabled** on a Knowledge Base to automatically update articles in that Knowledge Base.

    To use auto-merge, enable the **Identify duplicate articles** and **Merge Articles** skills, and the `sn_km_gen_ai.auto_merge.enable` system property. If this property is inactive, users see the existing potential duplicate article experience. Enable **Enable auto merge publish** on a Knowledge Base to automatically merge and publish potential duplicate articles in that Knowledge Base. Use the `sn_km_gen_ai.auto_merge.confidence_threshold` property to set the confidence threshold for automatic merge and publish. Use the `sn_km_gen_ai.auto_merge.revert_ttl_days` property to set the number of days after which an automatically merged article can no longer be reverted.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/now-platform-capabilities-rn-landing.md)

## September 2026

The September 2026 release extends Health score configuration with Duplicate score and, identification of stale and expiring articles to the Article Optimization scan.

### What's new

-   **[Health score configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-health-score-configuration.md)**

    In the Health score configuration page you can assign custom weights to the different scans both at the Article level and the Knowledge base level.

-   **[Review stale and expiring articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-review-stale-expiring-articles.md)**

    Article optimization scan comes with a new capability to identify stale and expiring articles. You can identify these both at the article and the knowledge base level.

-   **[SharePoint as a content source for Knowledge Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-article-using-sharepoint.md)**

    Connect ServiceNow Otto to a SharePoint site through an external content connection \(XCC\) so its content can be used when creating knowledge articles with AI. Microsoft SharePoint appears as an available source in the source list when you create an article using AI in Knowledge Center. ServiceNow Otto searches, aggregates, and summarizes relevant Microsoft SharePoint content to help generate the article.


### What's changed

-   **[Auto-fix article optimization findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/auto-update-articles.md)**

    Auto-fix applies to an AI-based **Image Alt Tag** scan based on the confidence score. Also, the AO auto publish enabled flag is renamed to Enable automatic updating and publishing of articles from AO findings.

-   **[Merge and publish potential duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/automerge-duplicate-articles.md)**

    A new system property **Define the eligibility of time to revert the automatically merged or automatically updated articles** is available to configure the period within which you can revert a run. Also, the Enable auto merge publish flag is renamed to Enable automatic merging and publishing of duplicate articles.

-   **[Article health score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/healthscore-metrics.md)**

    Duplicate score is added as a part of the Article health score and contributes to the overall health score of the article along with the Article optimization score. The article editor features a side panel with an Overview of: the Article health score, Article Optimization issues, Usage insights and Duplicate content alert.

-   **[Configure skills for potential gaps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configure-na-km.md)**

    HR case data is included in knowledge gap analysis so that gaps related to HR cases appear in the Gaps area of Knowledge Center, alongside the existing IT incident and CSM case gaps. To use this feature, an admin must turn on the **Knowledge gaps identification \(HR\)** AI skill in AI Admin Hub.


### What's deprecated or removed

-   **Now LLM Service deprecation notice**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. We're committed to bringing you the latest industry advancements while maintaining sovereignty-focused options, all hosted and governed by ServiceNow with the infrastructure and data protections you rely on today. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


## August 2026

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.

### What's new

-   **[Auto-fix article optimization findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/auto-update-articles.md)**

    Automatically update the articles by findings generated by article optimization scan. The Article Optimization skill must be enabled to use this feature.

-   **[Merge and publish potential duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/automerge-duplicate-articles.md)**

    Merge potential duplicate articles in a Knowledge Base, where the duplicate article drill- down widget groups them by topic and Knowledge Base. Enable auto-merge and auto-publish for a Knowledge Base, and set the confidence threshold and revert window at the system level.


### What's changed

-   **[Auto-fix article optimization findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/auto-update-articles.md)**

    The overview page shows automatic updates and manual review results for an automatically updated run, with progress indicators for bulk updates and reverts.

-   **[Merge and publish potential duplicate articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/automerge-duplicate-articles.md)**

    Merge potential duplicate articles in a Knowledge Base where, the duplicate article drill-down widget groups them by topic and Knowledge Base.


## June 2026

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.

### What's new

-   **[Knowledge Health score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-health-score.md)**

    Track Knowledge Base level quality by using Knowledge Base health score.

-   **[Search knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/search-knowledge-article.md)**

    Build a complete and accurate Knowledge Base. Focus on continuous improvement by discovering and filling content gaps, removing redundant information, and optimizing existing articles for better quality.

-   **[Create knowledge articles using AI and Box](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-create-article-with-Box.md)**

    The Knowledge Center now integrates with **Box**. This enables authors to use stored files as a source for generating knowledge articles with Now Assist.

-   **[Article Optimization with Reading Ease scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-reading-ease-scan.md)**

    The AI-based **Reading Ease** scan is integrated into the article optimization feature of the Knowledge Center, scans articles for readability. It provides actionable recommendations, and supports ongoing article improvement.


## Australia Early Availability

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.

### What's new

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


### What's changed

-   **[Knowledge Center article editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-article-editor.md)**

    The article editor displays a word count indicator next to the editor size controls. Authors can see the total number of words in an article as they write, helping them stay within recommended limits.


-   **[Knowledge Center Home Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/kc-home-page.md)**

    The Knowledge Center home page includes article health score, knowledge health score, and adoption metrics to support process flow and user experience. It also includes dashboards and features such as article optimization, knowledge gap identification, and duplicate article management. The article editor is integrated with article optimization support.


### Plugin information

-   **New plugins**

    The following plugin is new in Australia:

    Knowledge Center \(**com.snc.knowledge\_center**\): Knowledge Center helps you manage knowledge articles from a single interface equipped with dashboards, insights, and AI-powered features.


## Australia

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release.

### What's new

The following features are new in this release.

