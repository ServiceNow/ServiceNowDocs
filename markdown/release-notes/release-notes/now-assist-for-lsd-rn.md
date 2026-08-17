---
title: ServiceNow Otto for Legal Service Delivery \(LSD\) release notes
description: The ServiceNow ServiceNow Otto for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. ServiceNow Otto for Legal Service Delivery \(LSD\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# ServiceNow Otto for Legal Service Delivery \(LSD\) release notes

The ServiceNow® ServiceNow Otto for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. ServiceNow Otto for Legal Service Delivery \(LSD\) was enhanced and updated in the Zurich release.

## ServiceNow Otto for Legal Service Delivery \(LSD\) highlights for the Zurich release

Zurich Patch 12

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Legal Service Delivery \(LSD\). Check your entitlements to determine your access to specific features.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Disclose conflicts of interest using natural language from Now Assist in Virtual Agent rather than having to fill out intake forms.
-   Legal Request and Matter summarization now considers data from extended practice area tables when summarizing.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-landing.md) for more information.

**Important:** ServiceNow Otto for Legal Service Delivery \(LSD\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Submit COI request using ServiceNow Otto conversational intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-convi.md)**

    Submit a Conflict of Interest \(COI\) request through a natural language conversation. The conversational intake for Legal Conflict of Interest is available in the base system.


-   **[Now LLM LTS support for ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-llm-model-updates.md)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Changed in this release

-   **[ServiceNow® AI implementation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/sn-ai-implementation-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Summarize a legal request or matter by using ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-summarize-case.md)**

    Summarization now includes data from extended practice area tables, providing context‑rich summaries for your legal requests and matters.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install ServiceNow Otto for Legal Service Delivery \(LSD\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Browser requirements

The ServiceNow Otto for Legal Service Delivery \(LSD\) application works with the latest stable versions of popular web browsers. To find the list of supported browsers, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/browser-support.md).

## Related ServiceNow applications and features

-   **[Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/legal-management-overview.md)**

    Use to connect employees and legal teams through a unified platform with intelligent workflows, streamlining legal requests and managing complex matters efficiently via the Legal Counsel Center.

-   **[Overview tab in AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console to provide you with quick and easy access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[AI Admin Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Use to improve productivity and efficiency in your organization, deliver better self-service, suggest actions, provide answers, and empower your users to search more effectively.

-   **[Generative AI skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows. These AI skills include case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/lsd-rn-landing-page.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

