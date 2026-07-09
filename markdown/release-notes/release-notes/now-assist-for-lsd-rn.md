---
title: Now Assist for Legal Service Delivery \(LSD\) release notes
description: The ServiceNow Now Assist for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. Now Assist for Legal Service Delivery \(LSD\) was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Now Assist for Legal Service Delivery \(LSD\) release notes

The ServiceNow® Now Assist for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. Now Assist for Legal Service Delivery \(LSD\) was enhanced and updated in the Zurich release.

## Now Assist for Legal Service Delivery \(LSD\) highlights for the Zurich release

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Disclose conflicts of interest using natural language from Now Assist in Virtual Agent rather than having to fill out intake forms.
-   Legal Request and Matter summarization now considers data from extended practice area tables when summarizing.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-landing.md) for more information.

**Important:** Now Assist for Legal Service Delivery \(LSD\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Submit COI request using Now Assist conversational intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-convi.md)**

    Submit a Conflict of Interest \(COI\) request through a natural language conversation. The conversational intake for Legal Conflict of Interest is available in the base system.


-   **[Now LLM LTS support for Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-llm-model-updates.md)**

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

-   **[Summarize a legal request or matter by using Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-summarize-case.md)**

    Summarization now includes data from extended practice area tables, providing context‑rich summaries for your legal requests and matters.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


## Activation information

Install Now Assist for Legal Service Delivery \(LSD\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

The Now Assist for Legal Service Delivery \(LSD\) application works with the latest stable versions of popular web browsers. To find the list of supported browsers, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/browser-support.md).

## Related ServiceNow applications and features

-   **[Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/legal-management-overview.md)**

    Use to connect employees and legal teams through a unified platform with intelligent workflows, streamlining legal requests and managing complex matters efficiently via the Legal Counsel Center.

-   **[Overview tab in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Use to improve productivity and efficiency in your organization, deliver better self-service, suggest actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows. These AI skills include case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/lsd-rn-landing-page.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

