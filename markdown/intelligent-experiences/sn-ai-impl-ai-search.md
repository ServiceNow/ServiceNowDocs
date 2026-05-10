---
title: AI Search readiness for Now Assist on the ServiceNow AI Platform
description: Now Assist in AI Search is built directly on the robust foundation of ServiceNow AI Search. AI Search provides the underlying infrastructure that enables Now Assist to retrieve and rank enterprise content—such as knowledge articles, records, and documentation—based on relevance and access permissions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, agentic AI, AI readiness]
breadcrumb: [Application readiness, ServiceNow AI implementation, Enable AI experiences]
---

# AI Search readiness for Now Assist on the ServiceNow AI Platform

Now Assist in AI Search is built directly on the robust foundation of ServiceNow® AI Search. AI Search provides the underlying infrastructure that enables Now Assist to retrieve and rank enterprise content—such as knowledge articles, records, and documentation—based on relevance and access permissions.

Because AI Search adheres to ServiceNow security models, responses are always grounded in content the user is authorized to access. Additionally, AI Search admin tools give you control over relevancy tuning, allowing you to refine how content is surfaced and ensure that Now Assist delivers the most useful and trustworthy results.

Every AI-generated answer includes citations and references, allowing users to see exactly where the information came from. This not only boosts confidence in the accuracy of responses, but also reduces the risk of hallucination by grounding outputs in your organization’s actual content.

To maximize its impact, Now Assist in AI Search should be activated before Now Assist is more broadly implemented. Once enabled, it powers actionable Q&amp;A through Genius Results cards in global search, Service Portal, Employee Center, and Virtual Agent.

## High-level checklist

-   **1. Verify AI Search status**

    Make sure AI Search is active on your instance. To check status, navigate to **All** &gt; **AI Search** &gt; **AI Search Status**. If AI Search is not active, select the **Request AI Search** button to initiate activation.

    See:

    -   [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ais.md)
    -   [Enable AI Search in supported ServiceNow AI Platform® applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/explore-now-platform-apps-ais.md)
-   **2. Review search sources**

    Configure search sources to determine what data will be searched by user queries.

    See:

    -   [Control access to searchable content using search sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/explore-search-sources-ais.md)
    -   [Create a search source for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/create-search-source-ais.md)
-   **3. Configure search sources for external content**

    Allows Now Assist Q&amp;A search to include external content.

    See:

    -   [Indexing and searching external content in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/external-content-ais.md)
    -   [Create an indexed source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/create-indexed-source-ais.md)
    -   [Configuring External Content Connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/configuring-ext-cont-connectors.md)
-   **4. Enable AI Search on one or more portals**

    Display AI Search results in the portals on your instance.

    See:

    -   [Search application configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/defining-search-app-cfgs-ais.md)
    -   [Enabling and configuring AI Search in ServiceNow AI Platform® applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/enable-configure-apps-ais.md)
-   **5. Install Now Assist in AI Search**

    Install a Now Assist product in the Now Assist Admin console.

    See: [Install Now Assist in AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/install-now-assist-ais.md)

-   **6. Enable Now Assist Q&amp;A Genius Results in AI Search portals**

    Specify the Now Assist Genius Result types you want to make available in each of your AI Search portals. Now Assist Multi-Content Response Genius Results use an LLM to generate search and chat responses that synthesize information from knowledge articles, Service Catalog items, and other available content types. Answers are presented in Q&amp;A format.

    See:

    -   [Enable Now Assist Genius Results in AI Search portals and mobile applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/enable-now-assist-gr-ais-apps.md)
    -   [Now Assist Q&amp;A Genius Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/now-assist-qna-genius-results.md)
-   **7. Verify AI Search widget customizations**

    Customized AI Search widgets may not correctly show Q&amp;A search results even when configured for Now Assist, since customizations get skipped during upgrades.

    See: [AI Search Genius Results widget options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/ais-genius-results-widget-options.md)


The ServiceNow AI Platform® offers a variety of search tools, which may return different answers for the same or similar searches. This disparity in results is expected. For more information, see [Search result disparities between AI Search and Now Assist search features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ai-search/search-disparities-ai-search-now-assist.md).

**Tip:** For more information, see [Now Assist in AI Search FAQ](https://www.servicenow.com/community/now-assist-articles/now-assist-in-ai-search-faq/ta-p/2686538) in ServiceNow Community.

