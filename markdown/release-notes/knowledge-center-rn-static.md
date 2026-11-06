---
title: Knowledge Center release notes
description: The ServiceNow Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release. See the following sections for release notes by version.The September 2026 release extends Health score configuration with Duplicate score and, identification of stale and expiring articles to the Article Optimization scan. It also adds style guides for AI-generated articles in Knowledge Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/knowledge-center-rn-static.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [ServiceNow AI Platform capabilities release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Knowledge Center release notes

The ServiceNow® Knowledge Center helps you manage knowledge articles from a single interface. Knowledge Center is available starting with the Australia release. See the following sections for release notes by version.

## About Knowledge Center

-   Centralizes knowledge articles, giving your organization full visibility into documented processes and information.
-   Enhances productivity by providing users immediate access to accurate, well-maintained knowledge content whenever they need it.
-   Enables formatting and styling of knowledge articles using intuitive editing tools within the article editor to ensure consistent, professional presentation.
-   Improves the quality and effectiveness of your knowledge base with article optimization scans that maintain article health and relevance.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Knowledge Center is available by default to all roles in Knowledge Management.

    To use auto-update, enable the Article Optimization skill and the `sn_km_center.ao_auto_update.enabled` system property. This property is enabled by default. Enable AO auto publish enabled on a Knowledge Base to automatically update articles in that Knowledge Base.

    To use auto-merge, enable the Identify duplicate articles and Merge Articles skills, and the `sn_km_gen_ai.auto_merge.enable` system property. If this property is inactive, users see the existing potential duplicate article experience. Enable Enable auto merge publish on a Knowledge Base to automatically merge and publish potential duplicate articles in that Knowledge Base. Use the `sn_km_gen_ai.auto_merge.confidence_threshold` property to set the confidence threshold for automatic merge and publish. Use the `sn_km_gen_ai.auto_merge.revert_ttl_days` property to set the number of days after which an automatically merged article can no longer be reverted.


**Parent Topic:**[ServiceNow AI Platform capabilities release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/now-platform-capabilities-rn-landing.md)

## Brazil Early Availability

The September 2026 release extends Health score configuration with Duplicate score and, identification of stale and expiring articles to the Article Optimization scan. It also adds style guides for AI-generated articles in Knowledge Center.

### What's new

-   ****

    In the Health score configuration page you can assign custom weights to the different scans both at the Article level and the Knowledge base level.

-   ****

    Article optimization scan comes with a new capability to identify stale and expiring articles. Gain insights at the article and the knowledge base level.

-   ****

    Connect ServiceNow Otto to a SharePoint site through an external content connection \(XCC\) so its content can be used when creating knowledge articles with AI. Microsoft SharePoint appears as an available source in the source list when you create an article using AI in Knowledge Center. ServiceNow Otto searches, aggregates, and summarizes relevant Microsoft SharePoint content to help generate the article.

-   ****

    Style guides are now available in Knowledge Center, so you can define the tone, voice, and terminology that AI follows when it generates knowledge articles. Administrators create a style guide, assign it to a knowledge base, and set its order. Authors then select it when they generate an article.


### What's changed

-   ****

    Auto-fix applies to an AI-based **Image Alt Tag** scan based on the confidence score. Also, the AO auto publish enabled flag is renamed to Enable automatic updating and publishing of articles from AO findings.

-   ****

    A new system property **Define the eligibility of time to revert the automatically merged or automatically updated articles** is available to configure the period within which you can revert a run. Based on the confidence score, merging will automatically update the existing article. The **Enable auto merge publish** flag is renamed to **Enable automatic merging and publishing of duplicate articles**.

-   ****

    Duplicate score is added as a part of the Article health score and contributes to the overall health score of the article along with the Article optimization score. The article editor features a side panel with an Overview of: the Article health score, Article Optimization issues, Usage insights and Duplicate content alert.

-   ****

    HR case data is included in knowledge gap analysis so that gaps related to HR cases appear in the Gaps area of Knowledge Center, alongside existing IT incident and CSM case gaps. To use this feature, an admin must turn on the **Knowledge gaps identification \(HR\)** AI skill in AI Admin Hub.


### What's deprecated or removed

-   **Now LLM Service deprecation notice**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


